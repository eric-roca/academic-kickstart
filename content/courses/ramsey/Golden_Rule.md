---
title: Golden rule
linktitle: Golden rule
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 8 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 8
---

## The Golden rule{#Golden-rule}

This capital level $\bar{k}$ is called the _modified_ Golden-rule level of capital.
The adjective _modified_ comes from the fact that the Golden rule level of capital is the level of capital, $k^{\mathcal{GR}}$ that maximises consumption, $c$ at the steady state, thus achieving maximum consumption: $c^{\mathcal{GR}}.$

We already know that, at the steady state:

$$k=f(k)+(1-\delta)k-c \implies c = f(k) -\delta k.$$

Hence, the level of capital that maximises $c$ is given by:

$$\frac{\partial c(k)}{\partial k} = f^{\prime}(k) - \delta = 0.$$

From here, the Golden-rule level of capital which maximises consumption at the steady state satisfies

$$f^{\prime}(k^\mathcal{GR}) = \delta \implies k^{\mathcal{GR}} = {f^{\prime}}^{-1}(\delta).$$

However, the _competitive_ steady-state level of capital $\bar{k}$ was characterised by

$$f^{\prime}(\bar{k}) = \frac{1-\beta (1 - \delta)}{\beta} \implies \bar{k} = {f^{\prime}}^{-1}\left(\frac{1-\beta (1 - \delta)}{\beta}\right). $$

Hence, $k^{\mathcal{GR}} = \bar{k}$ is only possible if and only if $\frac{1-\beta (1 - \delta)}{\beta} = \delta \implies \beta = 1.$ 

### Under- or over-accumulation of capital in the Ramsey model

According to the results before, the competitive steady-state level of capital maximises consumption at the steady state.
In fact, we have that

$$f^{\prime}(\bar{k}) = \frac{1-\beta (1 - \delta)}{\beta}$$
$$f^{\prime}(k^{\mathcal{GR}}) = \delta.$$

So, unless $\beta = 1,$ the economy is not at the Golden-rule level of capital.

Since $\frac{1-\beta (1 - \delta)}{\beta} > \delta$, we conclude that $\bar{k} < k^{\mathcal{GR}}:$ the level of capital is below its Golden-rule level.

We derived the level of capital in the competitive equilibrium by maximising total utility.
However, $\bar{k}$ does **not** maximise steady-state consumption.
In that sense, achieving the Golden Rule level of capital $k^{\mathcal{GR}}$ is **not** desirable from the viewpoint of utility maximisation.

