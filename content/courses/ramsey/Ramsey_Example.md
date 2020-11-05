---
title: Example
linktitle: Example
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 7 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 7 
---

We can now completely solve an example.

## Utility and production functions

We assume that utility is logarithmic and we take a Cobb-Douglas production function.

$$\begin{eqnarray}
u(c\_{t}) = \log (c\_{t}), \\\\\\
F(K\_{t},L\_{t}) = AK\_{t}^{\alpha}L\_{t}^{1-\alpha}, \\\\\\
A >0, \alpha \in (0,1).
\end{eqnarray}
$$
We can check that both functions satisfy the Inada conditions:

$$\begin{eqnarray}\lim\_{c\_{t} \rightarrow 0}u^{\prime}(c\_{t}) = \lim\_{c\_{t} \rightarrow 0} \frac{1}{c\_{t}} = +\infty, \\\\\\
  \lim\_{c\_{t} \rightarrow +\infty}u^{\prime}(c\_{t}) = \lim\_{c\_{t} \rightarrow +\infty} \frac{1}{c\_{t}} = 0, \\\\\\
  \lim\_{K\_{t} \rightarrow 0} F^{\prime}\_{K\_{t}}(K\_{t}, L\_{t}) = \lim\_{K\_{t} \rightarrow 0} A\alpha K\_{t}^{\alpha - 1}L\_{t}^{1-\alpha} = +\infty, \\\\\\
  \lim\_{K\_{t} \rightarrow +\infty} F^{\prime}\_{K\_{t}}(K\_{t}, L\_{t}) = \lim\_{K\_{t} \rightarrow +\infty} A\alpha K\_{t}^{\alpha - 1}L\_{t}^{1-\alpha} = 0, \\\\\\
  \lim\_{L\_{t} \rightarrow 0} F^{\prime}\_{L\_{t}}(K\_{t}, L\_{t}) = \lim\_{L\_{t} \rightarrow 0} A (1-\alpha) K\_{t}^{\alpha}L\_{t}^{\alpha} = +\infty, \\\\\\
  \lim\_{L\_{t} \rightarrow +\infty} F^{\prime}\_{L\_{t}}(K\_{t}, L\_{t}) = \lim\_{L\_{t} \rightarrow +\infty} A (1- \alpha) K\_{t}^{\alpha}L\_{t}^{\alpha} = 0.
\end{eqnarray}
$$


The production function, expressed in intensive terms, becomes:

$$F(K\_{t}, L\_{t}) = L\_{T} F\left(\frac{K\_{t}}{L\_{t}},1\right) = L\_{t} f(k\_{t}) = L\_{t} k\_{t}^{\alpha}, k\_{t} \equiv \frac{K\_{t}}{L\_{t}}.$$
with total production $Y\_{t} = F(K\_{t},L\_{t})$ and production per capita is equal to $y\_{t} \equiv \frac{Y\_{t}}{L\_{t}} = f(k\_{t}).$

## Household's optimisation

Instead of using the results from previous sections, we develop again the utility maximisation.
First, we write down the household's budget constraint:

### Household's budget constraint

At each period, the total received income is composed of _wages_ and _interest_.
It can be spent on _consumption_ or _saving_.
Remember that capital depreciates at a rate $\delta \in [0,1].$
Hence, we receive back from firms $1-\delta$ times the capital we lend.
Therefore:

$$ w\_{t} + r\_{t}k\_{t} + (1-\delta)k\_{t} = c\_{t} + k \_{t+1}.$$

### Intertemporal utility maximisation: Lagrangian

The intertemporal utility maximisation problem is:

$$\begin{eqnarray}
\max\_{c\_{t}, k\_{t+1}}  \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t}) & \\\\\\
\mathrm{s.t.} \quad 	 w\_{t} + r\_{t} k\_{t} + (1-\delta)k\_{t} = c\_{t} + k\_{t+1}, \\\\\\
		 c\_{t}, k\_{t+1} >0, k\_{t=0} = k\_{0} > 0.
\end{eqnarray}
$$

The Lagrangian becomes:

$$ \mathcal{L} = \sum\_{t=0}^{\infty} \beta^{t} u(c\_{t}) + \sum\_{t=0}^{\infty} \lambda\_{t}(w\_{t} + (r\_{t} + 1 - \delta)k\_{t} - c\_{t} - k\_{t+1}).$$

We use the first-order conditions with respect to $c\_{t}$ and $k\_{t+1}$ to find the optimal consumption path: the Euler equation, which we combine later with the transversality condition.

$$\frac{\partial \mathcal{L}}{\partial c\_{t}} = \beta^{t} u^{\prime}(c\_{t}) - \lambda\_{t} = \beta^{t}\frac{1}{c\_{t}} - \lambda\_{t} = 0$$
$$\frac{\partial \mathcal{L}}{\partial k\_{t+1}} = -\lambda\_{t} + \lambda\_{t+1} (r\_{t+1} + 1 - \delta) = 0.$$

Combining both, we obtain the Euler equation:

$$\beta^{t}\frac{1}{c\_{t}} = r\_{t+1} \beta^{t+1} \frac{1}{c\_{t+1}} \implies c\_{t+1} = \beta (r\_{t} + 1 - \delta)c\_{t}.$$

Finally, we should remember to impose the transversality condition:

$$\lim\_{t \rightarrow +\infty} \beta^{t}u^{\prime}(c\_{t})k\_{t+1} = \lim\_{t \rightarrow +\infty}\beta^{t}\frac{1}{c\_{t}}k\_{t+1} = 0.$$

## Firm's optimisation

In this model, firms operate under perfect competition, making zero profits.
Moreover, factors are paid their marginal productivity.

$$r\_{t} = F^{\prime}\_{K\_{t}}(K\_{t}, L\_{t}) = \alpha K\_{t}^{\alpha - 1}L\_{t}^{1-\alpha} = \alpha \left(\frac{K\_{t}}{L\_{t}}\right)^{\alpha - 1} = \alpha k\_{t}^{\alpha -1},$$
$$w\_{t} = F^{\prime}\_{L\_{t}}(K\_{t}, L\_{t}) = (1-\alpha) K\_{t}^{\alpha} L\_{t}^{-\alpha} = (1-\alpha)\left(\frac{K\_{t}}{L\_{t}}\right)^{\alpha} = (1-\alpha) k\_{t}^{\alpha}.$$

Alternatively, using the information in the [Appendix]({{< ref "../math_app/Homogenous_Functions.md#intensive-form" >}}) and working directly with the intensive-form production function:

$$r\_{t} = f^{\prime}(k\_{t}) = \frac{\partial f(k\_{t})}{\partial k\_{t}} = \alpha k\_{t}^{\alpha -1},$$
$$w\_{t} = f(k\_{t}) - f^{\prime}(k\_{t})k\_{t} = k\_{t}^{\alpha} - \alpha k\_{t}^{\alpha - 1} k\_{t} = (1-\alpha)k\_{t}^{\alpha}.$$

## The dynamic system
We are now in a position to solve the model.
We have the following equations:

$$ c\_{t+1} = \beta (r\_{t+1} + 1 - \delta) c\_{t}, \\\\\\
   w\_{t} + r\_{t}k\_{t} + (1-\delta) k\_{t} = c\_{t} + k\_{t+1}, \\\\\\
   w\_{t} = (1-\alpha) k^{\alpha}\_{t}, \\\\\\
   r\_{t} = \alpha k^{\alpha-1}, \\\\\\
   \lim\_{t \rightarrow +\infty} \beta^{t}\frac{1}{c\_{t}} k\_{t+1} = 0.$$

Since markets clear, we substitute the wage and interest rate into the budget constraint.

$$c\_{t+1} = \beta (\alpha k^{\alpha-1} + 1 - \delta) c\_{t},$$
$$k\_{t}^{\alpha} + (1-\delta) k\_{t} = c\_{t} + k\_{t+1},$$
$$\lim\_{t \rightarrow +\infty} \beta^{t}\frac{1}{c\_{t}} k\_{t+1} = 0.$$

### Steady state

Before trying to solve for the optimal trajectory, we analyse the steady states of this economy.
A steady-state $(\bar{k}, \bar{c})$ is such that capital and consumption remain constant over time: $c\_{t+1} = c\_{t}$ and $k\_{t+1} = k\_{t}.$
Applying this idea to the equations above we get ---here we can temporarily forget about the transversality condition.

$$\bar{c} = \beta(\alpha \bar{k}^{\alpha-1} + 1 - \delta) \bar{c},$$
$$\bar{k}^{\alpha} + (1-\delta)\bar{k} = \bar{c} + \bar{k}.$$

Using the first equation we can easily get the steady level of capital:

$$ \bar{k} = \left(\frac{\alpha \beta}{1-\beta(1-\delta)}\right)^{\frac{1}{1-\alpha}}.$$

Applying $\bar{k}$ in the second equation yields the steady-state level of consumption:

$$ \bar{c} = \left(\frac{\alpha \beta}{1-\beta (1-\delta)}\right)^{\frac{\alpha}{1-\alpha}} - \delta \left(\frac{\alpha \beta}{1-\beta (1- \delta)}\right)^{\frac{1}{1-\alpha}}.$$ 

## Stability

First, we analyse the stability of the steady state, as we did in the [general case]({{< ref "Steady_State_Ramsey.md#stability" >}})
Since we are using log-utility, the coefficient of relative risk aversion $\epsilon\_{c} = 1.$

Instead of plugging the correct values in the Jacobian matrix $\bar{A}$, for the sake of clarity, we derive everything again:

$$\bar{A} = \begin{pmatrix}
\frac{\partial c\_{t+1}}{\partial c\_{t}} & \frac{\partial c\_{t+1}}{\partial k\_{t}} \\\\\\
\frac{\partial k\_{t+1}}{\partial c\_{t}} & \frac{\partial k\_{t+1}}{\partial k\_{t}}
\end{pmatrix}
$$
$$ = $$
$$\begin{pmatrix}
\beta \left( \alpha k\_{t+1}^{\alpha -1} + 1 - \delta \right) - \frac{\beta c\_{t} \alpha (\alpha-1) }{k\_{t+1}^{2-\alpha}} & \frac{\beta c\_{t} \alpha (\alpha -1)}{k\_{t+1}^{2-\alpha}} \left( \alpha k\_{t}^{\alpha-1} + 1 - \delta \right) \\\\\\
-1 & \alpha k\_{t}^{\alpha -1} + 1 - \delta \end{pmatrix}$$

Evaluating it at the steady state:
$$\bar{A}\bigr\rvert\_{\substack{
	k\_{t} = k\_{t+1} = \bar{k} \\\\\\
	 c\_{t} = c\_{t+1} = \bar{c}
}
}
   = \begin{pmatrix}
	1 - \beta \bar{c}  \alpha (\alpha -1) \bar{k}^{\alpha -2}  & \alpha (\alpha -1 ) \bar{c}  \bar{k}^{\alpha -2} \\\\\\
	-1  & \frac{1}{\beta}
\end{pmatrix},$$

where we have used $1 = \beta \left( \alpha \bar{k}^{\alpha -1} + 1 - \delta \right)$ at the steady state.

### Eigenvalues

We can use the fact $\mathrm{tr}(\bar{A}) = \lambda\_{1} + \lambda\_{2}, \mathrm{det}(\bar{A}) = \lambda\_{1} \lambda\_{2}.$
Therefore:

$$\lambda\_{1} \lambda\_{2} = \frac{1}{\beta} $$
$$\lambda\_{1} + \lambda\_{2} = \frac{1}{\beta} + 1 - \beta \bar{c} \alpha (\alpha-1) \bar{k}^{\alpha -2}.$$
The first equation implies that either a) $\lambda\_{1} > 0, \lambda\_{2} > 0$ or b) $\lambda\_{1} < 0, \lambda\_{2} < 0.$ 
However, since $\lambda\_{1} + \lambda\_{2} > 1$ b) is impossible.
Then, $\lambda\_{1} > 0, \lambda\_{2} > 0.$
Substitute $\lambda\_{1} \lambda\_{2} = \frac{1}{\beta} $ in the second equation:

$$ \lambda\_{1} + \lambda\_{2} = 1+ \lambda\_{1} \lambda\_{2} - \beta ( \alpha (\alpha - 1) \bar{k}^{\alpha -2}\frac{\bar{c}}{\epsilon\_{\bar{c}}}.$$

Rearranging:
$$ \lambda\_{1} + \lambda\_{2} - \lambda\_{1} \lambda\_{2} =  1+  - \beta \alpha (\alpha -1) \bar{k}^{\alpha -2}\frac{\bar{c}}{\epsilon\_{\bar{c}}} > 1 \implies \lambda\_{1} + \lambda\_{2} - \lambda\_{1}\lambda\_{2} - 1 >0.$$
Factorisation leads to:
$$(1 - \lambda\_{2})(\lambda\_{1} - 1) > 0.$$
Therefore, since $\lambda\_1,\, \lambda\_2 >0:
$$ \lambda\_{2} < 1 \implies \lambda\_{1} \in (0,1)$$
$$ \lambda\_{1} > 1 \implies \lambda\_{2} \in (1,+\infty)$$
and **the steady state is saddle.**

## Trajectory

Describing the trajectory around the steady state analytically would be cumbersome.
One possibility is to introduce an alternative production function of the $Ak$ family which alleviates this problem, see the notes by [Maurice Obsfeld](https://eml.berkeley.edu/~webfac/obstfeld/e202a_f13/lecture2.pdf)

Instead, we solve this section numerically.
In particular, assume that $\alpha = 0.3, \\, \beta = 0.9, \\, \delta = 0.1.$
The initial level of capital $k\_{t=0} = 1.$

With these values, we have the following:

$$\bar{k} = 1.65202, \\, \bar{c}=0.997329, \\, \bar{A} = \begin{pmatrix} 1.08029 & -0.089214 \\\\\\ -1 & 1.11111 \end{pmatrix}.$$

The eigenvalues of the matrix $\bar{A}$ are
$$\lambda\_{1} = 0.796618 \in (-1,1)$$ $$\lambda\_{2} =1.39479 > 1.$$

One possible set of eigenvectors is given by:

$$v\_{1} = (0.314494 , 1), v\_{2} = (-0.283675, 1)$$
which are associated with $\lambda\_{1}$ and $\lambda\_{2}$, respectively.
Hence, the matrix $X$ becomes:

$$X = \begin{pmatrix} 0.314494 & -0.283675 \\\\\\ 1 & 1 \end{pmatrix}.$$

### Solving the system

Applying the results from before the system is:

$$\begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k} \end{pmatrix} = z\_{0}^{1}\, 0.796618^{t} \begin{pmatrix} 0.314494 \\\\\\ 1 \end{pmatrix} + z\_{0}^{2}\, 1.39479 \begin{pmatrix} -0.283675 \\\\\\ 1 \end{pmatrix}.$$

Since $\lambda\_{2} > 1$ we must set the value $z\_{0}^{2} = 0$ to avoid explosive behaviour.
Consequently:

$$\begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k} \end{pmatrix} = z\_{0}^{1}\, 0.796618^{t} \begin{pmatrix} 0.314494 \\\\\\ 1 \end{pmatrix}.$$

To solve the system of equations, first set $t=0$ and focus on $k\_t - \bar{k}.$

$$\underbrace{k\_{0}}\_{=1} - \underbrace{\bar{k}}\_{=1.65202} =  z\_{0}^{1} \times 1= -0.652017.$$

Hence, capital dynamics are governed by

$k\_{t} - \bar{k} = -0.652017 \times 0.796618^{t}$

The law of motion of consumption becomes

$c\_{t} - \bar{c} = -0.652017 \times 0.314494 \times 0.796618^{t} = -0.205055 \times 0.786618^{t}.$

Finally, we solve for the initial level of consumption compatible with the saddle path.
For $t=0$ we have:

$c\_{0} - \underbrace{\bar{c}}\_{=0.997329} = \underbrace{z\_{0}^{1}}\_{= -0.652017} \times 0.314494 \implies c\_{0} = 0.792273.$
