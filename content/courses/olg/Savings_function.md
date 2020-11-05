---
title: Savings function
linktitle: Savings function
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

We now study how savings are affected by the remaining variables of the model.
Before turning to it, we compute the intertemporal elasticity of substitution on this model, because it turns out to be a crucial element influencing savings.
The _intertemporal elasticity of substitution_ is a special case of the [elasticity of substitution]({{< ref "../math_app/Elasticity_of_Substitution.md" >}}), that measures how the ratio of future to present consumption changes with the relative price (the interest rate).

## Intertemporal elasticity of substitution

The intertemporal elasticity of substitution is defined as:

$$\epsilon\_{d\_{t+1}, c\_{t}} = \frac{ \partial \left( \frac{d\_{t+1}}{c\_{t}} \right)}{\partial R\_{t+1}} \frac{ R\_{t+1}}{\left( \frac{d\_{t+1}}{c\_{t}} \right)}.$$

From the Euler equation we have $\frac{u^{\prime}(c\_{t})}{u^{\prime}(d\_{t+1})} = \beta R\_{t+1}.$
So, consumption when old $d\_{t+1}$ is going to be proportional to consumption when young $c\_{t}.$

Let $d\_{t+1} = x\_{t+1} c\_{t}.$
Then, the intertemporal elasticity of substitution becomes:


$$\epsilon\_{d\_{t+1}, c\_{t}} = \frac{ \partial x\_{t+1}}{\partial R\_{t+1}} \frac{ R\_{t+1}}{x\_{t+1}}.$$

We can compute it using the Euler equation $u^\prime(c\_{t}) = \beta R\_{t+1} u^\prime(x\_{t+1}c\_t).$
In fact, totally differentiating on both sides yields

$$0 = - \beta u^\prime(x\_{t+1}c\_t)\mathrm{d}R\_{t+1} + \beta R\_{t+1}u^{\prime \prime}(x\_{t+1}c\_t) c\_{t} \mathrm{d}x\_{t+1}.$$

Hence,

$$\frac{\mathrm{d}x\_{t+1}}{\mathrm{d}R\_{t+1}} = - \frac{u^\prime(x\_{t+1}c\_{t})}{R\_{t+1}u^{\prime \prime}(x\_{t+1}c\_t)c\_t} = - \frac{u^\prime (d\_{t+1})}{R\_{t+1}u^{\prime \prime}(d\_{t+1})c\_t}.$$

The intertemporal elasticity of substitution is then given by:


$$\epsilon\_{d\_{t+1}, c\_{t}} = \frac{\mathrm{d}x\_{t+1}}{\mathrm{d}R\_{t+1}}\frac{R\_{t+1}}{x\_{t+1}} = - \frac{u^\prime (d\_{t+1})}{R\_{t+1}u^{\prime \prime}(d\_{t+1})c\_t}\frac{R\_{t+1}}{\underbrace{x\_{t+1}}\_{\frac{d\_{t+1}}{c\_{t}}}} = - \frac{u^\prime(d\_{t+1})}{u^{\prime \prime}(d\_{t+1}) d\_{t+1}}.$$

**Note**: the intertemporal elasticity of substitution is equal to the inverse of the coefficient of relative risk aversion.
Risk averse individuals do _not_ want large changes in consumption, so they have a large risk aversion and are _not_ willing to trade off future and present consumption.
Conversely, risk neutral individuals do not mind abrupt changes in consumption, so they are willing to trade off future and present consumption.

Hence, in this model, the intertemporal elasticity of substitution coincides with the inverse of the coefficient of relative risk aversion.
**Note:** If you read p. 12 in _de la Croix and Michel_, they take a different approach and also refuse to use the concept or risk aversion: the model does not feature risk.

### CIES example

We illustrate the previous concept using a constant intertemporal elasticity of substitution utility function:

$$u( c ) = \frac{c^{1-\frac{1}{\sigma}}}{1-\frac{1}{\sigma}}.$$

In this case, we have the following Euler condition:

$$u^{\prime}(c\_{t}) = \beta R\_{t+1} u^{\prime}(d\_{t+1}) \implies \frac{d\_{t+1}}{c\_{t}} = \left( \beta R\_{t+1} \right)^\sigma.$$

Therefore, the intertemporal elasticity of substitution is

$$\epsilon\_{d\_{t+1}, c\_{t}} = \frac{ \partial  \frac{d\_{t+1}}{c\_{t}} }{\partial R\_{t+1}} \frac{R\_{t+1}}{\color{red}{\frac{d\_{t+1}}{c\_{t}}}}= \sigma (\beta R\_{t+1})^{\sigma-1}\beta R\_{t+1} \color{red}{\frac{1}{(\beta R\_{t+1})^{\sigma}}} = \sigma. $$

Meanwhile, the coefficient of relative risk aversion

$$RRA( c ) = - \frac{u^{\prime \prime}( c )}{u^{\prime}( c )}c = \frac{1}{\sigma} = \epsilon^{-1}\_{d\_{t+1},c\_{t}}$$

is the inverse of the intertemporal elasticity of substitution.

## The savings function

The savings function arises from solving:

$$s(w, R) = \arg \max \left[ u(w-s) + \beta u(Rs) \right].$$

Taking the first derivative with respect to $s$ and solving provides an implicit function: the savings function.

$$u^\prime(w-s)(-1) + \beta u^\prime(Rs)R = 0.$$

Denote this function $\phi(s,w,R)$:

$$\phi(s, w, R ) = -u^\prime(w-s)+ \beta R u^\prime(Rs) = 0.$$

Following from the assumption on the utility function, the savings function is continuous and continuously differentiable.

We are interested in determining whether savings increase or decrease with wealth and the interest rate.

### The effect of wages

We begin by analysing the effect of wages on savings:

$$\frac{\partial s}{\partial w} = - \frac{\frac{\partial \phi(\cdot)}{\partial w}}{\frac{\partial \phi(\cdot)}{\partial s}} = - \frac{ - u^{\prime \prime}(w-s)}{u^{\prime \prime}(w-s)+\beta R^{2} u^{\prime \prime}(Rs)} = \frac{1}{\underbrace{1+\beta R^{2} \underbrace{\frac{u^{\prime \prime}(Rs)}{u^{\prime \prime}(w-s)}}\_{>0}}\_{>1}} \in (0,1).$$

We thus have that the marginal propensity to save out of income is between 0 and 1:
$0 < s^{\prime}\_{w}  < 1,$
which reflects the fact that consumption goods are normal goods.

### The effect of the interest rate

Similarly, we compute the derivative of $\frac{\partial s(w,R)}{\partial R}$:

$$\frac{\partial s}{\partial R} = -\frac{ \beta u^{\prime}(d) + \beta R s u^{\prime \prime}(d)}{u^{\prime \prime}( c )+\beta R^{2} u^{\prime \prime}(d)} =- \frac{\beta u^{\prime}(d)\left[1-\frac{1}{\sigma (d)} \right]}{u^{\prime \prime}(c ) + \beta R^{2} u^{\prime \prime}(d)}.$$

Hence, 
$$\frac{\partial s}{\partial R} \gtreqqless 0 \quad \mathrm{if} \quad \sigma (d) \gtreqqless 1.$$

Two effects interact in this derivative:

* Wealth effect: if the interest rate rises, we obtain more out of the same savings, hence become wealthier.
	We consume more of all goods ---$c\_{t}$ and $d\_{t+1}$ are normal goods.
* Substitution effect: it is more profitable to save and consume $d\_{t+1},$ inducing savings.

When the inter-temporal elasticity of substitution is lower than 1, the substitution effect is dominated by the income effect. 
In that case, a rise in the rate of return has a negative effect on savings.
When the inter-temporal elasticity of substitution is higher than 1, households are ready to exploit the rise in the remuneration of savings by consuming relatively less today.
In this case, raising the rate of return boosts savings.
When the inter-temporal elasticity of substitution is equal to 1 (log-utility), the income effect exactly compensates the substitution effect and there is no effect of the rate of return on savings.

#### Example using a CIES function

Under a CIES utility, we have that:

$$s(w,R) = \frac{1}{1+\beta^{-\sigma}R^{1-\sigma}}w,$$

and 
$$s^{\prime}\_w  =\frac{1}{1+\beta^{-\sigma}R^{1-\sigma}} > 0.$$

However, $s^{\prime}\_{R} = - \frac{w R^{-\sigma}}{\left(1+\beta^{-\sigma}R^{1-\sigma}\right)^{2}}(1-\sigma)\gtreqqless 0$ depending on $\sigma \lesseqqgtr 1.$

**Log-utility:** 

In the case of logarithmic utility, savings are independent of the interest rate $R$ and are linear in wages.
Log-utility is a special case of the CIES function when $\sigma=1.$
In this case, the wealth and substitution effects cancel each other:

$$s(w,R) = \frac{\beta}{1+\beta}w.$$

#### Example using a CES function

**Note:** This is a transformation of the CIES function, so things will look rather similar.

$$U(c,d) = \left[ \alpha c^{\frac{\epsilon-1}{\epsilon}} + (1-\alpha)d^{\epsilon-1}{\epsilon} \right]^{\frac{\epsilon}{\epsilon-1}}.$$

From here, substituting $c=w-s$ and $d=Rs$, and solving for the optimal savings we obtain:

$$\begin{eqnarray}
& \alpha (w-s)^{-\frac{1}{\epsilon}} = (1-\alpha) R (Rs)^{-\frac{1}{\epsilon}} \\\\\\
& s = \frac{\left[ \frac{\alpha}{1-\alpha} \right]^{-\epsilon} w}{R^{1-\epsilon} + \left[\frac{\alpha}{1-\alpha} \right]^{-\epsilon}} = \frac{w}{1+\left[ \frac{\alpha}{1-\alpha} \right]^{\epsilon} R^{1-\epsilon}}.
\end{eqnarray}
$$

Therefore,

$$s^{\prime}\_{R} = - \frac{w}{\left(1+\left[ \frac{\alpha}{1-\alpha} \right]^{\epsilon} R^{1-\epsilon}\right)^{2}} \left(\frac{\alpha}{1-\alpha}\right)^\frac{\epsilon}{1-\epsilon}R^{-\epsilon}.$$

Then, when $\epsilon >1$ savings increase with the interest rate: $s^{\prime}\_{R} < 0.$
In that case, _the substitution effect dominates_.
**Alternative interpretation:** $\epsilon$ is the elasticity of intertemporal substitutability, hence if it is large, individuals are willing to substitute present consumption for future consumption.
**Alternative interpretation:** $\frac{1}{\epsilon}$ measures the relative risk aversion.
Hence, for large $\epsilon$ individuals accept more risk, meaning that they are willing to accept more changes in consumption.
Smoothing is less important.

Conversely, when $\epsilon <1$, an increase in the interest rate lowers savings: $s^{\prime}\_{R} < 0.$
In that case, the wealth effect dominates.
$\epsilon < 1$ also means that $c$ and $d$ are intertemporally complementary, and individuals want to consume them in constant proportions.
