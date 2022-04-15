---
title: "Counting possibilities"
date: 2022-04-13T16:14:05-04:00
draft: true
toc: false
images:
categories:
  - Probability
tags:
  - probability
description: "
When counting possibilities, we need to consider whether a chosen observation is replaced after each trial, and whether the ordering of the event matters.
"
---

| | Ordered | Not Ordered |
| :--- | :---: | :---: |
| Replacement | $\|\mathcal S\|^n$ |             |
| No replacement | ${n \choose k} = \frac{n!}{k!(n-k)!}$ | $k{n \choose k} = \frac{n!}{(n-k)!}$ |

## All possibilities

In the case of a coin flip, our sample space contains only two elements: "heads" and "tails." The event space, however, is much larger than the sample space, especially as we add successive trials to our experiment.

Let $\mathcal B_n$ represent the event space corresponding to $n$ trials. Given our model of a coin flip, the corresponding event spaces for an experiment consisting of up to three independent trials are

$$
\begin{align*}
\mathcal B_1 &= \\{ H, T \\} \\\\
\mathcal B_2 &= \\{ HH, HT, TH, TT \\} \\\\
\mathcal B_3 &= \\{ HHH, HHT, HTH, HTT, THH, THT, TTH, TTT \\}
\end{align*}
$$

You may quickly notice a pattern in these event spaces: given $n$ trials with two possible outcomes, there are $2^n$ elements in the corresponding event space. This means that if we were to flip a coin 10 times, there would be 1,024 possible events in the event space.

Generally speaking, if we let $\mathcal S$ represent some well-defined sample space, $| \cdot |$ represent an operator which counts the number of elements in a set, and $n$ represent the number of independent trials in our experiment, then there are $|\mathcal S|^n$ elements within a corresponding event space, $\mathcal B_n$.

Consider, for example, three rolls of a six-sided die: The sample space for each die roll contains six possibilities, so a single trial yields one of six observations. An experiment consisting of three trials yields an event containing three ordered observations, with each observation realizing one of six possibilities. This is only one of $6^3 = 216$ possible events in our experiment's event space, $\mathcal B$.

You may already intuit some sense of likelihood with these numbers. Assuming that each event in the event space is equally likely, only one out of 216 possibilities exactly matches the outcome our experiment.

## Permutations (ordered w/o replacement)

## Combinations (unordered w/o replacement)

## Grouping (unordered w/ replacement)