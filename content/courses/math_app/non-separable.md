---
title: Non-separable utility in OLG
linktitle: Non-separable utility in OLG
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  math_app:
    parent: Appendix
    weight: 5 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5
---

Here we analyse the behaviour of the savings function when utility is non-separable.
In particular, let utility be represented by

$$U = u(c,d).$$

We use the substitution method, but in this case we will introduce different alternatives, depending on the derivative we compute.
In particular, we introduce different elements of the budget constraint:

$$w = c + s$$
$$d = Rs$$
$$w = c + \frac{d}{R}$$

## $c$ and $d$ are normal goods

First, we derive conditions such that $c$ and $d$ are normal goods.
Optimality requires:

$$-u\_c (w-s,Rs) + R u\_d (w-s,Rs) =0.$$

### Consumption when young

We are interested in computing $\frac{\partial c}{\partial w}$ and showing it is positive so that $c$ is a normal good.
First, we rewrite the first order condition using some substitutions:

$$-u\_c (c, R(w-c)) + R u\_d (c, R(w-c)) =0.$$

Using implicit derivation we have:

$$\frac{\partial c}{\partial w} = - \frac{ -R u\_{cd} + R^2 u\_{dd}}{-u\_{cc} + u\_{cd} R + u\_{dc} R -u\_{dd} R^2} = \frac{R(u\_{cd} - R u\_{dd})}{-\underbrace{u\_{cc}}\_{<0} + 2 R u\_{cd} - R^2 \underbrace{u_{dd}}_{<0}} >0$$

<center> if and only if </center>

$$u\_{cd}- R u\_{dd} >0.$$

Since, in equilibrium $R = \frac{u\_c}{u\_d}$, the condition becomes

$$\frac{u\_{cd}}{u\_c} - \frac{u\_{dd}}{u\_d} > 0.$$

### Consumption when old

In this case, we write the optimality condition as

$$ - u\_c (w-\frac{d}{R}, d) + R u\_d(w-\frac{d}{R}, d).$$

Hence, we can compute the derivative

$$\frac{\partial d}{\partial w} = - \frac{-u\_{cc} + R u\_{cd}}{u\_{cc} \frac{1}{R} - u\_{cd} - u\_{cd} + u\_{dd} R} = \frac{R (R u\_{cd} - u\_{cc})}{-\underbrace{u\_{cc} +2Ru\_{cd} - R^2 u\_{dd}}\_{>0}} > 0$$

<center>if and only if</center>

$$R u\_{cd} - u\_{cc} > 0 \implies \frac{u\_{cd}}{u\_d}-\frac{u\_{cc}}{u\_c} > 0.$$

## Savings, wages and interest rate

We now show that savings are increasing in wages, and that they may increase or decrease with the interest rate.

First, we compute the relationship between savings and wages using the optimality condition $-u\_c(w-s, Rs) + u\_d(w-s, Rs)$:

$$\frac{\partial s}{\partial w} = - \frac{- u\_{cc} + Ru\_{cd}}{u\_{cc}-u\_{cd}R - u\_{cd}R + u\_{dd}R^2}= \frac{\overbrace{u\_{cc}-Ru\_{cd}}^{<0,\, \mathrm{normal\, goods}}}{\underbrace{u\_{cc}-2u\_{cd}R+u\_{dd}R^2}\_{<0}} \gt 0 $$

Using the same optimality condition we proceed with the relationship between savings and the interest rate:

$$\frac{\partial s}{\partial R} = - \frac{-u\_{cd}s+Ru\_{dd}s+u\_d}{u\_{cc}-2Ru\_{cd}+R^2u\_{dd}} = \frac{u\_d + s(Ru\_{dd}-u\_{cd})}{\underbrace{-u\_{cc} + 2Ru\_{cd}-u\_{dd}R^2}\_{>0}}.$$

Hence, the sign of the derivative depends on

$$u\_d + s(R u\_{dd} - u\_{cd}) \gtreqqless 0 \implies 1 + \underbrace{s}\_{\frac{d}{R}}\left(R \frac{u\_{dd}}{u\_{d}} - \frac{u\_{cd}}{u\_{d}}\right) \gtreqqless 0 \implies $$
$$1 + \underbrace{\frac{u\_{dd}}{u\_{d}}d}\_{-\frac{1}{\sigma}} - \frac{u\_{cd}}{u\_{d}}\frac{d}{R} \gtreqqless 0.$$

The relationship depends on the intertemporal elasticity of substitution ($\sigma$) and on the degree of complementarity between $c$ and $d$ as captured by $u\_{cd}.$
