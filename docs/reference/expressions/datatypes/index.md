---
title: Data Types
layout: default
parent: Expressions
nav_order: 1
---
# Data Types
#### Reference for the fundamental data types utilized in Funky Trees expressions.
---

## Numbers
Numbers represent quantitative values and include both integers and floating-point values (floats). They are the primary data type used for continuous mathematical calculations and telemetry data.

* **Format**: Standard numerical representation.
* **Examples**: `1`, `1314`, `12.0003`, `0.334`.

## Booleans
Booleans represent logic states and are primarily used for conditional statements, toggles, and binary activation groups.

* **Literal Values**: `true`, `false`.
* **Numeric Conversion**: When evaluated in a numeric context (in conjunction with number-type data), booleans automatically convert to specific integer values:
    * `true` evaluates to `1`.
    * `false` evaluates to `-1`.
* **Behavior**: Booleans maintain their literal `true`/`false` states when evaluated independently of other data types.

## Strings
Strings are sequences of alphanumeric characters representing text data.

* **Format**: Text must be enclosed in double quotation marks (`""`).
* **Examples**: `"Text"`, `"Boom 50"`, `"Cannon"`.
* **Usage**: Strings are utilized for weapon identification and as arguments for specific functions.
    * **Variable Example**: The `SelectedWeapon` variable returns a string representing the name of the active weapon.
    * **Function Example**: The `ammo("string")` function requires a string input to identify the weapon being queried.