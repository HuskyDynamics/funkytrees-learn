---
title: Variable Setters
layout: default
parent: Custom Variables
grand_parent: Variables
nav_order: 1
---

# Variable Setters
#### Technical reference for user-defined global variables and logic resolution.
---

Variable Setters allow for the creation of global custom variables within a craft. These allow for expression values that can be accessed by any Funky Trees expression without needing to re-calculate them locally.

## Configuration
Variable Setters are managed through the "Variable Setters" menu in the aircraft designer. Each entry defines how a specific variable name should behave based on logic and priority.

## Properties
* **Name**: The unique identifier for the variable used in Funky Trees expressions.
* **Expression**: The mathematical or logical formula used to calculate the variable's value.
* **Activator**: A Boolean expression that switches the setter on or off. When the activator is false, the setter does not update the variable.
* **Priority**: A numerical value that determines the precedence of the setter. If multiple setters target the same variable name, the one with the highest priority value controls the output.

## Logic Resolution
* **Global Scope**: Once defined, these variables are available globally. You do not need a prefix to call them in other expressions.
* **Precedence**: When no priority is specified, variable setters evaluate in the order shown in the variable setter menu. Priority, when used appropiately, allows for complex state-based logic, where different expressions can control the same variable depending on which setter's activator is currently engaged.

## Technical Notes
* **Update Rate**: Variable setter expressions are evaluated per-tick; the frequency is determined by the game physics quality setting.
* **Naming Conflicts**: Custom variable names must not match built-in variable names.