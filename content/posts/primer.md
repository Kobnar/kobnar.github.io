+++ 
draft = true
date = 2022-04-12T11:56:16-04:00
title = "A basic primer on probability"
description = "A basic primer on set-based probability theory."
slug = "primer"
authors = ["kobnar"]
tags = []
categories = ["Probability"]
externalLink = ""
series = []
+++

_Probability is the study of theoretical likelihood. The idea is to describe some "sample space" of possible outcomes which we use to calculate the likelihood of observing a particular set of outcomes called an "event space." The likelihood of a particular event is described by a "probability set function" which outputs some numeric value between 0 and 1 which corresponds to the likelihood of a particular event._

## What is the theory of probability?

Probability theory is an anlytical study of likelihood. Essentially, our goal is to analytically quantify uncertainty. More specifically, we are trying to predict the realization of some unknowable state, given some model of possibility within our world. In other words, we are trying to determine a degree of confidence that a predicted outcome conforms to reality.

Notice that I said "model" to describe our concept of what is possible. Like any mathematical model, our world and the possibilities within it are abstractions. "Flipping a coin," for example, is a common theoretical "world" consisting entirely of a "trial" for which the only possible outcomes are either "heads" or "tails."

In real life, of course, a coin can land on its edge and roll underneath the fridge. It could be a trick coin with two heads. It could be magnetized into a dipole and thrown into a powerful electric field so that "heads" is essentially a deterministic outcome. Don't these things matter?

The short answer is *don't worry about it.* We're not concerned about edge cases, parlor tricks, or contrived magnetism. We are generalizing a physical system into a mathematical abstraction so we can use deductive reasoning to say something about the real world. If a particular model insufficiently represents the features of the real world, simply use a better model. As long as it conforms to a basic construction, the theory of probability can help you say something about the physical system you are trying to represent.

## Modeling the world

Let's go back to when I said that "flipping a coin" was a theoretical "world." What does that even mean? What goes into a model of the world?

To begin with, let's think about the real world for a second. Consider what goes into a coin flip: we flip a disk with two marked sides into the air in such a way that it rotates around some unknown axis at some unknown rate for some unknown amount of time until it comes to rest on a designated surface, at which point we look at the coin to see which of the two marked sides is facing "up."

In the  On one hand, we know that only one of two sides of a coin can be facing "up" by the end of a successful flip because of the physical properties of a coin. On the other hand, we don't know which side will be facing "up" because of the chaotic nature of the flip. With this information, we have what we need to construct our theoretical model of the world.

In the language of probability, each coin flip is called a "trial," the set of possible outcomes for each trial is called the "sample space," and the result of a particular trial is called an "observation." By definition, each observation must correspond to a single element in the sample space. It's also necessary to point out that we can conduct multiple trials, and that we refer to a collection of one or more trials as an "experiment." Finally, an experiment yields an ordered set of observations called an "event," while the set of all possible events is called the "event space."

Translating all of this into human speak, we say the outcome (an observation) of a single coin flip (a trial) can take on one of two possibilities (the sample space). If we conduct multiple coin flips (an experiment) the ordered set of corresponding outcomes (an event) is one of several possible sets of outcomes (the event space).

## Counting possibilities

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

## Order and replacement

## Introducing likelihood (a.k.a. probability)

We begin with the assumption that each element in the sample space is equally likely. In the case of a coin flip, this would mean that a single trial is equally as likely to result in an observation of "heads" as "tails." 