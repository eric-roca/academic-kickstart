---
title: Intertemporal equilibrium
linktitle: Intertemporal equilibrium
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 4

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4
---

## Temporary equilibrium

Before turning to the intertemporal equilibrium and the analysis of the steady state, we study the temporary equilibrium that takes place every period.

We have not discussed the firms, but they follow the same setup as in Ramsey: use capital and labour in a perfectly competitive environment.

We shall work in intensive form: $k\_{t} \equiv \frac{K\_{t}}{N\_{t}}.$

1. **Labour market equilibrium:**
	_Only_ young individuals supply labour.
	Moreover, they do so _inelastically_.
	During period $t$ there are $N\_{t}$ young agents and, hence, the supply of labour is $N\_{t}$.
	Equating this to labour demand from firms $L\_{t}$ gives the wage rate:
	$$w\_{t} = \omega\left(\frac{K\_{t}}{N\_{t}}\right)=\omega(k\_{t}).$$

2. **Capital market:**
	_Only_ old individuals own capital.
	Since firms operate competitively, they make zero profits.
	Hence, $f^{\prime}(k\_{t})K\_{t}$ is distributed as interests.
	Old households receive $N\_{t-1}R\_{t}s\_{t-1} = R\_{t}K\_{t}.$
	So, what old households receive must equal what firms distribute
	In other terms: $R\_{t}K\_{t}= f^{\prime}(k\_{t}) K\_{t}$ and $R\_t = f^\prime (k\_t).$

3. **Good market:**
	Finding the equilibrium for this market departs from the otherwise similar Ramsey case.
	Remember that we have _two_ types of agents: young and old.
	Total production is given by:
	$$Y\_{t} = F(K\_{t}, N\_{t}) = \color{red}{N\_{t}} f(k\_{t}).$$
	Total demand for goods combines the consumption of $d\_{t}$, the old generation living in period $t$,
	and the demand for consumption _and_ investment from the young: $c\_{t}, s\_{t}.$
	Therefore, counting how many old and young individuals live during period $t$ we have that total demand equals:
	$$N\_{t-1}d\_{t} + N\_{t}(c\_{t}+s\_{t}).$$
	The equilibrium on the goods market implies:
	$$Y\_{t} = N\_{t-1}d\_{t} + N\_{t}(c\_{t}+s\_{t}).$$

	Also, we can check that total production equals total consumption:
	$$N\_{t}(c\_{t}+s\_{t}) = N\_{t}w\_{t}=N\_{t}(f(k\_{t})-k\_{t}f^{\prime}(k\_{t})) = Y\_{t}-K\_{t}f^{\prime}(k\_{t}),$$
	$$N\_{t-1}d\_{t} = N\_{t-1}R\_{t}s\_{t-1} = R\_{t}K\_{t} = K\_{t}f^{\prime}(k\_{t}).$$

A temporary equilibrium is a set $\\{w\_{t}, R\_{t}, K\_{t}, L\_{t}, Y\_{t}, k\_{t}, I\_{t}, c\_{t}, s\_{t}, d\_{t}\\}$ that satisfies:

$$\begin{eqnarray}
	 w\_{t} = \omega(k\_{t}), \\\\\\
	 R\_{t} = f^{\prime}(k\_{t}), \\\\\\
	 L\_{t} = N\_{t}, \\\\\\
	 Y\_{t} = N\_{t}f(k\_{t}), \\\\\\
     Y\_{t} = N\_{t-1}d\_t + N\_{t}(c\_{t}+s\_{t}) \\\\\\
	 I\_{t} = N\_{t}s\_{t}, \\\\\\
	 c\_{t} = w\_{t} - s\_{t}, \\\\\\
	 s\_{t} = s(\omega(k\_{t}),R\_{t+1}), \\\\\\
	 d\_{t} = R\_{t}s\_{t-1}.
\end{eqnarray}$$

The existence of a temporary equilibrium is guaranteed because the functions are single-valued.

## Intertemporal equilibrium with perfect foresight

The equilibrium equation that links two consecutive periods is the capital accumulation equation.
In particular, the savings of young individuals at period $t$ are transformed into productive capital at $t+1.$

**Note:** in this model, it is useful to write the equations first in aggregate terms and then convert them to its intensive-form representation.

$$K\_{t+1} = N\_{t}s\_{t} = N\_{t} s\left( \omega(k\_{t}), R\_{t+1} \right).$$

In intensive form:

$$k\_{t+1} = \frac{K\_{t+1}}{\color{red}{N\_{t+1}}} = \frac{N\_{t}}{\color{red}{N\_{t+1}}} s\left( \omega(k\_{t}), R\_{t+1} \right) = \frac{1}{1+n}s\left( \omega(k\_{t}), R\_{t+1} \right) .$$

Finally, we can incorporate the equilibrium in the capital market (together with perfect foresight) and replace $R\_{t+1} = f^{\prime}(k\_{t+1}):$

$$k\_{t+1} =\frac{1}{1+n}s \left( \omega(k\_{t}), f^{\prime}(k\_{t+1}) \right).$$

**Intertemporal equilibrium (for perfect foresigt)**:
Given an initial capital stock $k\_{0} = K\_{0} \big{/} N\_{-1}$, an intertemporal equilibrium (for perfect foresight) is a sequence of temporary equilibria that satisfies for all $t>0$ the equation:

$$k\_{t+1} =\frac{1}{1+n}s \left( \omega(k\_{t}), f^{\prime}(k\_{t+1}) \right).$$

**Note:** _de la Croix and Michel_ discuss on pp. 20--27 the existence and uniqueness of the intertemporal equilibrium.

## Existence of an intertemporal equilibrium

The existence of at least one temporary equilibrium is guaranteed by the properties of the functions.
The proof is quite involved, though, as is presented below.
Having an intertemporal equilibrium means having a solution for $k\_{t+1}$ in the equation

$$k\_{t+1} = \frac{1}{1+n}s(\omega(k\_t), f^\prime (k\_{t+1})),$$

where $k\_t$ is predetermined at $t.$

<details>
<summary>Proof</summary>

The proof uses the following equation about savings:
$$0< s\left( w, f^\prime(k) \right) < w.$$$
In words, it indicates that individuals have positive savings, and they save _only_ part of their total income.

Next, define 
$$H(k,w) = (1+n)k - s(w, f^\prime(k))= 0.$$
Basically, here we are using the definition of an intertemporal equilibrium.
Having an intertemporal equilibrium is then equivalent to finding a $k$ satisfying the previous equation.

We use the intermediate value theorem to show that at least one solution exists.
First, we analyse the behaviour of $H(k,w)$ when $k$ tends to $+\infty.$

From $0< s\left( w, f^\prime(k) \right) < w,$ we have

$$0 < \frac{s(w, f^\prime (k))}{k} < \frac{w}{k}.$$

**Limit when $k \rightarrow +\infty$**

Keeping $w$ fixed, the limit of $\frac{w}{k}$ when $k \rightarrow +\infty$ is 0.
Then,

$$\lim\_{k \rightarrow +\infty} \frac{s(w, f^\prime (k))}{k} = 0.$$

Consequently,

$$\lim\_{k \rightarrow +\infty}\frac{H(w,k)}{k} = \lim\_{k \rightarrow +\infty} (1+n) - \frac{s(w, f^\prime (k))}{k} = 1+n > 0.$$

**Limit when $k \rightarrow 0$**

When $k$ tends to zero, we shall distinguish two cases regarding $f^\prime (k)$.
It can be that either

* Case $\lim\_{k \rightarrow 0} f^\prime (k) = f^\prime (0)> 0$ and finite.
 	Then, the function $s(w, f^\prime(k))$ is well defined and positive and we have:
	
	$$\lim\_{k \rightarrow 0} H(w,k) = \lim\_{k \rightarrow 0} \left[(1+n)k - s(w,f^\prime (k)) \right] = -s(w, f^\prime (k)) < 0.$$

* Case $\lim\_{k \rightarrow 0} f^\prime (k) = +\infty.$
	Two things can occur in that case.

	* Savings are positive: $\lim\_{k \rightarrow 0} s(w,f^\prime (k))>0.$
		This case is analogous to the previous one:
	
	$$\lim\_{k \rightarrow 0} H(w,k) = \lim\_{k \rightarrow 0} \left[(1+n)k - s(w,f^\prime (k)) \right] = -s(w, f^\prime (k)) < 0.$$

	* Savings tend to zero: $\lim\_{k \rightarrow 0} s(w, f^\prime (k)) = 0.$
		In this case, since the interest rate goes to infinity individuals tend to save zero.
		This implies that consumption in the second period, $d$, tends to infinity.
		To see this, first notice that $d = f^\prime (k) s(w, f^\prime (k)).$
		Moreover, from the first order conditions we know that:
		$$u^\prime (d) = \frac {u^\prime ( w - s)}{\beta f^\prime (k)}$$
		and hence
		$$\lim\_{k \rightarrow 0}u^\prime (d) = \lim\_{k \rightarrow 0}\frac {u^\prime ( w - s)}{\beta f^\prime (k)}=0.$$
		Hence, $u^\prime (d)$ tends to zero which means that $d$ goes to infinity.
		Therefore:
		$$\lim\_{k \rightarrow 0} f^\prime (k) s(w, f^\prime (k)) = +\infty.$$

		We also know that $0 < f^\prime (k) k < f(k)$ because $f^\prime (k) k + \omega(k) = f(k)$ and $\omega(k) > 0.$
		Therefore, for a bounded $0<k<1$ we also have $f^\prime (k) k < f(1).
		Hence, for $k\<1$:

		$$\frac{s(w, f^\prime (k))}{k} = \frac{f^\prime(k) s(w,f^\prime(k))}{f^\prime (k) k} > \frac{f^\prime (k) s(w, f^\prime (k))}{f(1)}.$$
		Then, 

		$$\lim\_{k \rightarrow 0} \frac{s(w,f^\prime(k)}{k} = +\infty$$
		and
		$$\frac{H(w,k)}{k} = 1+n-\frac{s(w,f^\prime(k)}{k} < 0$$
		for small $k$.


</details>

## Uniqueness of the intertemporal equilibrium

Having established that at least one level $k\_{t+1}$ exists that solves the equation, we would like it to be unique, thus having a unique equilibrium.
Otherwise, for some level $k$ there would be multiple values for $k\_{t+1}$ (meaning multiple values for the savings).
Individuals lack a coordinating mechanism to select any of these equilibria.

We show that the intertemporal elasticity of substitution $\sigma$ is important in determining uniqueness.
In particular, if $\sigma > 1$, then the equilibrium is unique.
We will revisit this issue [later.]({{< ref "Monotonicity_of_the_Dynamics" >}})

---

We have used the intermediate value theorem to show that solutions exist.
Moreover, it shows that $\lim\_{k\rightarrow 0} \frac{H(w,k)}{k} < 0$ and $\lim\_{k \rightarrow +\infty} \frac{H(w,k)}{k} > 0.$
Therefore, if $H(w,k)$ is monotonically increasing in $k$, then there is one and only one solution to $H(w,k)=0.$
Hence, we would have a unique solution.
This means that given a value $k\_{t},$ we can find a unique valu $k\_{t+1}.$

If we take the derivative of $H(w,k)$ with respect to $k$, we obtain:

$$1+n - s^{\prime}\_R f^{\prime \prime}(k).$$

Consequently, in order to have a monotonous function it is sufficient to impose:

**Assumption OLG.4** : $$1+n - s^{\prime}\_R f^{\prime \prime}(k) > 0.$$

And then, $k\_{t+1} = g(k\_{t}).$

In particular, this condition indicates that the effect of the interest rate on savings should _not_ be too negative.


Moreover, if **OLG.4** is verified, then $k\_{t+1}$ is increasing in $k\_{t}.$
Indeed, 

$$k\_{t+1} = g(k\_t, k\_{t+1}) = \frac{1}{1+n} s(\omega(k\_t), R(k\_{t+1})).$$

and 

$$\frac{\partial k\_{t+1}}{\partial k\_t} = - \frac{\frac{\partial g(k\_{t}, k\_{t+1})}{\partial k\_t}}{\frac{\partial g(k\_t, k\_{t+1})}{\partial k\_{t+1}}} = \frac{\overbrace{s^\prime\_{\omega} \omega^\prime(k\_t)}^{>0}}{1+n-s^\prime\_{R} \underbrace{R^\prime(k\_{t+1})}\_{=f^{\prime \prime} (k\_{t+1}) < 0}} > 0,$$

and $k\_{t+1}$ increases in $k\_{t}.$

Finally, we can use a more restrictive ---but easier to work with--- assumption that ensures a unique solution for the intertemporal equilibrium.
Assumption **OLG.4** states:

$$1+n - s^{\prime}\_R f^{\prime \prime}(k) > 0.$$

Therefore, it is sufficient to have

$$s^{\prime}\_R \geq 0$$

meaning that savings increase with the interest rate.
This behaviour is readily verified when the [intertemporal elasticity of substitution of at least one.]({{< ref "savings_function.md#intertemporal-elasticity-of-substitution" >}})
Then, to have monotonic dynamics and unique temporal equilibrium it is sufficient to have $\sigma \geq 1.$
