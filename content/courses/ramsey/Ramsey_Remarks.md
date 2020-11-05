---
title: Last remarks
linktitle: Last remarks
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 9

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 9
---

## Optimality

Before [we claimed]({{< ref "Steady_State_Ramsey.md#Golden-rule" >}}) that the solution is _optimal_ despite the fact that it does not maximise consumption at the steady state.
However, what we claimed was that the _entire path_ was optimal.
We can prove it by solving the Ramsey allocation problem from the perspective of the social planner.

### Social planner

A social planner maximises total welfare, given by:

$$\max \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t}).$$

The social planner directly allocates resources between consumption and investment, so he is not bothered by wages or interest rates.
In particular, he has to allocate total production and capital net of depreciation between $c\_{t}$ and $k\_{t+1}.$
Hence his intertemporal budget constraint reads:

$$f(k\_{t}) = c\_{t} + k\_{t+1} + (1-\delta) k\_{t}.$$
The planner operates under a certain level $k\_{0} > 0$ given.

The budget constraint is equivalent to the one we found in the competitive equilibrium.
Moreover, total welfare coincides, with household's utility.
Hence, the solutions will be the same, proving that the competitive equilibrium was optimal.

The two main equations of the model are relevant for the planner as well.
First, he must follow the Euler equation.
In fact, he can reduce present consumption by $\Delta c$ at time $t$ and save it.
The present-day cost is $u^{\prime} ( c\_{t} ) \Delta\_{c}$.
He obtains $f^{\prime}(k\_t) \Delta\_{c} + (1-\delta) \Delta\_{c}$ at time $t+1,$ which raises utility by $\left( f^{\prime}(k\_{t}) \Delta\_{c} + (1-\delta) \Delta\_{c} \right)  u^{\prime}\_{c\_{t+1}}.$
Optimality implies that this trade off is not possible anymore, hence, we obtain the Euler equation again.

Second, although the planner directly allocates consumption and investments, he must follow the technological constraint displayed above.
This does not represent preferences, and coincides with the household's budget constraint after clearing the markets.

Finally, observe that the _first welfare theorem_ directly applies:
if markets are competitive and there are no externalities, then the decentralised equilibrium is Pareto-efficient.
All conditions hold in the Ramsey model.

## The Golden rule

We have discussed before that, in the Ramsey model, the economy converges to a steady state with $\bar{k}$ below the Golden-rule level of capital $k^{\mathcal{GR}}$.

This contrasts with the Solow model: in the Solow model, a sufficiently high saving rate causes capital over-accumulation.
This opens the possibility of finding alternative paths that yield higher consumption levels in each and every period ---meaning that such a saving rate was not Pareto-efficient.

In the Ramsey model, savings are optimally derived from utility maximisation, and the level of utility depends on consumption.
Moreover, the model features _no_ externalities.
Consequently, the model cannot produce a situation whereby it is possible to increase consumption at each and every period: this would contradict optimisation.

However, $\bar{k} < k^{\mathcal{GR}}$ implies that it is possible to increase the saving rate today, build up the extra capital needed to reach $k^{\mathcal{GR}}$ and then be able to consume $c^{\mathcal{GR}} > \bar{c}$ at the steady state ---which, remember, lasts forever.
Suppose that we had reached the steady-state.
Why do the households not change their saving rate to reach $c^{\mathcal{GR}}?$
The reason is that households value present consumption more than future consumption.
Therefore, the current utility cost of a reduction in consumption is larger the future gains once discounted.
Because of the discount rate, the utility gains from an eventual permanent increase in consumption are bounded.

All in all, the economy converges to a value $\bar{k}$ below the steady state.
Because $\bar{k}$ is the optimal level of $k$ for the economy to converge to, it is known as the _modified Golden-rule_ capital stock.

We [had already noticed]({{< ref "Steady_State_Ramsey#Golden-rule" >}}) that the discount factor $\beta$ prevents the economy from reaching the Golden-rule level of capital.
According to our computation, the Golden-rule level of capital is only attained if $\beta = 1.$
This implies that present and future consumption are valued the same, which complements the discussion above.
