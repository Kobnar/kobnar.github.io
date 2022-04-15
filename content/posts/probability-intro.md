---
title: "A primer on basic probability"
date: 2022-04-13T16:13:52-04:00
draft: true
toc: false
images:
categories:
  - Probability
tags:
  - probability
description: "
\"Probability Theory\" refers to the mathematical treatment of theoretical likelihood in the face of uncertainty. We model a discrete action as a repeatable \"trial\" which yields an \"observation\" drawn from a \"sample space\" of every possible observation. We then model an \"experiment\" as one or more repeated trials that yields an \"event\" drawn from an \"event space\" of every possible event. Given a \"probability set function\" which maps each possible observation to a particular numeric likelihood, we can compute the overall likelihood of a desired event.
"
---

## What is the theory of probability?

"Probability Theory" refers to the mathematical treatment of theoretical likelihood in the face of uncertainty. Essentially, our goal is to analytically quantify uncertainty. More specifically, we are trying to predict the realization of some unknowable state, given some model of possibility within our world. In other words, we are trying to determine a degree of confidence that a predicted outcome conforms to reality.

Notice that I said "model" to describe our concept of what is possible. Like any mathematical model, our world and the possibilities within it are abstractions. "Flipping a coin," for example, is a common theoretical "world" consisting entirely of a "trial" for which the only possible outcomes are either "heads" or "tails."

In real life, of course, a coin can land on its edge and roll underneath the fridge. It could be a trick coin with two heads. It could be magnetized into a dipole and thrown into a powerful electric field so that "heads" is essentially a deterministic outcome. Don't these things matter?

The short answer is *don't worry about it.* We're not concerned about edge cases, parlor tricks, or contrived magnetism. We are generalizing a physical system into a mathematical abstraction so we can use deductive reasoning to say something about the real world. If a particular model insufficiently represents the features of the real world, simply use a better model. As long as it conforms to a basic construction, the theory of probability can help you say something about the physical system you are trying to represent.