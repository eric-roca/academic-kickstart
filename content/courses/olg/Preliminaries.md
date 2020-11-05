---
title: Preliminaries
linktitle: Preliminaries
toc: true
type: docs
date: "2019-07-11T00:00:00Z"
lastmod: "2019-07-11T00:00:00Z"
draft: false
menu:
  olg:
    parent: OLG model
    weight: 1 

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

In this model, time is discrete and extends from $t=0, 1, \ldots, \infty.$
Individuals make decisions at points in time.
We shall have initial conditions detailing the state of the economy at $t=0.$

## Individuals live for two periods

The main difference with respect to the Ramsey model is that in the OLG model, individuals live for two periods.
**Note:** this means that, at every point in time, two generations are alive and overlap.

This is relevant: the economy goes on forever but individuals only operate during some periods.
Hence, there will be infinite two-period-lived generations.
In particular, at $t=0$, we will have a young and an adult generation.
This adult generation will die at the end of $t=1$, the young generation will become adults and have children: the _new_ young generation of $t=2.$
Hence, we can represent the generations diagrammatically ---in brackets I have denoted the year in which each generation was born.

$t=0$     | $t=1$      | $t=2$      | $t=3$      | $t=4$      | $t=5$
----------|------------|------------|------------|------------|---------
Old (t=-1)| Die
Young(t=0) | Old (t=0)| Die
           | Young(t=1) | Old (t=1) | Die
	   |            | Young(t=2)  | Old (t=2)| Die
	   |            |             | Young(t=3) | Old (t=3) | Die
           |            |             |            | Young(t=4)  | Old (t=4)
           |            |             |            |             | Young(t=5)

To simplify the model, we assume that each adult born in $t-1$ has $n>-1$ children.
**Note:** we assume the number of children to be constant.<br/>
More complex set-ups include endogenous fertility.<br/>
These are the young population at time $t$
Therefore, the total population $N$ at time $t$ is composed of adults and young people.

$$N\_{t} = \underbrace{N\_{t-1}}\_{\mathrm{Adults}} + \underbrace{N\_{t-1}n}\_{\mathrm{Youngs}} = N\_{t-1}(1+n).$$

The total population at any time $t$ is:

$$N\_{t} = N\_{0}(1+n)^{t}.$$
