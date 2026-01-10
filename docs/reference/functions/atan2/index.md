---
title: atan2
layout: default
parent: Functions
grand_parent: Reference
---
# atan2()
---

## Syntax
`atan2(y, x)`

## Returns
Number

## Description
Returns the angle in degrees whose tangent is the quotient of two specified numbers (`y/x`). Unlike `atan()`, this function evaluates the signs of both arguments to determine the correct quadrant of the resulting angle.

## Arguments
* **y** (Number): The y-coordinate (vertical component).
* **x** (Number): The x-coordinate (horizontal component).

## Examples
* `atan2(1, 1)` results in `45`.
* `atan2(1, -1)` results in `135`.
* `atan2(-1, -1)` results in `-135`.
* `atan2(VerticalG, GForce)` can be used to determine the angle of the total G-force vector.