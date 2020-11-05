---
title: Steady state
linktitle: Steady state
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 5 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5
---

We assume that the intertemporal equilibrium exists and is unique.
As noted when characterising the [uniqueness of the temporary equilibrium]({{< ref "Equilibrium.md#temporary-equilibrium" >}}), assuming that $\sigma>1$ is a sufficient condition.
Therefore, the dynamics of capital are given by:

$$k\_{t+1} = \frac{1}{1+n}s(\omega(k\_{t}), f^{\prime}(k\_{t+1})).$$

Hence, $k\_{t+1}$ is an implicit function of $k\_{t}$:

$$k\_{t+1} = g(k\_{t}).$$

## Steady states

The steady states of this economy can be found solving the previous equation for $k\_{t+1} = k\_{t}=\bar{k}.$

$$\bar{k} = \frac{1}{1+n}s\left(\omega(\bar{k}), f^{\prime}(\bar{k})\right).$$

### Steady state with $\bar{k}=0$

A steady state with $\bar{k}=0$ is only possible if $f(0)=0$ or, equivalently, $\omega(0)=0.$
We may call this steady state an _autarky steady state._
In that case, since $\omega(0)=0$ and we know that individuals save a fraction of their income:

$$s(\omega(0), R(0)) < \omega(0) = 0.$$

Hence, given zero capital, savings are equally zero and capital remains there, constituting a steady state.

Alternatively, if it is possible to produce without capital (CES production function with large enough substitutability), the autarkic steady state does not exist.


#### Example of the autarkic steady state

Take $F(K,L)=(\alpha K^{\rho} + (1-\alpha)L^{\rho})^{\frac{1}{\rho}}$ and $u( c ) = \log( c ).$
Furthermore, assume a low elasticity of substitution, $\rho << 0.$
In intensive form, production equals:

$$f(k\_{t}) = (\alpha k\_{t}^{\rho} + (1-\alpha))^{\frac{1}{\rho}}.$$
Wages and savings are:

$$\omega(k\_{t}) = (1-\alpha)(\alpha k^\rho + (1-\alpha))^{\frac{1}{\rho}-1}$$
$$s\_{t} = \frac{\beta}{1+\beta}w\_{t}.$$

Then, capital accumulation becomes:

$$k\_{t+1} = \frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)\left[\alpha k\_{t}^\rho + 1 - \alpha \right]^\frac{1-\rho}{\rho}.$$

With low substitutability, $\rho < 0$, zero is always a possible steady state.
There can be two additional, positive steady states depending on the curvature of $k\_{t+1}.$

![steady states](/img/olg/example_1.png)

Similarly, the Cobb-Douglas case $\rho \rightarrow 0$ also has zero as a steady state.
However, it is unstable.

### Other steady state

The economy can also present interior steady states with $\bar{k}>0.$
Unlike the Ramsey model, here we can have stable and unstable steady states, as we shall see.
Moreover, the configuration varies depending on the production and utility functions.

![behaviour](/img/olg/example_2.png)

## Stability of the steady state

This model can feature one or several steady states.
This depends on the characteristics of the production and utility functions.

First, the dynamics of $k$ are monotonic: either continuously increase or decrease.
This follows from assuming a unique intertemporal equilibrium, [see also]({{< ref "Equilibrium.md#uniqueness-of-the-intertemporal-equilibrium" >}}).
This extra assumption also implies that the intermporal elasticity of substitution is _not too small_.
In particular, we operationalise (p. 25 in _de la Croix and Michel_.) it as:

$$\forall c>0, \quad u^\prime( c ) + c u^{\prime \prime}( c ) \geq 0 \Leftrightarrow \sigma( c ) \geq 1.$$

Due to the fact the monotonicity of the dynamics, capital can converge either to $0,\, \bar{k}\in (0,+\infty),\, $ or $+\infty.$

### The economy _never_ goes to $k = +\infty$

This is equivalent to saying that starting with a a high level of capital $k\_{0}$, the dynamics imply $k\_{t+1} < k\_{t}.$

First, we have that:

$$g(k) = \frac{1}{1+n}s(\omega(k),f^\prime(\underbrace{g(k)}\_{k\_{t+1}}))<\frac{\omega(k)}{1+n}.$$
This holds because savings $s$ are _always_ a fraction of wages $\omega.$ 

Second, we show that:

$$\lim\_{k \rightarrow +\infty}\frac{g(k)}{k} = 0.$$

To see the intuition for this limit, assume for a moment it holds.
Then, it must be that for large enough $k,\, g(k) = k\_{t+1} < k\_{t}$ and the dynamics are decreasing and converge to some $\bar{k}.$
In this case, $\bar{k}$ is the largest steady state, and because the dynamics are monotonic, the economy never goes to the other side of the steady state.

We show next that $\lim\_{k \rightarrow +\infty}\frac{g(k)}{k} = 0.$
We do so by showing that $\lim\_{k \rightarrow +\infty} \color{green}{\frac{\omega(k)}{k}} = 0.$

<details>
<summary>Detailed explanation</summary>
We start by noting that:

$$\color{green}{\frac{\omega(k)}{k}} = \color{red}{\frac{f(k)}{k}} - \color{blue}{f^\prime (k)} \leftarrow \omega(k) = f(k) - f^\prime (k) k.$$

When $k \rightarrow +\infty$, **the first term $\color{red}{\frac{f(k)}{k}}$** admits a positive limit, let's call it $\mathcal{l}\_{1}.$
This is because:

1. $\color{red}{\frac{f(k)}{k}} > 0.$
2. $\color{red}{\frac{f(k)}{k}}$ is decreasing:
	$$\frac{\partial \color{red}{\frac{f(k)}{k}}}{\partial k} = \frac{f^\prime(k)k-f(k)}{k^{2}} = - \frac{f(k) - f^\prime (k) k}{k^{2}} = - \frac{\omega(k)}{k^{2}} < 0.$$

The **second term $\color{blue}{f^\prime (k)}$** is decreasing and positive, thus it admits a limit $\mathcal{l}\_{2}$ when $k \rightarrow +\infty.$

Apply the mean value theorem evaluated at $k$ and $2k$:[^1]

[^1]: The mean value theorem states that, for a continuous function on $[a,b],$ there is a point $c \in (a,b)$ such that the derivative a $c, f^\prime( c)$ coincides with the slope of the secant between $a$ and $b, \frac{f(b) - f(a)}{b-a}.$
	[More information](https://en.wikipedia.org/wiki/Mean_value_theorem).

$$f(2k) - f(k) = (2k-k)f^\prime(k(1+\theta)), \quad \mathrm{with}\, \theta \in (0,1).$$
Then,
$$\frac{2f(2k)}{2k} - \frac{f(k)}{k} = f^\prime(k(1+\theta))$$
Taking the limit when $k \rightarrow +\infty$ we obtain $2\mathcal{l}\_{1}-\mathcal{l}\_{1} = \mathcal{l}\_{2} \implies \mathcal{l}\_{1} = \mathcal{l}\_{2}.$

Finally,

$$\lim\_{k \rightarrow + \infty}\color{green}{\frac{\omega(k)}{k}} =\lim\_{k \rightarrow +\infty}\color{red}{\frac{f(k)}{k}} - \color{blue}{f^\prime (k)}=  \mathcal{l}\_{1} - \mathcal{l}\_{2} = 0.$$
</details>

Since $\lim\_{k \rightarrow +\infty} \color{green}{\frac{\omega(k)}{k}}=0$ and $\frac{g(k)}{k} < \color{green}{\frac{\omega(k)}{k}}$ then $\lim\_{k \rightarrow +\infty}\frac{g(k)}{k} = 0.$
In conclusion, if the inital value of capital is large enough, the dynamics are decreasing and $k$ converges to an interior steady state $\bar{k}.$

## Examples

### Example 1: Log-utility and Cobb-Douglas

Suppose that $u(c,d) = \log ( c ) + \beta \log(d)$ and $f(k\_t) = Ak\_t^\alpha.$

The wage rate is given by 
$$w\_t = f(k\_{t}) - f^\prime (k\_{t}) = (1-\alpha)Ak\_{t}^\alpha$$

and the savings function is obtained solving
$$u^\prime(w\_{t} - s\_{t}) = \beta R\_{t+1} u^\prime (R\_{t+1}s\_{t}).$$

Rearranging and isolating $s$ we are left with the savings function

$$s\_{t} = \frac{\beta}{1+\beta}w\_{t}.$$

The dynamics are given by the capital accumulation law

$$k\_{t+1} = \frac{1}{1+n}s\_{t} = \frac{1}{1+n}\frac{\beta}{1+\beta}w\_{t} = \frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)Ak\_{t}^\alpha.$$

The model with log-utility and Cobb-Douglas production functions has two steady states: zero and a unique positive steady state.
We can solve for them: 

$$\bar{k} = \frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)A\bar{k}^\alpha \implies \bar{k} = \begin{cases} 0 \\\\\\ \left(\frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)A\right)^{\frac{1}{1-\alpha}} \equiv \phi^\frac{1}{1-\alpha}\end{cases}.$$

**Local dynamics: stability**

We check the stability of the two steady states using the first derivative evaluated at the steady state.
**Note:** in general we would use the Jacobian matrix, but the OLG model has only one equation in one variable.

Remember that, for a discrete-time system, a [_non-hyperbolic_]({{< ref "../math_app/steady_state.md#hyperbolic-steady-states" >}}) steady state is stable if it the determinant of the Jacobian (here the absolute value of the derivative) evaluated at the steady state is in the unit circle $(-1, 1).$

In our case:

$$g(k) = k\_{t+1} = \frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)Ak\_{t}^\alpha$$
$$g^\prime(k) = \frac{1}{1+n}\frac{\beta}{1+\beta}(1-\alpha)\alpha Ak\_{t}^{\alpha-1}> 0.$$

Then

$$\bar{k}=0 \implies g^\prime (0) = + \infty \quad \rightarrow \mathrm{unstable}$$ 
$$\bar{k}=\phi^\frac{1}{1-\alpha} \implies g^\prime(\phi^\frac{1}{1-\alpha}) = \phi \alpha \phi^\frac{\alpha-1}{1-\alpha} = \alpha \in (0,1) \quad \rightarrow \mathrm{stable}.$$

**Global dynamics**

Suppose we have $k\_{t+1} \geq k\_{t}$.
We show that the dynamics are bounded above by the steady state $\bar{k} = \phi^\frac{1}{1-\alpha}.$

$$k\_{t+1} \geq k\_{t} \Leftrightarrow g(k\_t) \geq k\_t \Leftrightarrow \phi k\_t^\alpha \geq k\_t \Leftrightarrow \phi \geq k\_t^{1-\alpha} \Leftrightarrow \bar{k} \geq k\_t.$$

![log_cd](/img/olg/Log_CD.png)

### Log-utility and CES technology

Under a CES specification, $y\_{t} = A \left[ \alpha k\_{t}^\rho + (1-\alpha) \right]^\frac{1}{\rho}, \rho \leq 1$
wages are given by 
$$\omega\_{t} = (1-\alpha)\left[\alpha k^\rho + 1 -\alpha \right]^{\frac{1-\rho}{\rho}}.$$
Hence, the dynamics of capital are governed by:

$$k\_{t+1} = g(k\_t) = \frac{1}{1+n}s\_{t} = \frac{1}{1+n}\frac{\beta}{1+\beta}A(1-\alpha)\left[\alpha k\_{t}^\rho + 1 - \alpha\right]^\frac{1-\rho}{\rho}.$$
The curve $g(k)$ is increasing:

$$g^\prime (k) = \frac{\beta A (1-\alpha)}{(1+n)(1+\beta )}(1-\rho)\left[ \alpha k^\rho + 1 - \alpha \right]^\frac{1-2 \rho}{\rho}k^{\rho -1} > 0.$$

Depending on the value of $\rho$ we can have different configurations regarding the steady states.
Ultimately, what matters is the concavity of the function $g(k\_{t}).$

$$g^{\prime \prime}(k\_t) = -\frac{1}{1+n}\frac{\beta}{1+\beta}A(1-\rho)\alpha\left[\alpha k^\rho+1-\alpha\right]^\frac{1-3\rho}{\rho}k^{\rho-2}\left(\rho \alpha k^\rho +(1-\alpha)(1-\rho)\right).$$

#### Unique steady state, $\bar{k} > 0$

If $\rho \in (0,1)$, the second derivative is clearly negative, and $g$ is concave.
Moreover, $g(0)>0$, so $\bar{k} = 0$ cannot be a steady state:

$$g(k\_{t}) = \frac{\beta A(1-\alpha)}{(1+n)(1+\beta)}(\alpha k^\rho + 1 - \alpha)^\frac{1-\rho}{\rho} \implies g(0)=\frac{\beta A(1-\alpha)^\frac{1}{\rho}}{(1+n)(1+\beta)}> 0.$$
In that case, the economy displays a unique steady state, and it is globally stable.


![ces0](/img/olg/ces0.png)

#### Unique $\bar{k}=0$ or multiple steady states

If $\rho < 0,$ the function $g(k)$ changes concavity.
In particular, there exists a level $\hat{k}$ such that:
$$g^{\prime \prime}(k) > 0\, \mathrm{if} \,  k < \hat{k}.$$
$$g^{\prime \prime}(k) < 0\, \mathrm{if} \, k > \hat{k}.$$
with 
$$\hat{k} = \left( - \frac{(1-\alpha)(1-\rho)}{\rho \alpha}\right)^\frac{1}{\rho} > 0 \, \mathrm{since}\, \rho <0.$$
Moreover, $g(0)=0$ so $\bar{k}=0$ can be a steady state.

In this case, there are two sub-cases:

1. If $k\_{t+1} < k\_{t} \implies \frac{\omega(k)}{k} < (1+n)\frac{1+\beta}{\beta}$ then the trajectory of $k\_{t+1}$ is always below $k$.
	Then, there is one unique steady state: $\bar{k}=0.$
	The economy converges towards this unique steady state.
    We can derive the condition above from:
    $\begin{align}
        k\_{t+1} < k\_{t} & \implies \frac{1}{1+n}s\left(\omega(k\_{t}),R\_{t+1}\right) < k\_{t}  \implies \\\\\\
        \frac{1}{1+n}\frac{\beta}{1+\beta}w\_t < k\_{t} & \implies \frac{w\_{t}}{k\_{t}} < (1+n)\frac{1+\beta}{\beta}.
        \end{align}$

2. If there is some $k\_{t+1} > k\_{t} \implies \frac{\omega(k)}{k} > (1+n)\frac{1+\beta}{\beta}$ then there are two positive steady states $\bar{k}\_{a} < \bar{k}\_{b}$ plus the zero steady state $\bar{k}=0.$
	1. All trajectories starting at $k\_0 < \bar{k}\_{a}$ converge to $\bar{k}=0$ and $\bar{k}=0$ is locally stable in the range $[0,\bar{k}\_{a}].$
	The steady state with $\bar{k}=0$ is a **poverty trap**: whenever the economy starts with a low enough level of capital, it will always converge towards the $\bar{k}=0$ steady state.
	2. Trajectories starting at $k\_0=\bar{k}\_{a}$ remain at $\bar{k}\_{a}$. This steady state is unstable.
	3. Finally, trajectories starting with $k\_0 > \bar{k}\_{a}$ converge towards $\bar{k}\_{b}$, which is a locally stable steady state in $(\bar{k}\_{a}, +\infty).$


![ces1](/img/olg/ces1.png)
