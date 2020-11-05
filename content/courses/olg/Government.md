---
title: Debt and public expenditures
linktitle: Debt and public expenditures
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 9

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 9

---

Based on _de la Croix and Michel, Chapter 4.4_

## The Ricardian equivalence

The Ricardian equivalence states that forward-looking agents internalise the government's budget constraint when deciding.
Hence, whether public expenditures are financed using debt or taxes is irrelevant.

Intuitively, forward-looking agents ---who shall live forever-- know that, if the government increases expenditures today without raising taxes, debt will be issued and taxes eventually increased to pay it off.

However, as we shall see, in the **OLG model, the Ricardian equivalence does not hold.**
Clearly, the main difference between the OLG and Ramsey models is that agents live only for two periods in the former.
Suppose that the government decides to run a deficit today to increase public expenditures.
Young and old individuals today are not that much affected because, when the government raises the taxes to pay the debt off, they would have already died.
Instead, if the government decides to increase taxes today, it affects present-day young and old individuals.

## The model with a government

### The government

Suppose the government has public expenditures of $g\_t$ per young individual.
Total expenditures are then $G\_t = N\_t g\_t.$
These public expenditures are financed by a lump-sum tax of $\tau\_t$, which is paid only by the young.
Total revenues are $T\_t = N\_t \tau\_t.$
Finally, the government can have debt.
The total outstanding debt is $B\_t,$ and $b\_t$ represents it per young terms.
The government pays interest on the debt of the previous period: $R\_t B\_{t-1}.$

We can write the government's budget constraint:

$$G\_t + R\_t B\_{t-1} = B\_t + T\_t.$$

The constraint, expressed in per capita terms, is:

$$\frac{G\_t}{N\_t} + R\_t \frac{B\_{t-1}}{N\_t} = \frac{B\_t}{N\_t} + \frac{T\_t}{N\_t} = $$
$$g\_t + R\_t \underbrace{\frac{B\_{t-1}}{N\_{t-1}}}\_{b\_{t-1}}\underbrace{\frac{N\_{t-1}}{N\_{t}}}\_{\frac{1}{1+n}} = b\_t + \tau\_t = $$
$$g\_t + R\_t \frac{b\_{t-1}}{1+n}  = b\_t + \tau\_t $$

As a final note, government spending is unproductive: it does not affect the production function.
Moreover, individuals do _not_ derive utility from it.
Finally, we assume that the government _always_ honors its debt. 
In that sense, government debt is a riskless asset.

### Individuals

The budget constraint of a young individual who now pays taxes $\tau\_t$ is:

$$w\_t = c\_t + s\_t + \tau\_t$$
$$R\_{t+1}s\_t = d\_{t+1}.$$

Alternatively, we can express it as an intertemporal budget constraint:

$$w\_t = c\_t + \tau\_t +\frac{d\_{t+1}}{R\_{t+1}}.$$

We can easily obtain the savings function as we did before by substitution:

$$\max\_{c\_t, s\_t, d\_{t+1}} u(c\_t) + \beta u(d\_{t+1})$$
$$\mathrm{s.t.}\, w\_t = c\_t + s\_t - \tau\_t$$
$$\phantom{\mathrm{s.t.}}\, d\_{t+1} = R\_{t+1}s\_t.$$

Then:

$$\max\_{s\_t} u(w\_t-s\_t-\tau\_t) + \beta u(R\_{t+1}s\_t).$$

The first order condition reads:

$$u^\prime(w\_t - s\_t-\tau\_t) = \beta R\_{t+1} u^\prime(R\_{t+1}s\_t).$$

From here, we can recover the savings function: 

$$s\_t = s(w\_t-\tau\_t, R\_{t+1}).$$

In this model, households have access to **two** types of savings: 

* savings in capital
* and government bonds.

Moreover, the risk of both types of investment is the same: none, because both assets are riskless.
Hence, **bonds and capital are perfect substitutes.** in the portfolio of wealth owners.[^1]
Therefore, the entire amount households decide to save is split between the two

[^1]: We have implicitly assumed it when we stated that bonds payed the same interest rate as capital.

$$N\_t s\_t = K\_{t+1} + N\_t b\_t.$$

### Equilibrium

At the (temporal) equilibrium , the government chooses $B\_t, \tau\_t$ to satisfy its budget constraint: $g\_t + R\_t \frac{b\_{t-1}}{1+n}  = b\_t + \tau\_t.$
Moreover, as we have already discussed, because debt and capital are substitutes, both bear the same interest $R.$
Also, firms operate in a perfectly competitive environment and factors are paid their marginal productivities:

$$w\_t = \omega(k\_t)$$
<center>and</center>
$$R\_t = f^\prime(k\_t)$$
with $k\_t \equiv \frac{K\_t}{N\_t}.$

Introducing this into the government budget constraint we obtain:

$$B\_t + N\_t \tau\_t = G\_t + f^\prime(\color{red}{k\_t})B\_{t-1}.$$

We have implicitly assumed that investment is positive, this is,
$$K\_{t+1} = N\_t s\_t - B\_t = N\_t s(w\_t - \tau\_t, R\_{t+1}) - B\_t >0.$$

Capital thus evolves:

$$K\_{t+1} = N\_t s\_t - N\_t b\_t \implies k\_{t+1} = \frac{1}{1+n} s(\omega(k\_t)-\tau\_t, R(k\_{t+1})) - b\_t.$$

### Constant deficit policy

To simplify the analysis, we assume that the government faces constant expenditures $g\_t = g$ and that the number of bonds is also constant: $b\_t = b.$
The government can adjust the tax rate $\tau\_t$ each period.
Therefore, the _deficit_ at time $t$ is given by:

$$\mathcal{d}\_t \equiv g - \tau\_t = b\left(1-\frac{R\_t}{1+n}\right) = b\left(\frac{n+\delta - r\_t}{1+n}\right),$$

where we have used $R\_t = 1 + r\_t - \delta$ together with the budget constraint of the government evaluated when $g\_{t}=g$ and $b\_{t}=b:$

$$g + \frac{b}{1+n}R\_{t} = \tau\_{t} + b \implies g - \tau\_{t} = b\left(1-\frac{R\_{t}}{1+n}\right).$$

If $n + \delta > r\_t$, then the government can be perpetually indebted while running a public deficit $g-\tau\_t.$
Otherwise, if $n + \delta < r\_t$, the government needs to run a budget surplus: $\tau\_t > g.$

Replacing the new government budget $g - \tau\_t = b\left(\frac{n+\delta - r\_t}{1+n}\right)$ in the equation for capital dynamics we obtain:

$$k\_{t+1} = \frac{1}{1+n}s\left(\omega(k\_t)-b\frac{r(\color{red}{k\_t})-\delta - n}{1+n}-g, R(\color{green}{k\_{t+1}})\right)- \frac{b}{1+n}.$$

In this case, the _policy parameters_ $g, b$ affect the evolution of the capital stock.
Notice also that if $b=g=0$ we recover the original version of the OLG model.

### Steady state

For the moment, let's assume that this model features, at least, one steady state.
As usual, we denote its level of capital by $\bar{k}.$

As before, we can compute how $k\_{t+1}$ changes with $k\_t.$

$$\frac{\partial k\_{t+1}}{\partial k\_t} = \frac{s^\prime\_{\omega}\left(w^\prime (k\_t)-b\frac{r^\prime (k\_t)}{1+n}\right)}{1+n-s^\prime\_{R}R^\prime (k\_{t+1})}.$$

Since $r^\prime (k) <0$ we can already see that the speed at which capital adjusts in the presence of a government is larger than without it.

$$\frac{s^\prime\_{\omega}\left(\omega^\prime (k\_t)-b\frac{r^\prime (k\_t)}{1+n}\right)}{1+n-s^\prime\_{R}R^\prime (k\_{t+1})} > \frac{s^\prime\_{\omega}\omega^\prime (k\_t)}{1+n-s^\prime\_{R} R^\prime(k\_{t+1})}.$$

Also, notice that the numerator is positive: $\omega^\prime (k) - b \frac{\overbrace{r^\prime(k)}^{<0}}{1+n} > 0.$
Hence,if $1+n-s^\prime\_{R}R^\prime(k) > 0$ the dynamics will be monotonous.
A sufficient condition is $s^\prime\_{R} > 0 \implies \sigma > 1.$
Let's assume this condition is verified.

### Stability

We have assumed that a steady state exists.
We analyse its stability.
In particular, we should evaluate the derivative $\frac{\partial k\_{t+1}}{\partial k\_t}$ at the steady state:

$$\frac{\partial k\_{t+1}}{\partial k\_t} = \frac{s^\prime\_{\omega}\left(w^\prime (k\_t)-b\frac{\overbrace{r^\prime (k\_t)}^{<0}}{1+n}\right)}{1+n-s^\prime\_{R}R^\prime (k\_{t+1})}.$$

At the steady state we have that:


$$\frac{\partial k\_{t+1}}{\partial k\_t}\Bigg|\_{k\_t=k\_{t+1}=\bar{k}} = \frac{s^\prime\_{\omega}\left(w^\prime (\bar{k})-b\frac{\overbrace{r^\prime (\bar{k})}^{<0}}{1+n}\right)}{1+n-s^\prime\_{R}R^\prime (\bar{k})}.$$

We then have that the steady state is stable if $\frac{\partial k\_{t+1}}{\partial k\_t}\Bigg|\_{k\_t = k\_{t+1} = \bar{k}} \in (-1,1).$
Therefore, the steady state is stable if and only if:

$$\frac{s^\prime\_{\omega}\left(w^\prime (\bar{k})-b\frac{\overbrace{r^\prime (\bar{k})}^{<0}}{1+n}\right)}{1+n-s^\prime\_{R}R^\prime (\bar{k})} < 1 \implies s^\prime\_\omega \omega^\prime(\bar{k})-b\frac{r^\prime(\bar{k})}{1+n} < 1+n-s^\prime\_R R^\prime(\bar{k}).$$

We shall assume that the steady state is stable.
Hence, we assume that:

$$s^\prime\_\omega \omega^\prime(\bar{k})-b\frac{r^\prime(\bar{k})}{1+n} < 1+n-s^\prime\_R R^\prime(\bar{k}).$$

### The effects of fiscal policy on $\bar{k}$

We can now study how the fiscal policy variables $b$ and $g$ affect the steady-state level of capital.

$$\bar{k}=\frac{1}{1+n}s\left(w(\bar{k})-b\frac{r(\bar{k})-n-\delta}{1+n}-g, R(\bar{k})\right)-\frac{b}{1+n}.$$

$$\frac{\partial \bar{k}}{\partial b} = - \frac{s^\prime\_{\omega}\left(\frac{r(\bar{k}) -n - \delta}{1+n}\right)+1}{\underbrace{1+n-s^\prime\_\omega \left(\omega^\prime(\bar{k})-b\frac{r^\prime(\bar{k})}{1+n}\right)-s^\prime\_R R^\prime(\bar{k})}\_{>0\, \mathrm{because\, of\, stability}}}.
$$

Using the fact that $R(k) = 1 + r(k) - \delta$ we can rewrite the numerator as:

$$s^\prime\_{\omega}\left(\frac{r(\bar{k}) -n - \delta}{1+n}\right)+1=s^\prime\_\omega \left(\frac{R(\bar{k})-1-n}{1+n}\right)+1 = 1 - \underbrace{s^{\prime}\_\omega}\_{\in (0,1)} + \underbrace{s^\prime\_\omega}\_{>0} \frac{R(\bar{k})}{1+n} > 0.$$

We showed that $s^\prime\_{\omega} \in (0,1)$ when we discussed [the savings function.]({{< ref "Savings_function.md#the-effect-of-wages" >}})

Then, we have that

$$\frac{\partial \bar{k}}{\partial b} = - \frac{s^\prime\_{\omega}\left(\overbrace{1-s^\prime\_\omega+s^\prime\_\omega\frac{R(\bar{k})}{1+n}}^{>0}\right)}{\underbrace{1+n-s^\prime\_\omega \left(\omega^\prime(\bar{k})-b\frac{r^\prime(\bar{k})}{1+n}\right)-s^\prime\_R R^\prime(\bar{k})}\_{>0\, \mathrm{because\, of\, stability}}}< 0 .$$


We proceed similarly with $g$:

$$\frac{\partial \bar{k}}{\partial g}= - \frac{s^\prime\_\omega}{\underbrace{1+n-s^\prime\_\omega \left(\omega^\prime(\bar{k})-b\frac{r^\prime(\bar{k})}{1+n}\right)-s^\prime\_R R^\prime(\bar{k})}\_{>0\, \mathrm{because\, of\, stability}}}< 0 .$$

Therefore, as long as the steady state is stable, increasing the fiscal policies decreases the long-run value of $\bar{k}.$
In other terms, higher expenditures or debt reduce capital.
Thus, the fiscal policy **makes over-accumulation less likely** if the steady state is stable.
The role of debt is intuitive: government bonds are perfect substitutes with capital, hence households holding them invest less in capital.
Similarly, higher expenditures must be financed either with debt or taxes.
The latter reduces available income, which reduces savings, impacting capital accumulation.

## Example

To illustrate the findings so far we proceed with an example.
As usual, we take a log-utility function and a Cobb-Douglas production function.
**Note:** this choice of utility already implies that $s^\prime\_R = 0.$

Furthermore, we assume that $\delta = 1:$ capital fully depreciates in one period.
Since here one period corresponds to roughly 30 years, this may be a good approximation.

$$f(k) = k^\alpha, \alpha \in (0,1)$$
$$u(c,d) = \log ( c ) + \beta \log(d), \beta \in (0,1).$$

The budget constraint is:

$$w\_t = c\_t + s\_t + \tau\_ t$$
$$d\_{t+1} = R\_{t+1} s\_t.$$

We can readily see that the savings function satisfies:

$$u^\prime(w\_t - \tau\_t - s\_t) = R\_{t+1}\beta u^\prime (R\_{t+1} s) \implies s\_t = \frac{\beta}{1+\beta}(w\_t - \tau\_t).$$

With the technology we are given we also know that:

$$R\_t = \alpha k\_t^{\alpha-1},\quad  w\_t = (1-\alpha)k\_t^\alpha.$$

The law of motion of capital follows:

$$k\_{t+1} = \frac{1}{1+n}s\left(w\_t - \tau\_t \right) = \frac{1}{1+n}\frac{\beta}{1+\beta}(w\_t - \tau\_t) - \frac{b}{1+n}.$$

We can already substitute into it the equilibrium values for the interest rate and the government's budget constraint:

$$\tau\_t = g + \frac{R\_t - 1 -n}{1+n}.$$

Hence

$$k\_{t+1} = \frac{\beta}{(1+n)(1+\beta)}\left((1-\alpha)k\_t^\alpha - b \frac{\alpha k\_t^{\alpha -1} -1 -n}{1+n}-g\right)-\frac{b}{1+n} =  \xi \left((1-\alpha)k\_t^\alpha - b \frac{\alpha k\_t^{\alpha -1}}{1+n}-g\right)-\frac{b}{1+n}+\xi b = \phi(b,g,k\_t),$$
where $\xi \equiv \frac{\beta}{(1+n)(1+\beta)}.$

### Stability

Instead of computing the value of capital at the steady state (which we cannot do), we study the function $\phi(b,g,k\_t).$

First, notice that changing $b$ or $g$ displaces $\phi$ downwards, but the displacement is not parallel.
$$\phi^\prime\_b = - \frac{\beta}{(1+n)(1+\beta)}\frac{\alpha k^{\alpha-1}}{1+n} - \frac{1}{1+n} + \xi < 0$$
$$\phi^\prime\_g = -\frac{\beta}{(1+n)(1+\beta)} < 0.$$

However, increasing $g$ always reduces $k\_{t+1}$ by the same amount: $g$ moves the curve vertically.
$$\phi^{\prime \prime}\_{g,k} = 0.$$
Instead, raising $b$ has a different effect depending on the value of $k.$
In particular, the gap widens and reaches a constant difference:
$$\phi^{\prime \prime}\_{b,k} = \frac{k^{\alpha-2}(1-\alpha)\alpha\beta}{(1+n)^2(1+\beta)} > 0$$
and
$$\lim\_{k \rightarrow +\infty}\phi^{\prime \prime}\_{b,k} = 0.$$

The function $\phi$ is increasing and concave in $k$:

$$\phi^\prime\_k = \xi \left((1-\alpha)k^{\alpha-1}-\frac{b \alpha (\alpha-1)}{1+n}k^{\alpha-2}\right) > 0.$$
$$\phi^{\prime \prime}\_{k,k} = \xi \left((1-\alpha)(\alpha-1)k^{\alpha-2}-\frac{b \alpha(\alpha-1)(\alpha-2)}{1+n}k^{\alpha-3}\right) < 0.$$

Finally, we have the following limits:

$$\lim\_{k \rightarrow 0}\phi = 0 \, \mathrm{if} \, b=0$$
$$\lim\_{k \rightarrow 0}\phi = -\infty \, \mathrm{if} b>0.$$
$$\lim\_{k \rightarrow +\infty}\phi = +\infty.$$

![taxes](/img/olg/taxes.png)

When $b=g=0$ we are back to the initial case without government.
The Cobb-Douglas and log-utility specifications are characterised by two steady states:

* $\bar{k} > 0$, which is stable,
* $\bar{k}=0$, which is unstable.

With $b,g>0$ the $k\_{t+1}$ curve moves downwards and the economy displays two steady states:

* $\bar{k}$, which is unstable,
* $\overline{k}$, which is stable.

There are two additional possibilities:
in the first one, the $k\_{t+1}$ curve is tangent to the 45 degree line.
In that (unlikely) case, a unique steady state arises, but it is non-hyperbolic and we cannot infer its stability from the linearised version.
**Note:** we know that the steady state is non-hyperbolic because $k\_{t+1}$ evaluated at the steady state is tangent to a 45 degree line.

In the second case, if $b$ or $g$ are big enough, the economy has no steady state.
