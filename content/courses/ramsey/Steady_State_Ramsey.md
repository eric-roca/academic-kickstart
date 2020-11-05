---
title: Steady state
linktitle: Steady state
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 4 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4 
---

## Steady states

A steady state of an N-dimensional dynamic system is a configuration of the system variables such that the system remains unchanged over time.
This is, upon reaching a steady state, the system remains there forever.
Hence, if the system is given by:

$$\left.
\begin{eqnarray}
x^{1}\_{t+1} & = f\_{1}(x^{1}\_{t}, \ldots, x^{N}\_{t}) \\\\\\
\vdots & \\\\\\
x^{N}\_{t+1} & = f\_{N}(x^{1}\_{t}, \ldots, x^{N}\_{t})
\end{eqnarray}
\right\\}$$

in a steady state we have that

$$\left.
\begin{eqnarray}
x^{1}\_{t+1} & = x^{1}\_{t} \\\\\\
\vdots & \\\\\\
x^{N}\_{t+1} & = x^{N}\_{t}.
\end{eqnarray}
\right\\}$$

In many cases, a steady state is only reached at the limit when $t \rightarrow +\infty,$ unless we intentionally start the dynamics exactly at the steady state.
Moreover, the steady state is often approached asymptotically: it is never fully reached, but we get infinitesimally close to it.
Finally, steady states can be (asymptotically) stable or unstable.
In the first sort, variables approach the steady-state level.
In the second, the system _diverges_ from the steady state.

---
## The steady state in the Ramsey model

In our case, denote by $(\bar{k}, \bar{c}) \in \mathbb{R}\_{+}^{2}$ the capital and consumption levels at the steady state.
Then, a steady-state solution satisfies the following system of equations:

$$\left.
\begin{eqnarray}
u^{\prime}(\bar{c}) & = \beta (f^{\prime}(\bar{k}) + 1 -\delta) u^{\prime}(\bar{c}), \\\\\\
\bar{k} & = f(\bar{k}) + (1-\delta) \bar{k} - \bar{c}.
\end{eqnarray}
\right\\} \tag{9, Steady St.} \label{eq:ss}$$

Simplifying we can obtain the following, equivalent expression:

$$\left.
\begin{eqnarray}
f^{\prime}(\bar{k})  = \frac{\theta}{\beta}, \\\\\\
\bar{c}  = f(\bar{k}) - \delta \bar{k},
\end{eqnarray}
\right\\} \tag{9.1, Steady St.} \label{eq:ss2}$$

where $\theta \equiv 1 - \beta(1-\delta) \in (0,1).$

### Existence of the steady state

From the Inada conditions for the production (Assumption R3.6) function we have that

$$0 = \lim\_{k \rightarrow +\infty} f^{\prime}(k) < \frac{\theta}{\beta} < \lim\_{k \rightarrow 0}f^{\prime}(k) = +\infty.$$

Hence, $f^\prime (k)$ takes values on the interval $(0, +\infty).$
Since the function $f^\prime$ is continuous, by the intermediate value theorem there exists at least one $k=\bar{k}$ such that $f^\prime{\bar{k}} = \frac{\theta}{\beta}.$

Moreover, from Assumption R3.4 the function $f^\prime (k)$ is monotonically decreasing.
Therefore, there exists one and only one value $\bar{k} \in (0,+\infty)$ that solves the first equation in \ref{eq:ss2}.
Also, the second equation in \ref{eq:ss2} uniquely determines the level of consumption given capital.
Hence, the steady-state consumption level $\bar{c}$ is unique.

We can obtain an overview of the dynamics of the model using the [phase diagram]({{< ref "Phase_Diagram.md" >}}) and derive the exact solution using the method outlined in [trajectory]({{< ref "Ramsey_Trajectory.md" >}}).

### Stability of the steady state {#stability}

We are now interested in determining the behaviour of the economy when it starts with some level of capital $k\_0$ and consumption $c\_0.$
The economy is represented by a $2 \times 2$ system of first-order difference equations.
The stability of a steady state depends on the Jacobian matrix's eigenvalues evaluated at the steady state.
**Note:** the [Appendix]({{< ref "../math_app/Steady_State.md" >}}) discusses this in more detail.
In particular, we wonder whether the dynamics are such that they converge towards the steady state or diverge away from it.

The equations that govern the economy are the Euler equation and the law for capital accumulation:

$$\left.
\begin{eqnarray}
u^{\prime}(c\_{t}) = \beta (f^{\prime}(k\_{t+1}) + 1 - \delta) u^{\prime}(c\_{t+1}), \\\\\\
k\_{t+1} = f(k\_{t}) + (1-\delta) k\_{t} - c\_{t}
\end{eqnarray}
\right\\}. \tag{8.1 Equilibrium}
$$

The stability of the steady state first requires computing the Jacobian matrix.
The Jacobian matrix associated to the system is:

$$\bar{A} = \begin{pmatrix}
\frac{\partial c\_{t+1}}{\partial c\_{t}} & \frac{\partial c\_{t+1}}{\partial k\_{t}} \\\\\\
\frac{\partial k\_{t+1}}{\partial c\_{t}} & \frac{\partial k\_{t+1}}{\partial k\_{t}}
\end{pmatrix}.$$

Notice that $\bar{A}$ represents the approximate linear behaviour of the economy at any given point: $\begin{pmatrix}c\_{t+1} \\\\\\ k\_{t+1}\end{pmatrix} \approx \begin{pmatrix} c\_0 \\\\\\ k\_0 \end{pmatrix} + \bar{A} \begin{pmatrix} c\_t - c\_0 \\\\\\ k\_t - k\_0 \end{pmatrix}.$

In our case, the Jacobian matrix reads:

$$\bar{A} = \begin{pmatrix}
\frac{u^{\prime \prime}(c\_{t})+\beta f^{\prime \prime}(k\_{t+1})u^{\prime}(c\_{t+1})}{\beta \left[ f^{\prime}(k\_{t+1}) + 1 - \delta \right] u^{\prime \prime}(c\_{t+1})} & -\frac{\beta f^{\prime \prime}(k\_{t+1}) \left[ f^{\prime}(k\_{t}) + 1 - \delta \right] u^{\prime}(c\_{t+1})}{\beta \left[ f^{\prime}(k\_{t+1}) + 1 - \delta \right] u^{\prime \prime}(c\_{t+1})} \\\\\\
-1 & f^{\prime}(k\_{t}) + 1 - \delta
\end{pmatrix}. \tag{10, Jacobian} \label{eq:jacobian}$$

Then, we evaluate \ref{eq:jacobian} at the steady state.
In particular, we use \ref{eq:ss} characterising the steady state.

$$\color{red}{k\_{t+1} = k\_{t} = \bar{k},} $$
$$\color{green}{c\_{t+1} = c\_{t} = \bar{c},} $$
$$\color{blue}{1 = \beta \left( f^{\prime}(\bar{k}) + 1 - \delta \right).}  $$

Substituting all $t$ and $t+1$ variables for their steady-state values $\bar{k}$ and $\bar{c}$ yields:

$$\bar{A}\bigr\rvert\_{\substack{
	k\_{t} = k\_{t+1} = \bar{k} \\\\\\
	 c\_{t} = c\_{t+1} = \bar{c}
}
}
   = \begin{pmatrix}
\frac{
	u^{\prime \prime}(\textcolor{green}{\bar{c}})+\beta f^{\prime \prime}(\textcolor{red}{\bar{k}})u^{\prime}(\textcolor{green}{\bar{c})}
}
{
\beta \left[ f^{\prime}(\textcolor{red}{\bar{k}}) + 1 - \delta \right] u^{\prime \prime}(\bar{\textcolor{green}{c}})
}
&
 -\frac{
\beta f^{\prime \prime}(\bar{k}) \left[ f^{\prime}(\bar{k}) + 1 - \delta \right] u^{\prime}(\bar{\textcolor{green}{c}})
}
{
\beta \left[ f^{\prime}(\bar{k}) + 1 - \delta \right] u^{\prime \prime}(\bar{\textcolor{green}{c}})}
\\\\\\
-1
& 
f^{\prime}(\textcolor{red}{\bar{k}}) + 1 - \delta
\end{pmatrix} = $$

$$\begin{pmatrix}
\frac{
	u^{\prime \prime}(\bar{c})+\beta f^{\prime \prime}(\bar{k})u^{\prime}(\bar{c)}
}
{
\textcolor{blue}{\beta \left[ f^{\prime}(\bar{k}) + 1 - \delta \right]} u^{\prime \prime}(\bar{c})
}
&
 -\frac{
\textcolor{blue}{\beta} f^{\prime \prime}(\bar{k}) \textcolor{blue}{\left[ f^{\prime}(\bar{k}) + 1 - \delta \right]} u^{\prime}(\bar{c})
}
{
\textcolor{blue}{\beta \left[ f^{\prime}(\bar{k}) + 1 - \delta \right]} u^{\prime \prime}(\bar{c})}
\\\\\\
-1
& 
\color{blue}{f^{\prime}(\bar{k}) + 1 - \delta}
\end{pmatrix} = $$


$$\begin{pmatrix}
\frac{
	u^{\prime \prime}(\bar{c})+\beta f^{\prime \prime}(\bar{k})u^{\prime}(\bar{c)}
}
{
u^{\prime \prime}(\bar{c})
}
&
 -\frac{
f^{\prime \prime}(\bar{k}) u^{\prime}(\bar{c})
}
{
u^{\prime \prime}(\bar{c})}
\\\\\\
-1
& 
\frac{1}{\beta}
\end{pmatrix} = $$


$$\begin{pmatrix}
	1 - \beta f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}}
&
f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}}
\\\\\\
-1
& 
\frac{1}{\beta}
\end{pmatrix}, $$

where $\epsilon\_{c} = - \frac{u^{\prime \prime}( c )}{u^{\prime}( c )} c$ represents the degree of relative risk aversion.

**Technical note on steady states**
A steady state can be:

* Source: starting from any point, trajectories diverge away from it,
* Sink: starting from any point, trajectories converge towards it,
* Saddle: a unique combination of initial points presents a converging trajectory (saddle path), all other initial conditions imply an diverging trajectory.

As mentioned before, the stability of a steady state depends on the eigenvalues of $\bar{A}$ (eigenvalues are the roots of the characteristic equation).
Typically, we are only interested in some properties of the eigenvalues.

**Blanchard-Kahn** characterises the types of steady states in terms of their eigenvalues.
Denote by $l$ the number of eigenvalues in the unit circle, and denote by $m$ the number of pre-determined state variables:

* if $l=m$ (standard case): saddle-path, _unique_ optimal trajectory. The eigenvalues within the unit circle govern the speed of convergence.
* if $l \lt m$: unstable
* if $l \gt m$: multiple optimal trajectories.

We can use different techniques to determine whether the eigenvalues lay in the interval $(-1,1).$

#### Direct computation of the eigenvalues

The first method we present uses the definition of eigenvalue: the roots of the characteristic equation.
It requires solving:

$$\begin{vmatrix}
	1-\beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} - \lambda & f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}} \\\\\\
	-1 & \frac{1}{\beta} - \lambda
\end{vmatrix} = 
\lambda^{2} + \lambda \left( \beta f^{\prime \prime} (\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}} - 1 - \frac{1}{\beta} \right) + \frac{1}{\beta} = 0.$$

The roots of this equation are:


$$\lambda\_{1} = \frac{\overbrace{1+\overbrace{\frac{1}{\beta}}^{>1} - \overbrace{\beta f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}}}^{<0} + \sqrt{\left( 1+\frac{1}{\beta} - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} \right)^2 - \frac{4}{\beta}}}^{>2}}{2} > 1 .$$

For $\lambda\_{2}$ we have:

$$\lambda\_{2} = \frac{1+\frac{1}{\beta} - \beta f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}} - \sqrt{\left( 1+\frac{1}{\beta} - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} \right)^2 - \frac{4}{\beta}}}{2} > 0$$

To simplify notation, let $\phi \equiv 1+\frac{1}{\beta} - \beta f^{\prime \prime}(\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}}$ and $\kappa \equiv \frac{4}{\beta}$.<br/>
Assume that $\lambda\_{2} > 1$, then we must have:

$$\frac{\phi - \sqrt{\phi^{2} - \kappa}}{2} > 1 \implies \kappa > 4\phi - 4.$$
Substituting:
$$4 + \frac{4}{\beta} - 4 \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} - 4 < \frac{4}{\beta} \implies -4\beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} < 0.$$
But this is impossible because $f^{\prime \prime}(\cdot) < 0.$
Hence, $\lambda\_{2} < 1$.

Summarising, the eigenvalues are such that
$$\lambda\_{1} > 1$$
<center>and</center>

$$\lambda\_{2}\in(0,1)$$

and the **steady state is a saddle.**

#### Use the intermediate value theorem

The characteristic equation associated with the Jacobian evaluated at the steady state is:

$$G(\lambda) = \lambda^{2} + \lambda \left( \beta f^{\prime \prime} (\bar{k}) \frac{\bar{c}}{\epsilon\_{\bar{c}}} - 1 - \frac{1}{\beta} \right) + \frac{1}{\beta} = 0.$$

First, notice that $G(\lambda)$ is a continuous function on $\lambda.$
We want to assess whether its roots (or at least one root) lay in the interval $(-1,1)$.
The behaviour of $G(\lambda)$ is as follows:

$$\lim\_{\lambda \rightarrow -\infty} G(\lambda) = + \infty$$
$$\lim\_{\lambda \rightarrow +\infty} G(\lambda) = + \infty$$
$$G(-1) = 2 + \frac{2}{\beta} - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} > 0$$
$$G(0) = \frac{1}{\beta} > 0 $$
$$G(1) =  \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} < 0.$$

Hence, $\exists \lambda\_{2} \in (-1,0)$ such that $G(\lambda\_{2}) = 0$.
The second root lies beyond $1.$
Therefore, $\lambda\_{1} > 1, \lambda\_{2}\in(0,1)$ and the **steady state is a saddle.**

#### Use eigenvalues' properties

For any matrix, we have the following:

* The product of eigenvalues equals the **determinant** of the matrix: $\mathrm{det}(M) = \lambda\_{1} \lambda\_{2} \ldots \lambda\_{N},$
* The sum of eigenvalues equals the **trace** of matrix: $\mathrm{tr}(M) = \lambda\_{1} + \lambda\_{2} + \ldots + \lambda\_{N}.$

In our case:

$$\lambda\_{1} \lambda\_{2} = \frac{1}{\beta} $$
$$\lambda\_{1} + \lambda\_{2} = \underbrace{1+ \frac{1}{\beta} - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}}}\_{>1}.$$

The first equation implies that either 

* a) $\lambda\_{1} > 0, \lambda\_{2} > 0$ or 
* b) $\lambda\_{1} < 0, \lambda\_{2} < 0.$ 

However, since $\lambda\_{1} + \lambda\_{2} > 1$ b) is impossible.
Therefore, $\lambda\_{1} > 0, \lambda\_{2} > 0.$

Substitute $\lambda\_{1} \lambda\_{2} = \frac{1}{\beta}$ in the second equation:

$$ \lambda\_{1} + \lambda\_{2} = 1+ \lambda\_{1} \lambda\_{2} - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}}.$$

Rearranging:
$$ \lambda\_{1} + \lambda\_{2} - \lambda\_{1} \lambda\_{2} =  1+  - \beta f^{\prime \prime}(\bar{k})\frac{\bar{c}}{\epsilon\_{\bar{c}}} > 1 \implies \lambda\_{1} + \lambda\_{2} - \lambda\_{1}\lambda\_{2} - 1 >0.$$
Factorisation leads to:
$$(1 - \lambda\_{2})(\lambda\_{1} - 1) > 0.$$
Therefore, because $\lambda\_{1},\, \lambda\_{2} > 0$ we must have

$$ \lambda\_{2} < 1 $$
$$ \lambda\_{1} > 1 $$
$$ \lambda\_{1} > 0, \lambda\_{2} > 0$$
and **the steady state is a saddle.**
