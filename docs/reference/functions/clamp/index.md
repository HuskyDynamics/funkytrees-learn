---
title: clamp
layout: default
parent: Functions
grand_parent: Reference
---
# clamp()
---

## Syntax
`clamp(x, min, max)`

## Returns
Number

## Description
Restricts the input value so that it stays between the specified minimum and maximum bounds.

## Arguments
* **x** (Number): The value to be clamped.
* **min** (Number): The lower bound.
* **max** (Number): The upper bound.

## Examples
* `clamp(Throttle, 0.2, 0.8)` ensures the output never drops below 0.2 or exceeds 0.8.