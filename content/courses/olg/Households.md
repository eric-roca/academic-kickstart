---
title: Households
linktitle: Households
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 2 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

## Building the budget constraint

Individuals live for two periods.
As before, we assume perfect foresight for individuals.
**Assumption OLG.1** Individuals have perfect foresight.

When **young**, they are endowed with _one unit of labour_ that they _supply inestastically._
**Assumption OLG.2** Individuals supply one unit of labour inelastically when young.
They receive the ongoing wage rate $w\_{t}$ and allocate this income between:

* current consumption $c\_{t}$,
* savings $s\_{t}$ that are invested in the firms.

Therefore, the budget constraint of a _young_ individual in period $t$ is:

$$ w\_{t} = c\_{t} + s\_{t}.$$

Once an individual reaches old age the next period, he consumes his savings (plus the interest rate received), reproduces ---exogenous fertility at rate $n$--- and dies.
Old people _do not care_ about anything happening after death.
Therefore, an agent has one unique choice:

* consumption when adult, $d\_{t+1}.$

The budget constraint for this period is:[^1]

$$s\_{t}(1 - \delta + r\_{t+1}) = d\_{t+1}.$$

with $\delta \in (0,1)$ being the capital depreciation rate.

[^1]: There plenty of alternative notations for the OLG model.
	One may write $c^{y}\_{t}$ and $c^{o}\_{t}$ for young and adult consumption.
	Similarly, the subindeces $t, t+1, \ldots$ denote the period of consumption, but we could have denoted the period in which the individual was born.

Hence, an individual faces two budget constraints.
However, we can collapse both into a unique _intertemporal budget constraint._

### The intertemporal budget constraint

In the economy, we have consumption as the numeraire.
It is more convenient for us to combine the two budget constraints corresponding to young and old ages into one single constraint.
Starting from

$$\left. \begin{eqnarray} 
w\_{t} = c\_{t} + s\_{t} \\\\\\
d\_{t+1} = s\_{t}(1 - \delta + r\_{t+1}) = s\_{t} R\_{t+1} \end{eqnarray}
\right\\}.$$

where $R\_{t} \equiv 1 - \delta + r\_{t+1}$ represents the return on savings, isolate $s\_{t}$ in the second equation and plug it in the first one:

$$ w\_{t} = c\_{t} + \frac{d\_{t+1}}{R\_{t+1}}. \tag{1, Int. Budget Const.} \label{eq:budget}$$

The intertemporal budget constraint indicates that the total present value of income ($w\_{t}$, the only source of income) equals the total present value of expenditures.
The present value of consumption when old $d\_{t+1}$ is discounted using the interest rate $R\_{t+1}.$

It is clear that savings, as usual, will be a function of wages $w$ and interests $R.$
So will consumption at all periods of time.

## Utility function

We suppose that the life-cycle utility function is additively separable:

$$U(c,d) = u( c ) + \beta u(d),\, \beta \in(0,1) \tag{2, Utility} \label{eq:utility}$$

where $\beta \in (0,1)$ is the psychological discount factor.
We assume that $u( c )$ has the properties

**Assumption OLG.3**

* **OLG.3.1** $u^{\prime}( c ) > 0,$
* **OLG.3.2** $u^{\prime \prime} ( c ) < 0,$
* **OLG.3.3** $ \lim\_{c \rightarrow 0} u^{\prime}( c) = +\infty.$

The last assumption $\lim\_{c \rightarrow 0} u^{\prime}( c ) = +\infty$ implies that an individual will always have a positive consumption ---as long as he has enough income to finance it.

Another important implication of the choice of the utility formulation is that $c$ and $d$ are normal goods: the demand is _not decreasing_ in wealth.
It follows from additive separability and concavity.
In the [Appendix]({{< ref "../math_app/non-separable.md" >}}) we discuss it in more detail for a non-separable utility function.

## The behaviour of individuals

At time $t$, young individuals receive their wages, consume and save while maximising the utility function.

$$\begin{eqnarray}
& \max u(c\_{t}) + \beta u(d\_{t+1}) \\\\\\
& \mathrm{s.t.} \quad w\_{t} = c\_{t} + s\_{t} \\\\\\
& \phantom{s.t.} \quad d\_{t+1} = R\_{t+1}s\_{t} \\\\\\
& \phantom{s.t.} \quad c\_{t} \geq 0, d\_{t+1} \geq 0.
\end{eqnarray}$$

We have two possibilities to solve this problem:

### Substitution

First, we can substitute $c\_{t}$ and $d\_{t+1}$ in the utility function, leading to:

$$u(w\_{t} - s\_{t}) + \beta u(R\_{t+1}s\_{t}).$$

This function is strictly concave with respect to $s\_{t}$ because of our assumptions.
The solution is _the savings function_:

$$s\_{t} = s(w\_{t}, R\_{t+1}).$$

The solution is interior as a consequence of the assumptions, and it is characterised by the first-order condition:

$$u^{\prime}(w\_{t} - s\_{t}) = \beta R\_{t+1} u^{\prime}(R\_{t+1}s\_{t}).$$

### Lagrangian

Instead, we can use the intertemporal budget constraint and build the Lagrangian:

$$\mathcal{L} = u(c\_{t}) + \beta u(d\_{t+1}) + \lambda\_{t}(w\_{t} - c\_{t} - \frac{d\_{t+1}}{R\_{t+1}}).$$

The first order conditions imply that:

$$u^{\prime}(c\_{t}) = \lambda\_{t}, \quad \beta u^{\prime}(d\_{t+1}) = \frac{\lambda\_{t}}{R\_{t+1}}$$

Combining both, we obtain the Euler equation:

$$u^{\prime}(c\_{t}) = \beta R\_{t+1} u^\prime (d\_{t+1}).$$
