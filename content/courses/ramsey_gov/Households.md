---
title: Households
linktitle: Households
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  ramsey_gov:
    parent: Introduction
    weight: 2 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

We modify the household's budget constraint to take into account the taxes they pay.
It remains exactly the same as [before]({{< ref "../ramsey/Households.md" >}}), except for the fact that less income is available for consumption:

$$k\_{t+1} + c\_{t} = w\_{t} + r\_{t}k\_{t} + (1-\delta) k\_{t} - \color{red}{T\_{t}}. \tag{1, Budget Const.} \label{eq:budget}$$

Except for this modification, households still present the same utility formulation and maximise:

$$\max \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t})$$
$$\mathrm{s.t.} \quad k\_{t+1} + c\_{t} = w\_{t} + r\_{t} + (1-\delta) k\_{t} - \color{red}{T\_{t}}.$$

Building up the Lagrangian [(as in the basic case)]({{< ref "../ramsey/Households.md#solving-the-household-s-problem" >}}) leads to the following equation:


$$\mathcal{L} = \sum\_{t=0}^{\infty} \beta^t u(c\_{t}) + \sum\_{t=0}^{\infty} \lambda\_{t}(w\_{t} + r\_{t}k\_{t} + (1-\delta)k\_{t} - c\_{t} - k\_{t+1} - \color{red}{T\_{t}}).$$

Despite the introduction of taxes $T\_{t}$, the optimality conditions are exactly the same as before.
Indeed, we introduced lump-sum taxes, and these do not affect optimality conditions, only allocations.[^1]

[^1]: From a mathematical perspective, we introduce a constant which has a nil derivative.
	Of course, the optimal allocation will be affected because less resources are available, but it _will not_ impact the optimal ratios.

Deriving and solving we obtain again the Euler equation:

$$\frac{\partial \mathcal{L}}{\partial c\_{t}} = \beta^{t} u^{\prime}(c\_{t}) - \lambda\_{t}$$
$$\frac{\partial \mathcal{L}}{\partial k\_{t+1}} = - \lambda\_{t} + \lambda\_{t+1}(r\_{t+1}+(1-\delta))$$

Setting both equal to zero to obtain the maximum, and combining the equations to get:

$$u^{\prime}(c\_{t}) = \beta u^{\prime}(c\_{t+1})(r\_{t+1}+1-\delta).$$

As before, we shall also impose the Transversality condition, which remains unaltered:

$$\lim\_{t \rightarrow \infty} \beta^{t}u^{\prime}(c\_{t})k\_{t+1} = 0.$$

It may seem that introducing government expenditures is innocuous: the Euler equation remains, market clearing will ensure that $r\_{t} = f^{\prime}(k\_{t})$ and $w\_{t} = f(k\_{t}) - f^{\prime}(k\_{t}) k\_{t}.$
However, it changes the steady state equilibrium:
households will consume less.

