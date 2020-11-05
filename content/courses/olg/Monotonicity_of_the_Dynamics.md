---
title: Multiple intertemporal equilibria
linktitle: Multiple intertemporal equilibria
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 6 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6 
---

In the OLG model, a unique intertemporal equilibrium arises if, for a given $k\_t$, the equation

$$H(k\_{t+1}) = k\_{t+1} - \frac{1}{1+n}s\left(\omega(k\_t), f^\prime(k\_{t+1})\right) = 0$$

has a unique solution.
We know that $\lim\_{k\rightarrow 0}H(k) < 0$ and $\lim\_{k\ rightarrow +\infty}H(k) > 0,$
which guarantees the existence of at least one solution.

Hence, if the function $H$ is monotonously increasing, the solution is unique.
This condition depends on the sign of:

$$\frac{\partial H(k\_{t+1})}{\partial k\_{t+1}} = 1 + \frac{1}{1+n}s^{\prime}\_{R}f^{\prime \prime}(k\_{t+1}).$$

We have different cases (check [the notes]({{< ref "savings_function.md" >}}) on the savings function):

1. $s^\prime\_{R} = 0$, which happens under log-utility. 
	In this case, $s^\prime\_{R} = 0 > \frac{1+n}{R^\prime(k\_{t+1})}$ and $H(k\_{t+1})$ is always increasing.

2. $s^\prime\_{R} >0$, the intertemporal elasticity of substitution is greater than 1 and individuals are willing to trade off higher future consumption against present consumption.
	Savings increase to consume more in the future.
	Then, clearly $s^\prime\_{R} > 0 > \frac{1+n}{R^\prime(k\_{t+1})}.$

3. $s^\prime\_{R} < 0$, we can have a non-monotonous capital path as $k\_{t+1}$ can be increasing or decreasing with $k\_{t}$.

Under case 3, the condition is not satisfied, multiple levels of $k\_{t+1}$ solve the intertemporal equilibrium.

### Non-monotonous dynamics

**Note:** Based on the [lecture notes of Groth, pp. 92--93](http://web.econ.ku.dk/okocg/MAT-OEK/Mak%C3%98k2/Mak%C3%98k2-2016/Forel%C3%A6sninger/Ch%203-2016-1.pdf)

Under case 3, the function $g(k)$ is backwards bending for some values of $k.$
This feature implies that there is more than one _intemporal equilibrium_, check [also]({{< ref "equilibrium.md/#temporary-equilibrium" >}}).
We ruled out such a possibility assuming that $\sigma( c ) \geq 1$, this is, we imposed a large enough intertemporal elasticity of substitution.

If this is not the case and $s^\prime\_{R}(\omega(k\_t), R(k\_{t+1})) < \frac{1+n}{R^\prime(k\_{t+1})}$ then there are multiple temporary equilibriums.

For instance, take an isoelastic utility function $u( c ) = \frac{c^{1-\frac{1}{\sigma}}-1}{1-\frac{1}{\sigma}}$ and a CES production with $A=20, \, \alpha = \frac{1}{2}, \, \beta = 0.3, \, n = 1.097, \, \sigma = 0.1, \, \rho = -2.$
First, since $\sigma < 1$, it allows for the possibility of having multiple temporary equilibria.
Second, we can verify that this is the case.
For example, if $k\_{t} = 1$, then:

$k\_{t+1} = \frac{1}{1+n} s(\omega(k\_{t}), R(k\_{t+1})) \implies k\_{t+1} = \begin{cases} 0.26 \\\\\\ 1.234 \\\\\\ 5.832 \end{cases}.$

In fact, for the entire range $k\_{t} \in [0.76, 1.37]$ there is multiplicity of equilibria.
Consequently, in all these cases we also have that $\frac{\mathrm{d}k\_{t+1}}{\mathrm{d}k\_t} < 0.$

![multiple_eq](/img/olg/backwards.png)
