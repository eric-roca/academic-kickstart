---
title: Firms
linktitle: Firms
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 2 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

We assume that a large number of identical firms populate the economy.
Firms produce a single, homogeneous good using labour and capital.
The production function $F(K,L)$ has the following properties:

**Assumption R3:**
The production function satisfies the following properties:

* **R3.1** $F(K, L)$ is continuous and defined on $[0,+\infty)^{2},$
* **R3.2** $F(K, L)$ has continuous derivatives of every required order on $(0,+\infty)^2,$
* **R3.3** The production function is strictly increasing in both arguments:
	$F\_{i}(K, L) > 0$, 
* **R3.4** The production function is strictly concave:
	$$F\_{ii}(K, L) < 0$$
	$$F\_{ii}(K,L) F\_{jj}(K, L) - F\_{ij}(K, L)F\_{ji}(K, L)>0$$
* **R3.5** $F(K, L)$ is homogeneous of degree one.
* **R3.6** $F(K, L) \label{eq:inada_firm}$ satisfies the Inada conditions:
	$$\lim\_{K \rightarrow 0} F^\prime\_{K}(K, L) = \lim\_{L \rightarrow 0} F^\prime\_{L}(K, L) = +\infty$$
	$$\lim\_{K \rightarrow +\infty} F^\prime\_{K}(K, L) = \lim\_{L \rightarrow +\infty} F^\prime\_{L}(K, L) = 0.$$

**Note:** Assumption R3.4 implies that the  Hessian matrix of the production function is negative definite, hence the function is strictly concave.

Firms maximise real profits.
Since there are many firms competing, in equilibrium they make exactly zero profits.
Moreover, in equilibrium factors are paid their marginal productivity.
Since the production function $F$ is homogeneous of degree, we can write it in _intensive_ terms:

$$f(k) \equiv F\left(\frac{K}{L},1\right), \quad k \equiv \frac{K}{L}. \tag{5, Prod. Func.}$$

Because markets are competitive, capital earns its marginal product $\partial F(K,L)/ \partial K$ or, equivalently, $f^{\prime}(k)$ in intensive terms. Thus, the real interest rate at time $t$ is:

$$r\_{t} = f^{\prime}(k\_{t}). \tag{6, Interest rate}$$

The marginal product of labour is given by $\partial F(K,L)/\partial L.$
In intensive terms, it is equal to:

$$w\_{t} = f(k) - f^{\prime}(k) k. \tag{7, Wage}$$

**Note**: The [appendix]({{< ref "../math_app/Homogenous_Functions.md" >}}) details how to obtain the previous expressions.
