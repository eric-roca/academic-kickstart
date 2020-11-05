---
title: The transversality condition
linktitle: The transversality condition
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  math_app:
    parent: Appendix
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

The transversality condition appears as a necessary condition to determine the optimal path in dynamic models.
It complements the Euler equation and allows to pinpoint the exact optimal path (see example below).

We use the transversality condition to avoid explosive consumption or saving paths that would end up in:

* Excessive consumption, driving the capital stock of the economy to zero and impeding future consumption,
* Excessive savings, up to the point that a large amount of the output is devoted to replace capital that depreciates.

---

Indeed, using only the Euler equation alongside with initial conditions allows for infinitely many optimal paths to be found.
The Ramsey problem does not state any final value for capital $k\_{t=T}$ (in fact, it does not even state a final period $T$ because $T \rightarrow \infty).$
Therefore, working only with the Euler equation and the initial stock of capital $k\_{t=0} = k\_{0}$ allows for infinitely optimal paths. 
In the following example, we try to solve the simple cake-eating problem without imposing the transversality condition, and obtain infinitely many solutions.

## Example: Cake-eating problem

We try to maximise utility from eating a finite cake over an infinite amount of time.
The size of the cake ($k$) is given: $k\_{t=0} = k\_0 \ > 0.$
The problem reads:

$$\begin{eqnarray}
\max & \sum\_{t=0}^{\infty} \beta^{t} \ln ( c\_{t} ) \\\\\\
& k\_{t+1}  = k\_{t} - c\_{t} \\\\\\
& k\_{t=0} = k\_{0}
\end{eqnarray}$$

We solve it noting that we can decide on $c\_{t}$ and $k\_{t}.$
The Lagrangian is:
$$\mathcal{L} = \sum\_{t=0}^{\infty} \beta^{t} \ln (c\_{t}) + \sum\_{t=0}^{\infty} \lambda\_{t} (k\_{t+1} - k\_{t} + c\_{t}).$$
Taking derivatives with respect to $c\_{t}$ and $k\_{t}$, and noticing that $k\_{t}$ appears together with the $\lambda\_{t-1}$ term gives us the Euler equation:
$$c\_{t+1} = \beta c\_{t}.$$
Hence, iterating, $c\_{t} = \beta^{t}c\_{0}$<br/>
Plugging it in the constraint gives us: $k\_{t+1} = k\_{t} - \beta^{t}c\_{0}.$<br/>
Solving for $k\_{t}$ gives us $k\_{t} = D - \frac{c\_{0}(1-\beta^{t})}{1-\beta}.$
At this point, we can no longer proceed (we have the unknown $D$) unless we have the extra restriction given by the transversality condition.
If we use it, which reads, $\lim\_{t \rightarrow \infty} \beta^{t} u^{\prime} (c\_{t})k\_{t+1}=0$ we can substitute $c\_{t} = \beta^{t} c\_{0}$.
Therefore: $\lim\_{t \rightarrow \infty} \beta^{t} \frac{1}{c\_{t} k\_{t+1}} = \lim\_{t \rightarrow \infty} \beta^{t} \frac{1}{\beta^{t} c\_{0}} k\_{t+1} = \lim\_{t \rightarrow \infty} k\_{t+1} = 0.$
So, at the limit, the size of the cake becomes zero, and we eat it completely.<br/>
**Note:** This makes sense, because utility is increasing in consumption and leaving something behind would be a waste of resources.

Now, with this additional information ($\lim\_{t \rightarrow \infty} k\_{t+1} = 0$) we can close the problem using:
$k\_{t+1} = D - \frac{c\_{0}(1-\beta^{t-1})}{1-\beta}$.
Hence $\lim\_{t \rightarrow \infty} k\_{t+1} = \lim\_{t \rightarrow \infty} D - \frac{c\_{0}(1-\beta^{t-1})}{1-\beta} = D - \frac{c\_{0}}{1-\beta} = 0.$
Therefore, $D = \frac{c\_{0}}{1-\beta}$ which implies that $k\_{t} = \frac{c\_{0}\beta^{t}}{1-\beta}$.
Since $k\_{t=0} = k\_{0}$ we can easily obtain $c\_{0}$ from: $k\_{0} = \frac{c\_{0}}{1-\beta} \implies c\_{0} = (1-\beta)k\_{0}.$

Finally, we have that $c\_{t} = \beta^{t} c\_{0} = \beta^{t}(1-\beta)k\_{0}.$

**Note:** This problem is more easily solved assuming since the beginning that the entire cake will be consumed.
This is, $\sum\_{t=0}^{\infty} c\_{t} = k\_{0}$.
In that case, the Lagrangian is: $\mathcal{L} = \sum\_{t=0}^{\infty} \beta^{t} \ln (c\_{t}) + \lambda (\sum\_{t=0}^{\infty} c\_{t} - k\_{0}).$
Notice that in this case we have only one $\lambda$.
It is simple to show that $c\_{t} = \beta c\_{t-1}.$
Substituting this information in the constraint gives us $k\_{0} = \sum\_{t=0}^{\infty} \beta^{t} c\_{0} = \frac{c\_{0}}{1-\beta}.$
Therefore, $c\_{t} = \beta^t (1-\beta)k\_{0}.$
There is one important remark regarding this alternative method.
It _indirectly_ uses the transversality condition.
Remember that we obtained that $\lim\_{t \rightarrow \infty} k\_{t+1} = 0$ which implies that the entire cake is consumed.
In the alternative method we assumed it, which makes sense just by looking at the utility formulation.


## A **wrong** proof of the transversality condition

In some cases the transversality constraint is justified as the limit when time goes to infinity of an equivalent problem with a finite horizon.
This is, one can write an optimal program that ends at some specific period.
For instance, our Ramsey problem with a terminal state can be written as:
$$\max\_{c\_{t}, k\_{t+1}} \sum\_{t=0}^{T} \beta^{t} u(c\_{t}).$$

We impose that capital must be positive all periods: $k\_{t+1} \geq 0.$
Write the Lagrangian that corresponds to the Kuhn-Tucker problem:

$$\mathcal{L} = \sum\_{t=0}^{T} \beta^{t} u(c\_{t}) + \sum\_{t=0}^{T} \lambda\_{t}(w\_{t} + r\_{t} k\_{t} + (1-\delta)k\_{t} - c\_{t} - k\_{t+1}) + \sum\_{t=0}^{T} \mu\_{t}k\_{t+1}.$$

Taking the appropriate derivatives with respect to $k\_{t+1}, c\_{t}$ and remembering the complementary slackness condition leaves us with the following system of equations, which we evaluate at $t=T.$
$$\begin{eqnarray}
\beta^{T} u^{\prime}(c\_{T}) & = \lambda\_{T} \\\\\\
\lambda\_{T} & = \mu\_{T} \\\\\\
\mu\_{T} k\_{T+1} & = 0.
\end{eqnarray}$$ 

Rearranging we can get:
$$\begin{equation}
\beta^{T} u^{\prime} (c\_{T}) k\_{T+1} = 0.
\end{equation}$$

The equation above indicates that one of either two possibilities must be true:

* $\beta^{T} u^{\prime} (c\_{T}) >0$ which requires $k\_{T+1} = 0,$
* $\beta^{T} u^{\prime} (c\_{T}) = 0$ and $k\_{T+1} \geq 0.$

The first case indicates that we leave the world at time $T$ with zero capital.
This makes sense because the optimisation does not go beyond $T$, and leaving resources unconsumed is not efficient: after all, we _eat_ capital.
So we eat everything before dying.
The second case never arises: the marginal utility is zero only when consumption is infinite.

Letting time go to infinity, the equation above becomes the transversality condition:
$$\lim\_{t \rightarrow \infty} \beta^{t}u^{\prime}(c\_{t})k\_{t+1} = 0.$$

## The transversality condition is a necessary condition: proof

Proof by Kamihigashi (2002): [A Simple Proof of the Necessity of the Transversality Condition](https://www.jstor.org/stable/25055538?seq=1#page_scan_tab_contents)
 
Kamihigashi (2002) shows that the transversality condition is a necessary condition in an optimal control problem.
This proof neglects consumption and focuses on current and future values of $x\_{t}.$
Consider the following maximisation problem:

$$
\max\_{ \\{x\_{t} \\}\_{t=0}^{\infty} }  \sum\_{t=0}^{\infty} v\_{t}(x\_{t}, x\_{t+1}) \\\\\\
 x\_{0} = \bar{x\_{0}}, \forall t \in \mathbb{Z}\_{+}, (x\_{t}, x\_{t+1}) \in X\_{t}.
$$

We assume the following:

1.  $x\_{t} \in X \subset \mathbb{R}\_{+}^{m}$, basically, $x\_{t} \geq 0,$
2.  $X\_{t}$ is convex, $(0,0) \in X\_{t},$
3.  $U: Gr(\Gamma) \rightarrow \mathbb{R}$ is $\mathcal{C}^{1}$ and concave,
4.  $\forall (x,y) \in Gr(\Gamma), U\_{y}(x,y) \leq 0,$
5.  For any feasible path $\{x\_{t}\}, \sum\_{t=0}^{\infty} v\_{t}(x\_{t}, x\_{t+1}) \equiv \lim\_{T \rightarrow \infty} \sum\_{t=0}^{T} v\_{t}(x\_{t}, x\_{t+1})$ exists in $(-\infty, \infty).$

First, define an optimal path $\\{x\_{t}^{\star}\\}$ as a feasible path such that:
$$\sum\_{t=0}^{\infty} v\_{t}(x\_{t}, x\_{t+1}) \leq \sum\_{t=0}^{\infty} v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star}).$$

The proof only involves using an argument derived from concavity.
$$\forall \gamma \in [0,1), \forall \lambda \in [\gamma, 1), \frac{f(1)-f(\lambda)}{1-\lambda} \leq \frac{f(1)-f(\gamma)}{1-\gamma}.$$

Suppose we deviate $\lambda \in [0,1)$ from the optimal path $\{x\_{t}^{\star}\}$ and follow a path that is feasible:

**Lemma 1**
$$\{x\_{0}^{\star}, x\_{1}^{\star}, \ldots, x\_{T}^{\star}, \lambda x\_{T+1}^{\star}, \lambda x\_{T+2}^{\star}, \ldots \}.$$

Again, we are assuming that by taking $\lambda \in [0,1)$ this alternative path is feasible.
By optimality we have:
$$v\_{T}(x\_{T}^{\star}, \lambda x\_{T+1}^{\star}) - v\_{T}(x\_{T}^{\star}, x\_{T+1}^{\star}) + \sum\_{t=T+1}^{\infty}[v\_{t}(\lambda x\_{t}^{\star}, \lambda x\_{t+1}^{\star}) - v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star})] \leq 0.$$
This condition essentially says that deviating from the optimal path reports less utility than following it.

Divide through by $(1-\lambda)$ and obtain:


$$\frac{v\_{T}(x\_{T}^{\star}, \lambda x\_{T+1}^{\star}) - v\_{T}(x\_{T}^{\star}, x\_{T+1}^{\star})}{1-\lambda} \leq \sum\_{t=T+1}^{\infty} \frac{v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star}) - v\_{t}(\lambda x\_{t}^{\star}, \lambda x\_{t+1}^{\star})}{1-\lambda} \leq \sum\_{t=T+1}^{\infty} [v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star}) - v\_{t}(0,0)].$$

The last inequality follows because of Lemma 1 and because $v$ is concave, setting $\gamma = 0$.
Now take the $\lim\_{\lambda \rightarrow 1}$ on the right-hand side to obtain:

$$0 \leq -v\_{T,2}(x\_{T}^{\star}, x\_{T+1}^{\star}x\_{T+1)}^{\star} \leq \sum\_{t=T+1}^{\infty} [v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star}) - v\_{t}(0,0)].$$

The first inequality follows from Assumption 4 and a rewrite of derivative definition: $f^{\prime}(x) = \lim\_{\eta \rightarrow 0} \frac{f(\eta x) - f(x)}{x - \eta x}.$

Finally, take $\lim\_{T \rightarrow \infty}$, which yields:

$$0 \leq \lim\_{T \rightarrow \infty}[-v\_{T,2}(x\_{T}^{\star}, x\_{T+1}^{\star}] \leq \lim\_{T \rightarrow \infty} \sum\_{t=T+1}^{\infty}[v\_{t}(x\_{t}^{\star}, x\_{t+1}^{\star}) - v\_{t}(0,0)] = 0,$$

where the equality holds by Assumption 5.
We have obtained the transversality condition.

https://link.springer.com/referenceworkentry/10.1007%2F978-1-4471-5102-9_200-1 
https://www.encyclopediaofmath.org/index.php/Pontryagin_maximum_principle
http://web.sgh.waw.pl/~mbrzez/Adv_Macro/2_Ramsey_model.pdf
http://cyber.sci-hub.tw/MTAuMTAwNy9zMDAxOTkwMTAwMTk4/10.1007%40s001990100198.pdf
https://economics.mit.edu/files/8336
http://www.econ2.jhu.edu/people/ccarroll/Public/LectureNotes/Growth/HamiltonianVSDiscrete.pdf
https://eml.berkeley.edu/~webfac/obstfeld/e202a_f13/lecture2.pdf
http://www.princeton.edu/~moll/ECO503Web/Lecture2_ECO503.pdf
https://dl1.cuni.cz/pluginfile.php/97847/mod_resource/content/0/Lecture_3.pdf
