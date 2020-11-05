---
title: Changes in $G$
linktitle: Changes in $G$
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  ramsey_gov:
    parent: Introduction
    weight: 4 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4
---

We focus now on how a change in $G\_{t}$ affects the behaviour of the economy.
We rely on the phase diagram for this analysis: it conveys the message quite efficiently.
In what follows, we assume that the economy is at its steady-state level $(\bar{k}^{\mathcal{Gov}}, \bar{c}^{\mathcal{Gov}})$ when the government decides to change $G\_t.$
Furthermore, we assume taxes are constant at some level $G\_{t} = G\_{1} > 0.$

## Unexpected, permanent rise in $G$ {#un_perm}

Suppose that the government announces a _sudden and unexpected_ increase in $G: G\_{2} > G\_{1}.$
The Ramsey model illustrates the consequences of such a change.

First, we assumed that the economy was at its steady state.
The change in $G$, as we discussed before, moves the $k$-locus closer to the horizontal axis.

With the change in $G$, a new steady state emerges.
The steady-state capital level $\bar{k}^\mathcal{Gov}(G\_2) = \bar{k}^\mathcal{Gov}(G\_{1})$ remains the same.
However, households need to adjust their consumption level.
Otherwise, they would _not_ be on the saddle path, and they would follow a diverging trajectory leading to zero consumption.
The unique possibility that puts the economy in the new steady state is for consumption to jump directly into it.
This is, consumption must be reduced by the amount $\Delta\_{G} = G\_{2} - G\_{1}.$
Thus the size of the immediate fall in consumption is equal to the full amount of the increase in government purchases, and the **capital stock and the real interest rate are unaffected**.

A similar policy under the Solow model would have implied a smaller reduction in consumption.
In Solow, consumption is the fraction $1-s$ of current income.
The tax decreases current income by $G$, but consumption would only change by $(1-s)G < G.$
Hence, the remaining part of the increase in $G$ is absorbed by a reduction in investments of the size $sG$: _government purchases crowd out investment in the Solow model._

![permanent_increase](/img/ramsey_gov/permanent_increase.png)

## Unexpected, temporary rise in $G$ {#un_temp}

Different from before, suppose that the increase in $G$ is only temporary, starting at $t=t\_{0}$ and lasting until $t=t\_{1}.$
We still suppose that the increase in taxes is unexpected.
One possibility is to first jump to the new steady state, remain there while taxes are high, and at time $t=t\_{1}$ jump back to the original steady state.
However, this implies two discontinuities in consumption: the first and second jumps.
This would imply that marginal utility falls discontinuously and this is not optimal.

There is a second possibility.
First, decrease consumption by a smaller amount than before: $\Delta\_{c} < \Delta\_{G}.$
This implies that the economy is _not_ in the new steady state $(\bar{k}^\mathcal{Gov}(G\_2) , \bar{c}^{\mathcal{Gov}}(G\_{2}))$, but above it.
Thus, it is subject to the dynamics implied by the phase diagram: capital decreases and consumption increases.
The initial jump in consumption must be carefully computed such that, at time $t=t\_{1}$, the dynamics implied by $G\_{2}$ put the economy on the saddle path of $G\_{1}.$
This is, the economy undergoes a transition such that, at $t=t\_{1}$ when taxes and dynamics ---and the phase diagram--- return to the original  configuration, the economy is on its saddle path.


![temporary_increase](/img/ramsey_gov/temp_increase.png)

The figure above depicts in black the original $k$-locus ---for $G=G\_{1}$--- and in red the temporary one while with $G=G\_{2}.$
The economy first jumps from the initial steady state $(\bar{k}^{\mathcal{Gov}}(G\_{1}), \bar{c}^{\mathcal{Gov}}(G\_{1}))$ following the black arrow.
From then onwards, the dynamics of the red $k$-locus determine the trajectory of the economy.
In particular, it moves north-west following the orange curve.
The initial jump is calculated in such a way that at $t=t\_{1}$ the economy is on the saddle path corresponding to $G=G\_{1}.$
From there, it simply follows the saddle path towards the steady state $(\bar{k}^{\mathcal{Gov}}(G\_{1}), \bar{c}^{\mathcal{Gov}}(G\_{1})).$

During the transition, households reduce capital to sustain a higher and increasing level of consumption that would not be possible with $G\_{2} > G\_{1}.$
From $t=t\_{1}$, consumption continues to grow, but capital starts accumulating again.

![temporary_increase_2](/img/ramsey_gov/temp_increase_2.png)

The change in consumption during $t=t\_{0}$ is directly proportional to the length of the increase in taxes.
The longer it is, the closer the economy jumps to the steady state $(\bar{k}^{\mathcal{Gov}}(G\_{2}), \bar{c}^{\mathcal{Gov}}(G\_{2})).$
However, it never reaches it: households always decrease their savings, which allows them to later be on the saddle path when taxes go back to $G\_{1}.$

## Anticipated, permanent rise in $G$ 

**Note:** when analysing an _anticipated_ measure, start from the end move backwards.

Suppose that at time $t=t\_{0}$ the government announces that at time $t=t\_{1}$ taxes will permanently increase.

One possibility is to mimic the [unanticipated, permanent change](<{{ ref "#un_perm" >}}): remain at the original steady state $(\bar{k}^\mathcal{Gov}(G\_{0}), \bar{c}^\mathcal{Gov}(G\_{0}))$ until $t\_{1}$, and then jump onto the new steady state.
However, this represents a large cost in terms of utility: non-smooth changes penalise utility.

Instead, households will slightly decrease consumption at $t\_{0}$.
The dynamics of the $(\bar{k}^\mathcal{Gov}(G\_{0}), \bar{c}^\mathcal{Gov}(G\_{0}))$ steady state will move the economy south-east: consumption decreases while capital increases.
The first initial jump at $t\_{0}$ must be such that, at $t\_{1}$ the economy is on the saddle path corresponding to the new steady state $(\bar{k}^\mathcal{Gov}(G\_{1}), \bar{c}^\mathcal{Gov}(G\_{1})).$

![perm_an](/img/ramsey_gov/perm_an_increase.png)

Hence, during the transition, consumption continuously falls, but smoothly.
Capital, instead, first accumulates and decreases from $t\_{1}$ onwards.

![perm_an2](/img/ramsey_gov/perm_an_increase_2.png)

## Anticipated, temporary rise in $G$

**Note:** when analysing an _anticipated_ measure, start from the end move backwards.

Finally, suppose that the increase in $G$ is temporary.
At time $t=t\_{0}$ the government announces that at time $t=t\_{1}$ taxes will increase from $G\_{0}$ to $G\_{1}.$
The new tax regime will apply for some time, until $t=t\_{2}$ when taxes will return to their original level $G\_{0}.$

In that case households can decide to follow the same strategy as in an [unanticipated, temporary increase]({{< ref "#un_temp" >}}).
However, it entails a relatively large adjustment in terms of consumption at time $t=t\_{1}$, when the new policy becomes effective.
Instead, households can take advantage of the anticipation in the announcement:
decrease the consumption at the announcement time $t=t\_{0}$ by a relatively small amount.
This places households on the black arrow trajectory, since the economy is still governed by the $(\bar{k}^\mathcal{Gov}(G\_{0}), \bar{c}^\mathcal{Gov}(G\_{0}))$-locus.
In that case, though, the change in consumption is such that, when the new tax policy becomes effective, consumption follows the orange arrow.
Finally, timing is again crucial because at time $t=t\_{2}$ the economy must be on the saddle path that corresponds to the initial steady state: $(\bar{k}^\mathcal{Gov}(G\_{0}), \bar{c}^\mathcal{Gov}(G\_{0})).$

![an_temp_inc](/img/ramsey_gov/temp_an_increase.png)

In that case, between $t\_{0}$ and $t\_{1}$, households decrease consumption and save.
Between $t\_{1}$ and $t\_{2}$ first consumption continues to decrease and so does capital, but eventually consumption rises while capital continues to decrease.
Finally, from $t\_{2}$ onward, both capital and consumption rise along the saddle path.
Note that, although consumption decreases, it does so continuously except for the initial jump.
This consumption-smoothing decreases utility less than a discontinuous jumps.

![an_temp_inc](/img/ramsey_gov/temp_an_increase_2.png)
