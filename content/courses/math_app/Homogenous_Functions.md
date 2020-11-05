---
title: Homogenous functions
linktitle: Homogenous functions
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  math_app:
    parent: Appendix
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1 
---

Notes based on Appendix A.1.1 of _de la Croix and Michel: A Theory of Economic Growth._ and Appendix M.B of _Mas-Colell, Whinston and Green: Microeconomic Theory._

## Homogeneity

A function of N variables $f(x\_{1}, \ldots, x\_{N})$ defined for all non-negative values $(x\_{1}, \ldots, x\_{N})$ is **homogeneous of degree $p$** if:

$$f(\lambda x\_{1}, \ldots, \lambda x\_{N}) = \lambda^{p} f(x\_{1}, \ldots, x\_{N}) \forall \lambda > 0.$$

Hence, if we scale all the components $x\_{1}, \ldots, x\_{N}$ of the function by the same amount $\lambda$, the result that we obtain is equal to the one before scaling times $\lambda^{p}.$
Production functions are often homogeneous of degree one: if all inputs are doubled, the output doubles as well.

**Example: A Cobb-Douglass production function**
A Cobb-Douglass production function is of degree one.
To see this, take its typical form:

$$f(x,y) = x^\alpha y^{1-\alpha}$$

and verify that $f(\lambda x, \lambda y) = \lambda f(x,y).$
Indeed, $f(\lambda x, \lambda y) = (\lambda x)^{\alpha} (\lambda y)^{1-\alpha} = \lambda x^{\alpha} y^{1-\alpha} = \lambda f(x,y).$

**Example: A CES production function**

A CES production function takes the form $f(x,y) = \left(\alpha x^{\eta} + (1-\alpha) y ^{\eta}\right)^{\frac{\zeta}{\eta}},\, \eta \leq 1.$
This type of function is homogeneous of degree $\zeta:$

$$f(\lambda x, \lambda y) = \left(\alpha \lambda^{\eta} x^{\eta} + (1-\alpha) \lambda^{\eta} y^{\eta}\right)^{\frac{\zeta}{\eta}} = \lambda^{\zeta} f(x,y).$$

### Properties of the derivatives of homogeneous functions

Assume that $f$ is continuously differentiable of as many degrees as required.

**The derivative of a function homogeneous of degree $p$ is homogeneous of degree $p-1$.**

If a function $f$ is of degree $p$, then for any $n = 1, \ldots, N$ the partial derivative $\partial f(x\_{1}, \ldots, x\_{N})/\partial x\_{n}$ is of degree $p-1.$

**Note:** see proof in Mas-Colell et al.

**Examples:**

1.  A Cobb-Douglas production function $f(x,y) = x^{\alpha} y^{1-\alpha}$ has derivates equal to $f\_{x}(x,y) =  \alpha x^{\alpha-1} y^{1-\alpha}$ and $f\_{y}(x,y) = (1-\alpha) x^{\alpha} y^{-\alpha}.$ 
Then it is easy to check that 
$$f\_{x}(\lambda x, \lambda y) = \lambda^{0} f\_{x}(x,y)$$ 
and 
$$f\_{y}(\lambda x, \lambda y) = \lambda^{0} f\_{y}(x,y),$$
which implies that derivatives are homogeneous of degree zero.

2. The CES function $f$: $f(x,y) = (\alpha x^{\eta} + (1-\alpha) y^{\eta})^{\frac{\zeta}{\eta}}$ is homogeneous of degree $\zeta$. 
The derivative function $f\_{x}(x,y) = \alpha \zeta x^{\eta - 1} (\alpha x^{\eta} + (1-\alpha)y^{\eta})^{\frac{\zeta-\eta}{\eta}}$ is homogeneous of degree $\zeta-1$: 
$$f\_{x}(\lambda x, \lambda y) = \alpha \zeta x^{\eta - 1}\lambda^{\eta-1}(\alpha \lambda^{\eta} x^{\eta} + (1-\alpha) \lambda^{\eta} y^{\eta})^{\frac{\zeta-\eta}{\eta}} = \lambda^{\zeta-1} \alpha \zeta x^{\eta - 1}(\alpha x^{\eta} + (1-\alpha) y^{\eta})^{\frac{\zeta-\eta}{\eta}} = \lambda^{\zeta-1} f\_{x}(x,y).$$
We can proceed similarly for $y$.

### Euler's formula

This is an interesting property of homogeneous functions.
In particular, it is useful in showing that, if the production function is homogeneous of degree one and factors are paid their marginal product, then profits are zero.

Suppose that $f(x\_{1}, \ldots, x\_{N})$ is homogeneous of degree $p$ and differentiable.
So, at any set of values $(\bar{x\_{1}}, \ldots, \bar{x\_{N}})$ we have:

$$\sum\_{n=1}^{N} \frac{\partial f(\bar{x\_{1}}, \ldots, \bar{x\_{N}})}{\partial x\_{n}} \bar{x\_{n}} = p f(\bar{x\_{1}}, \ldots, x\_{N}).$$

In words, if we multiply the derivatives by the variable with respect which we derivate and add all of them up, we retrieve the original function $p$ times.
Setting $p=1$ delivers the property we announced before.

**Example**

1. If the production function is homogeneous of degree one, under perfect competition (factors are paid their marginal product) firms make zero profits:
For simplicity, take a Cobb-Douglas function
$$f(x,y)=x^{\alpha} y^{1-\alpha}.$$ 
Marginal products are 
$$f\_{x} = \alpha x^{\alpha -1}y^{1-\alpha}$$ 
and 
$$f\_{y} = (1-\alpha) x^{\alpha} y^{-\alpha}.$$
Applying Euler's formula we get:
$$f\_{x} x + f\_{y} y = \alpha x^{\alpha - 1} y^{1-\alpha} x + (1-\alpha) x^{\alpha} y^{-\alpha} y = f(x,y).$$
Hence, the total amount produced ($f(x,y)$) is distributed to factor owners, and the firm necessarily makes zero profits.

### Applications to work with intensive-form functions {#intensive-form}


Often, we express the production function $F(K,L)$ in intensive terms.
This is, instead of focusing on the level of capital and labour, we are interested in the level of capital _per_ worker.
In other terms, we focus on $k \equiv \frac{K}{L}.$
Since we assume a production function of degree one, the transformation is simple.
Remember that if we multiply both factors by the same number, the result is also multiplied by that same number.
Hence, if we pick $\lambda = \frac{1}{L}$ we obtain:

$$f(k) \equiv F\left(\frac{K}{L}, \frac{L}{L} \right) = \frac{1}{L} F\left( K,L \right).$$
Therefore, rearranging:
$$F(K,L) = Lf(k).$$

We use this last relationship to compute the marginal products in intensive form:
$$F\_{K}(K,L) = \frac{\partial F(K,L)}{\partial K} = \frac{\partial L f\left(\frac{K}{L} \right)}{\partial K} = L \frac{1}{L}f\_{k}(k) = f^{\prime}(k).$$

Similarly:
$$F\_{L}(K,L) = \frac{\partial F(K,L)}{\partial L} = \frac{\partial L f\left(\frac{K}{L}\right)}{\partial L} = f\left(\frac{K}{L}\right)-Lf^{\prime}\left(\frac{K}{L}\right)\frac{K}{L^{2}} = f(k) - f^{\prime}(k)k.$$
Alternatively, we can use the Euler's formula to compute $F\_{L}(K,L)$.
$$F(K,L) = F\_{K} K + F\_{L} L$$
 hence, isolating 
$$F\_{L} = \frac{F(K,L) - F^{\prime}\_{K} K}{L}.$$
We know that $F(K,L)$ is homogeneous of degree one, hence $F\left(\frac{K}{L},1\right) = \frac{F(K,L)}{L}.$
Therefore,
$$F\_{L} = F\left(\frac{K}{L}\right) - F^{\prime}\_{K}\frac{K}{L} = f(k) - f^{\prime}(k) k,$$
where we use the fact that $F^{\prime}\_{K}$ is homogeneous of degree zero ($F$ was homogeneous of degree one) and we can divide the arguments without changing the value of the function:
$$F^{\prime}(K,L) =F^{\prime}\left(\frac{K}{L},\frac{L}{L}\right) = f^{\prime}(k).$$

