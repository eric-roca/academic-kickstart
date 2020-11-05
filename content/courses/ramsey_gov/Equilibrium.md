---
title: Steady state
linktitle: Steady state
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  ramsey_gov:
    parent: Introduction
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

We close the model imposing market clearing.
This affects the budget constraint:

$$\begin{eqnarray}
k\_{t+1}  = w\_{t} + r\_{t+1}k\_{t} + (1-\delta)k\_{t} - c\_{t} - \color{red}{T\_{t}}, & \\\\\\
w\_{t}  = f(k\_{t}) - f^{\prime}(k\_{t})k\_{t},& \\\\\\
r\_{t}  = f^{\prime}(k\_{t}). &
\end{eqnarray}$$

Hence the dynamics for capital are now affected by public expenditures:

$$k\_{t+1} = f(k\_{t}) + (1-\delta)k\_{t} - c\_{t} - \color{red}{T\_{t}}.$$

The inclusion of the term $T\_{t}$ will impact the level of consumption ---and only consumption--- at the steady state.
Indeed, we can compute it as we did before.
From the Euler equation we have:

$$u^{\prime} (c\_{t}) = \beta (f^{\prime}(k\_{t+1}) + 1 - \delta)u^{\prime}(c\_{t+1}).$$
The budget constraint above determines the dynamics of capital.
Setting $c\_{t} = c\_{t+1} = \bar{c}^\mathcal{Gov}$ and $k\_{t} = k\_{t+1}= \bar{k}^{\mathcal{Gov}}$ reveals the steady-state levels of capital and consumption:

$$1 = \beta( f^{\prime}(\bar{k}^{\mathcal{Gov}}) + 1 - \delta) \implies f^{\prime}(\bar{k}^\mathcal{Gov}) = \frac{1-\beta(1-\delta)}{\beta},$$
$$\bar{c}^\mathcal{Gov} = f \left( \bar{k}^{\mathcal{Gov}} \right) - \delta \bar{k}^{\mathcal{Gov}} - \color{red}{G\_{t}},$$
where we have used $G\_{t} = T\_{t}.$

Two main comments are important here:

* The $c$-locus is not affected, hence the steady-state level of capital remains the same,
* The $k$-locus moves closer to the horizontal axis, because we subtract $G\_{t} > 0$ from it.
	This implies that the steady-state level of consumption is reduced.

![phase_diagram](/img/ramsey_gov/phase_diagram.png)
