---
title: Additional material -  trajectory
linktitle: Trajectory
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  Ramsey:
    parent: The Ramsey model
    weight: 6

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6
---

## The trajectory around the steady state

For the moment, we have established that the model converges towards a unique steady state following a saddle path.
**Note:** This means that there is only one combination of initial capital and consumption, $(k\_{0}, c\_{0})$, such that the economy converges towards it.
Any other initial value consumption at $t=0$ (capital is pre-determined and thus we _cannot_ change it) has a diverging trajectory.

We now compute the exact behaviour of $(k\_{t}, c\_{t})$ around the steady state.

The model is highly non-linear, so we study a simpler linearised version around the steady state.
First, let's approximate the dynamics of capital and consumption [around the steady state.]({{< ref "../math_app/Steady_State.md#Approximation" >}})

### The approximation around the steady state

The behaviour of the dynamical system around the steady state can be approximated using a first-order Taylor expansion around it.
In that sense:

$$\begin{pmatrix}
c\_{t+1} - \bar{c} \\\\\\ k\_{t+1} - \bar{k}
\end{pmatrix}
\approx
\bar{A}
\begin{pmatrix}
c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k}
\end{pmatrix}.$$

Next, we solve this equation of difference equations, this is, we obtain $c\_t = \mathcal{C}(c\_0, k\_0, t), k\_t = \mathcal{K}(c\_0, k\_0, t).$

### Diagonalising the matrix: eigenvalues and eigenvectors

**Note:** based on the notes by [Benjamin Moll](http://www.princeton.edu/~moll/ECO503Web/Lecture4_ECO503.pdf).

To simplify the notation, let $y\_{t} = \begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} -\bar{k} \end{pmatrix}.$
Hence, our problem becomes:
$$y\_{t+1} = \bar{A} y\_{t}.$$

It $\bar{A}$ were a diagonal matrix, the solution to the system would be straightforward.
In fact, if that were the case it would have been (I change variables to avoid confusion):

$$\begin{pmatrix} \phi\_{t+1} \\\\ \omega\_{t+1} \end{pmatrix} = \begin{pmatrix} a\_{1,1} & 0 \\\\\\ 0 & a\_{2,2} \end{pmatrix} \begin{pmatrix} \phi\_{t} \\\\\\ \omega\_{t} \end{pmatrix}.$$
So, it is clear that $\phi\_{t+1} = a\_{1,1} \phi\_{t} \implies \phi\_{t} = a\_{1,1}^{t} \phi\_{0}$ and we would find a similar expression for $\omega.$

$\bar{A}$ is not diagonal, but we can apply a spectral decomposition and obtain an equivalent system governed by a diagonal matrix.
In particular, we are looking for an $2 \times 2$ invertible matrix $X$ such that $ X^{-1} \bar{A} X = `Lambda$, where $\Lambda$ is diagonal.
We will then apply the following transformation to our system (pre-multiplying by $\color{red}{X^{-1}}$ on both sides and multiplying by $\color{green}{XX^{-1}}$ on the right-hand side).
$$ \color{red}{X^{-1}} y\_{t+1} = \color{red}{X^{-1}} \bar{A} \color{green}{(X X^{-1})} y\_{t} = X^{-1} \bar{A} X (X^{-1} y\_{t}) =$$
$$ = \Lambda X^{-1} y\_{t}.$$

Denote $z \equiv X^{-1} y$.
Thus, the system becomes:

$$z\_{t+1} = \Lambda z\_{t}.$$
Since $\Lambda$ is diagonal, the solutions are of the form:
$$z\_{t} = \Lambda^{t} z\_{0}.$$
**Note:** in general, the power of a matrix is complex.
However, for a _diagonal matrix_ it is simply the power of each component.

Once we have the solution for the transformed system we must undo the transformation: in fact, we do not care about the evolution of $z$.
This step involves using that $X^{-1} y = z \implies y = X z$.

#### The matrix $\Lambda$

In a spectral decomposition, the diagonal matrix $\Lambda$ consists of the matrix whose entries are its eigenvalues.
Thus (we have a $2 \times 2$ system),
$$\Lambda = \begin{pmatrix} 
	\lambda\_{1} & 0  \\\\\\
	0 & \lambda\_{2} 
\end{pmatrix}.$$

#### The matrix $X$

The matrix $X$ has as columns the eigenvectors of $\bar{A}.$
There is one eigenvector associated with each eigenvalue.
**Note:** it is important to correctly relate each eigenvector to its eigenvalue.

To find an eigenvector associated with $\lambda\_{1}$ (_there are infinitely many possible eigenvectors, we only want one_) we solve the following system:

$$\bar{A} \begin{pmatrix} v\_{1} \\\\\\ v\_{2} \end{pmatrix} = \lambda\_{1} \begin{pmatrix} v\_{1} \\\\\\ v\_{2} \end{pmatrix} \quad \mathrm{or} \quad (\bar{A} - \lambda\_{1} \mathbb{I}) 
\begin{pmatrix} v\_{1} \\\\\\ v\_{2} \end{pmatrix} = \begin{pmatrix} 0 \\\\\\ 0 \end{pmatrix}.$$

The matrix $X$ then becomes:

$$X = \begin{pmatrix} v\_{1,1} & v\_{2,1} \\\\\\ 1 & 1 \end{pmatrix}.$$

### Solving the system

We begin with the solution for the transformed variable $z.$
We already know it takes the form:

$$z\_{t} = \Lambda^{t} z\_{0} \quad \mathrm{or} \quad \begin{pmatrix} z\_{t}^{1} \\\\\\ z\_{t}^{2} \end{pmatrix} = \begin{pmatrix} \lambda\_{1}^{t} & 0 \\\\\\ 0 & \lambda\_{2}^{t} \end{pmatrix} \begin{pmatrix} v\_{0}^{1} \\\\\\ v\_{0}^{2} \end{pmatrix}.$$

Next, we reverse the transformation, this is, we obtain the dynamics of $y: y\_{t} = X z\_{t}.$
Therefore, we obtain:

$$y\_{t} = X z\_{t} = X \Lambda^{t} z\_{0} = \begin{pmatrix} v\_{1,1} & v\_{2,1} \\\\\\ v\_{1,2} & v\_{2,2} \end{pmatrix} \begin{pmatrix} \lambda\_{1}^{t} & 0 \\\\\\ 0 & \lambda\_{2}^{t} \end{pmatrix} \begin{pmatrix} z\_{0}^{1} \\\\\\ z\_{0}^{2} \end{pmatrix}.$$

Alternatively, multiplying the matrices and recalling that $y\_{t}=\begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k} \end{pmatrix}$ :

$$\begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k} \end{pmatrix} = z\_{0}^{1} \lambda\_{1}^{t} \begin{pmatrix} v\_{1,1} \\\\\\ v\_{1,2} \end{pmatrix} + z\_{0}^{2} \lambda\_{2}^{t} \begin{pmatrix} v\_{2,1} \\\\\\ v\_{2,2} \end{pmatrix}.$$

The eigenvalues appear clearly in the solution.
**Remember** that we know that one eigenvalue is bigger than one, while the second lies within the unit circle.
Without loss of generality, assume that $\lambda\_{1} \in (-1,1)$ and $\lambda\_{2} > 1.$
According to the solution before, this implies an explosive behaviour: $\lambda\_{2} > 1 \implies \lim\_{t \rightarrow +\infty} \lambda\_{2}^{t} = +\infty.$
To have well-behaved dynamics we must impose $z\_{0}^{2} = 0$, which eliminates explosive behaviour.


After imposing $z\_{0}^{2} = 0$ the system becomes:

$$\begin{pmatrix} c\_{t} - \bar{c} \\\\\\ k\_{t} - \bar{k} \end{pmatrix} = z\_{0}^{1} \lambda\_{1}^{t} \begin{pmatrix} v\_{1,1} \\\\\\ v\_{1,2} \end{pmatrix}.$$

#### Closing the model with initial values

We know that the economy begins with a level of capital $k\_{t=0} = k\_{0} > 0.$
Substituting $t=0$ in the equation above, and focusing on capital, we obtain:

$$k\_{0} - \bar{k} = z\_{0}^{1} v\_{1,2} \implies \color{red}{z\_{0}^{1} = \frac{k\_{0} - \bar{k}}{v\_{1,2}}}.$$
Therefore, we can substitute the value for $z\_{0}^{1}$ to obtain the dynamics of capital:

$$k\_{t} - \bar{k} = \color{red}{z\_{0}^{1}} \lambda\_{1}^{t} v\_{1,2} = \left(k\_{0} - \bar{k} \right) \lambda^{t}.$$

Similarly,for consumption we have:

$$c\_{t} - \bar{c} = \color{red}{z\_{0}^{1}} \lambda\_{1}^{t} v\_{1,1} = \frac{v\_{1,1}}{v\_{1,2}} \lambda\_{1}^{t} (k\_{0} - \bar{k}).$$
Finally, the initial value of consumption $c\_{0}$ that puts the economy in the saddle path is obtained by setting $t=0$ in the previous equation:

$$c\_{0} - \bar{c} = \frac{v\_{1,1}}{v\_{1,2}} (k\_{0} - \bar{k}).$$
