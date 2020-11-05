---
title: Intertemporal equilibrium
linktitle: Intertemporal equilibrium
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

At the equilibrium, factors are paid their marginal productivity, thus:

$$r\_{t} = f^{\prime}(k\_{t})$$
<center>and</center>

$$w\_{t} = f(k\_{t}) - f^{\prime}(k\_{t})k\_{t}.$$

## Definition of intertemporal equilibrium

An intertemporal equilibrium with perfect foresight is **a sequence** $(k\_{t}, c\_{t}) \in \mathbb{R}\_{++}^{2}, t=0,\ldots,+\infty$, such that given $k\_{0} > 0$, **households and firms optimise**, **markets clear**, and **capital accumulation follows** $k\_{t+1} = f(k\_{t}) + (1-\delta)k\_{t} -c\_{t}.$
Thus, all the following equations must be satisfied:

$$\left.
\begin{eqnarray}
u^{\prime}(c\_{t}) = \beta (r\_{t+1} + 1 - \delta) u^{\prime}(c\_{t+1}) \\\\\\
k\_{t+1} = f(k\_{t}) + (1-\delta)k\_{t} - c\_{t} \\\\\\
w\_{t} = f(k\_{t}) - f^{\prime}(k\_{t})k\_{t} \\\\\\
r\_{t} = f^{\prime}(k\_{t}) \\\\\\
\lim\_{t \rightarrow \infty} \beta^{t}u^{\prime}(c\_{t})k\_{t+1} = 0
\end{eqnarray} 
\right\\} \tag{8, Equilibrium} \label{eq:equilibrium}$$

The first equation in \ref{eq:equilibrium} is the Euler equation, which implies that households optimise.
The second equation is the law of motion for capital: capital next period equals production net of consumption plus the remaining capital that has not depreciated.
The third and fourth equations ensure that capital and labour markets clear.
Finally, the transversality condition allows us to pick a non-explosive path.

After some substitutions, we can express the intertemporal equilibrium ---forgetting for a moment about the transversality condition--- as:

$$\left.
\begin{eqnarray}
& u^{\prime}(c\_{t}) = \beta (f^{\prime}(k\_{t+1}) + 1 - \delta) u^{\prime}(c\_{t+1}) \\\\\\
& k\_{t+1} = f(k) + (1-\delta)k\_{t} - c\_{t}.
\end{eqnarray}
\right\\} \tag{8.1, Equilibrium} \label{eq:equilibrium2}$$

\ref{eq:equilibrium2} is a two-dimensional dynamic system with a unique predetermined state variable: $k\_{t}.$
To analyse it, we first compute its steady state and then check the dynamics.


