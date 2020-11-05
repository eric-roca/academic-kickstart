---
title: Planner
linktitle: Planner
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 8

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 8

---

Suppose now, instead, that a central planner is in charge of organising consumption and investment for all individuals.
The planner operates by aggregating individual utility, discounting future generations at the rate $\gamma.$<br/>
**Note:** $\gamma$ is the discount rate of future _generations_, not how young people discount old-age utility.

Her utility considers the utility of all generations, including the initial old generation who owns the initial stock of capital $k\_0.$

## Planner's utility

Planner's utility reads:

$$\sum\_{t=-1}^\infty \gamma^t U(c\_t, d\_{t+1}).$$

Note that, although the planner can decide any allocation, she must respect the resource constraint:

$$f(k\_t) + (1-\delta) k\_t = c\_t + \frac{1}{1+n} d\_t + (1+n)k\_{t+1}.$$

Assume that $U(c\_t, d\_{t+1})$ is separable: $U(c\_t, d\_{t+1}) = u(c\_t) + \beta u(d\_{t+1}).$
Expanding the utility of the planner, we can reformulate it in more convenient terms:

$$\sum\_{t=-1}^\infty \gamma^t \left(u(c\_t)+\beta u(d\_{t+1}) \right) = $$
$$\gamma^{-1}u(c\_{-1}) +\gamma^{-1}\beta u(d\_0) + \gamma^0 u(c\_0)+ \gamma^0 \beta u(d\_1) + \gamma^1 u(c\_1) + \gamma^1 \beta u(d\_2) + \ldots $$
$$= \sum\_{t=0}^\infty \gamma^t \left(u(c\_t) + \frac{\beta}{\gamma} u(d\_t) \right) + \gamma^{-1}u(c\_{-1}).$$
The term $\gamma^{-1}u(c\_{-1})$ represents the consumption of the generation born at $t=-1$, but since it is a constant it will not affect the maximisation.

Hence, the planner's problem is now how to allocate consumption between the young and old that are alive during period $t$.

## Maximisation

We use a substitution to obtain the planner's optimal allocation, namely, the Euler equation;

$$\begin{eqnarray}
&\max\_{k\_{t+1}, c\_t, d\_t} \sum\_{t=0}^\infty \gamma^t \left(u(c\_t) + \frac{\beta}{\gamma} u(d\_t)\right) \\\\\\
&\mathrm{s.t.}\, f(k\_t) + (1-\delta)k\_{t} = c\_t + \frac{1}{1+n}d\_t + (1+n)k\_{t+1}. \end{eqnarray}$$

$$\max\_{c\_t, k\_{t+1}} \sum\_{t=0}^\infty \gamma^t \left( u(c\_t) + \frac{\beta}{\gamma}u\Bigg(\underbrace{\left[1+n\right]\left[f(k\_t)+(1-\delta)k\_t -(1+n)k\_{t+1} - c\_t\right]\Bigg)}\_{d\_t}\right).$$

Taking derivatives and equating them to zero yields:

$$\gamma^t u^\prime(c\_t) = \gamma^t \frac{\beta}{\gamma} u^\prime(d\_t)(1+n)$$
$$\gamma^t\frac{\beta}{\gamma}u^\prime (d\_t)(1+n)(1+n)=\gamma^{t+1}\frac{\beta}{\gamma}(1+n)u^\prime (d\_{t+1})\left(f^\prime (k\_{t+1}) + 1 - \delta \right).$$

Combining both equations we get the Euler equation:

$$u^\prime (c\_t) = \beta u^\prime (d\_{t+1})\left(f^\prime (k\_{t+1}) + 1 -\delta \right).$$

The planner's Euler equation coincides with the decentralised one, where we had $R\_{t+1} = f^\prime(k\_{t+1}) + 1 -\delta.$

However, the planner also allocates consumption between the young and the old at time $t$.
$$\gamma^t u^\prime(c\_t) = \gamma^t \frac{\beta}{\gamma} u^\prime(d\_t)(1+n)$$
In the centralised equilibrium, individuals do _not_ arbitrage between young and old consumption at time $t.$
We missed this equation because individuals are short-sighted, and only derive utility while alive.
Hence, they have no interest in trading off utility with the young generation once they are old.

## Steady state and modified golden rule

Using the fact that
$$\gamma^t\frac{\beta}{\gamma}u^\prime (d\_t)(1+n)(1+n)=\gamma^{t+1}\frac{\beta}{\gamma}(1+n)u^\prime (d\_{t+1})\left(f^\prime (k\_{t+1}) + 1 - \delta \right)$$
we can easily characterise the steady state knowing that $d\_t = d\_{t+1} = \bar{d}, k\_t = k\_{t+1} = \bar{k}.$

$$f^\prime (\bar{k}) = \frac{1+n}{\gamma}+1-\delta.$$

This equation provides us with the modified golden rule: the level of capital that maximises the planner's utility.
Clearly, if $\gamma=1$, the planner attributes the same weight to all generations and we recover the golden rule: $f^\prime(k) = n + \delta.$
As we discussed [before]({{< ref "Optimality.md" >}}), it is quite _unlikely_ the decentralised equilibrium converges towards the golden rule (modified or not).
