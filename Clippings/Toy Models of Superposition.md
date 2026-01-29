---
title: "Toy Models of Superposition"
source: "https://transformer-circuits.pub/2022/toy_model/index.html#motivation"
author:
  - "[[Nelson Elhage∗]]"
  - "[[Tristan Hume∗]]"
  - "[[Catherine Olsson∗]]"
  - "[[Nicholas Schiefer∗]]"
  - "[[Tom Henighan]]"
  - "[[Shauna Kravec]]"
  - "[[Zac Hatfield-Dodds]]"
  - "[[Robert Lasenby]]"
  - "[[Dawn Drain]]"
  - "[[Carol Chen]]"
published:
created: 2026-01-29
description:
tags:
  - "clippings"
---
We hypothesize that there are really two countervailing forces driving this:

Privileged Basis: Only some representations have a privileged basis which encourages features to align with basis directions (i.e. to correspond to neurons).

Superposition: Linear representations can represent more features than dimensions, using a strategy we call superposition. This can be seen as neural networks simulating larger networks. This pushes features away from corresponding to neurons.

features as properties of the input which a sufficiently large neural network will reliably dedicate a neuron to representing