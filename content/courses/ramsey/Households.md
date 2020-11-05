---
title: Households
linktitle: Households
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 1 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

The economy is populated by a large number of identical households.
Each household is composed of one individual who lives indefinitely.

## Utility representation
Households  exhibit the following utility representation:
$$U = \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t}),\quad \beta \in (0,1) \tag{1, Utility}$$

**Assumption R1:**
The utility function satisfies the following properties:

* **R1.1** $u( c )$ is a continuous function defined over $[0,+\infty)$
* **R1.2** It has continuous derivatives of any required order defined over $(0,+\infty)$
* **R1.3** $u^{\prime}( c )>0$ and $u^{\prime \prime}( c )<0$
* **R1.4** $u (c )$ satisfies the Inada conditions: 
	$$\lim\_{c \rightarrow 0}u^{\prime}( c ) = +\infty$$
	$$\lim\_{c \rightarrow +\infty}u^{\prime}( c ) = 0$$

## Household's budget constraint

At each period, the household receives labour income $(w\_t)$ which is used to save $(k\_{t+1})$ and consume $(c\_t)$.
For simplicity, savings take the form of capital (instead of assets).
Households lend capital to firms, obtaining a real interest $r\_t$.
However, capital is subject to a constant depreciation rate $\delta$.

Therefore, at each period of time, households face the following budget constraint:

$$c\_{t} + k\_{t+1} = w\_{t} + r\_{t} k\_{t} + (1-\delta) k\_{t}. \tag{2, Budget C.}$$

The left-hand side represents expenditures during the period $t$:

* Consumption
* Saving

The right-hand side includes all sources of income:

* Wages
* Interests
* Remaining capital after depreciation
    * Effectively, households can _eat_ capital

**Note:** The budget constraint could have included _dividends_ $d\_{t}$ on the right-hand side.
	However, as we shall see, firms operate in perfect competition, and make zero profits.

## Solving the household's problem

First, we assume that households have **perfect foresight.**
This means that a household is able to perfectly forecast all the future values of the relevant variables when deciding.
For instance, at time $t$ the household is able to correctly compute $r\_{t+1}$ and $w\_{t+1}.$

**Assumption R2:** Households have perfect foresight.

We are interested in finding the optimal consumption and savings path, this is, the one that yields maximum utility.
Note that the problem is infinite, in the sense that we need to determine $c\_{t}$ and $k\_{t+1}$ for each and every period of time.
From the perspective of a household, the intertemporal maximisation problem reads:

$$\begin{eqnarray}
&\max\_{c\_{t}, k\_{t+1}} \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t}) \\\\\\
& c\_{t} + k\_{t+1}  = w\_{t} + r\_{t} k\_{t} + (1- \delta) k\_{t} \forall t\geq0.
\end{eqnarray}$$

---

First, we write the Langrangian equation corresponding to the problem:

$$\mathcal{L} = \sum\_{t=0}^{\infty} \beta^t u(c\_{t}) + \sum\_{t=0}^{\infty} \lambda\_{t}(w\_{t} + r\_{t}k\_{t} + (1-\delta)k\_{t} - c\_{t} - k\_{t+1}).$$

**Note:** this Lagrangian has infinite multipliers $\lambda\_{t},$ one for each period.

At time $t$, households have _two_ decisions to make:

* How much to consume at $t$: $c\_{t}$
* How much to save at $t$: $k\_{t+1}$

Therefore, we derive the Lagrangian function with respect to $c\_{t}$ and $k\_{t+1}$.

$$\frac{\partial \mathcal{L}}{\partial c\_{t}} = \beta^{t} u^{\prime}(c\_{t}) - \lambda\_{t}$$
$$\frac{\partial \mathcal{L}}{\partial k\_{t+1}} = - \lambda\_{t} + \lambda\_{t+1}(r\_{t+1}+(1-\delta))$$

Setting both expressions equal to zero to obtain the maximum and combining them yields:

$$u^{\prime}(c\_{t}) = \beta u^{\prime}(c\_{t+1})(r\_{t+1}+1-\delta). \tag{3, Euler Eq.}$$

This condition is called the **Euler equation**.
It tells us the optimal behaviour of the household.
Rearranging the expression a little bit, we are left with a clearer expression linking present and future consumption:

$$\frac{u^{\prime}(c\_{t})}{u^{\prime}(c\_{t+1})} = \beta (r\_{t+1} + 1 - \delta). \tag{3.1, Euler eq.}$$

Slightly more complex relationships can arise if the population grows or there is technological progress, see Romer, Chapter 2.

### The Euler equation

The Euler equation often appears in optimisation problems: either using discrete or continuous time.
The discrete-time version is relatively easier to interpret and obtain.
In our case, the Euler equation relates the present and future marginal utilities of consumption.
Imagine that the household decreased the amount consumed today, $c\_{t}$ by an infinitesimally small amount $\Delta\_{c\_{t}}$.
This causes a utility loss of $\Delta\_{c\_{t}} u^{\prime}(c\_{t})$.
Saving $\Delta\_{c\_{t}}$ until tomorrow and consuming all the proceedings generates a utility gain of $\Delta\_{c\_{t}}(r\_{t+1} + 1 - \delta) u^{\prime}(c\_{t+1})$.
This gain _must_ be, of course, discounted using the rate $\beta$ to compare present-day equivalents.

Since the household is optimising, both the loss and the gain must be equal, otherwise, there would be an alternative consumption level that would maximise utility.
Hence, putting everything together:
$\Delta\_{c\_{t}} u^{\prime}(c\_{t}) = \beta \Delta\_{c\_{t}} (r\_{t+1} + 1 - \delta) u^{\prime}(c\_{t+1}).$
Cancel $\Delta\_{c\_{t}} > 0$ on both sides to obtain the Euler equation.
Alternatively, we can interpret the Euler equation as stating that it is not optimal to slightly deviate from the optimal path, consuming slightly less for instance, and later returning to the optimal path.
**Remark:** the scheme we are putting in place here does not modify the intertemporal budget constraint because all the additional proceedings from savings are consumed.

### The Transversality Condition

The Euler equation is _not_ enough to fully determine the optimal sequence of consumption and savings.
For the moment, trajectories where capital or consumption grows boundedless are feasible, but these should not be optimal.

* First, consider the economy continuously accumulates capital. In that case, consumption must decrease towards zero.
Since we have assumed that $\lim\_{c \rightarrow 0}u^{\prime}( c )=+\infty$ (Inada condition) a small increase in consumption raises utility by a large amount, this is, the marginal utility of consumption is very large.
Hence, it cannot be optimal to accumulate capital and let consumption go to zero.
* Alternatively, let savings vanish. This case typically implies that $k\_{t}$ converges to zero in finite time (this is, for some $t<\infty$). The condition that capital must be positive prevents such cases.

**Note:** the preceding points are only descriptive of what the transversality condition implies.

In fact, that transversality condition reads as:

$$\lim\_{t \rightarrow \infty} \beta^{t}u^{\prime}(c\_{t})k\_{t+1} = 0. \tag{4, Trans. Cond.}$$

In general, we will obtain a steady-state equilibrium in which the path of capital and consumption are bounded.
This is, in the optimal solution, consumption $c\_{t} \rightarrow c^{\star}$ and capital $k\_{t} \rightarrow k^{\star}$.
In this case, the fact that $\beta \in (0,1)$ ensures the validity of the transversality condition.
