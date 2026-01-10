---
title: PID
layout: default
parent: Functions
grand_parent: Reference
---
# PID()
---

## Syntax
`PID(target, current, p, i, d)`

## Returns
Number

## Description
A Proportional-Integral-Derivative (PID) controller that calculates an output to match a target requirement based on feedback from a current observed status.

## Arguments
* **target** (Number): The desired goal value.
* **current** (Number): The observed status variable to be compared against the target.
* **p** (Number): The Proportional constant; determines the magnitude of the immediate correction.
* **i** (Number): The Integral constant; determines how quickly the system corrects persistent errors.
* **d** (Number): The Derivative constant; prevents overshooting by dampening the correction.

## Examples
* `PID(10, AltitudeAgl, 1, 0.5, 2)` attempts to maintain the aircraft at a hover height of 10 meters.