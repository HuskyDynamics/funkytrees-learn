---
title: Variables
layout: default
parent: Learn
nav_order: 5
---
# Variables
#### An introduction to the data sources available to your aircraft.
---

Variables are the "inputs" for your expressions. They come in several different types, each with their own use cases and characteristics.

## Number Variables

Number variables are simply variables that produce a number based on their associated input condition, and are by far the most common variable type. Some number variables have inherent limits built into their output ranges, meaning that they will only ever output values within their assigned range. Other number variables are unrestricted, and can output any valid decimal value.

The following groups of number-type input variables are available for every craft. See [Built-in Variables](/funkytrees/docs/reference/variables/builtin/) for details about each one.

<details>
<summary>

### Flight Controls
</summary>

|   Name   	|     Description     	|    Range    	|
|:--------:	|:-------------------:	|:-----------:	|
| `Throttle` 	| Throttle axis input 	|  `0` to `1` 	|
|   `Brake`  	|   Brake axis input  	|  `0` to `1` 	|
|   `Roll`   	|   Roll axis input   	| `-1` to `1` 	|
|   `Pitch`  	|   Pitch axis input  	| `-1` to `1` 	|
|    `Yaw`   	|    Yaw axis input   	| `-1` to `1` 	|
|   `Trim`   	|  Trim slider input  	| `-1` to `1` 	|
|   `VTOL`   	|  VTOL slider input  	| `-1` to `1` 	|
|   `Flaps`  	|  Flaps slider input 	| `-1` to `1` 	|

</details>

<details>
<summary>

### Craft State
</summary>

| Name | Description | Range |
|:---:|:---:|:---:|
| `Altitude` | Distance from sea level (meters) | `-inf` to `inf` |
| `AltitudeAgl` | Distance from ground (meters) | `-inf` to `inf` |
| `IAS` | Indicated airspeed (m/s) | `0` to `inf` |
| `TAS` | True airspeed (m/s) | `0` to `inf` |
| `GS` | Ground speed (m/s) | `0` to `inf` |
| `Fuel` | Proportion of fuel remaining | `0` to `1` |
| `AngleOfAttack` | Angle of attack (degrees) | `-180` to `180` |
| `AngleOfSlip` | Angle of slip (degrees) | `-180` to `180` |
| `PitchAngle` | Pitch angle from horizontal (degrees) | `-90` to `90` |
| `RollAngle` | Roll angle from horizontal (degrees) | `-180` to `180` |
| `PitchRate` | Rate at which the craft rotates about its x-axis (deg/s) | `-inf` to `inf` |
| `RollRate` | Rate at which the craft rotates about its z-axis (deg/s) | `-inf` to `inf` |
| `YawRate` | Rate at which the craft rotates about its y-axis (deg/s) | `-inf` to `inf` |
| `Heading` | Aircraft heading (degrees) | `-180` to `180` |
| `Latitude` | y-position of the craft in the world | `-inf` to `inf` |
| `Longitude` | x-position of the craft in the world | `-inf` to `inf` |
| `Time` | Time elapsed since craft was loaded (seconds) | `0` to `inf` |
| `GForce` | Omnidirectional "force" on the pilot (g) | `0` to `inf` |
| `VerticalG` | Vertical component of `GForce` (g) | `0` to `inf` |

</details>

<details>
<summary>

### Target State (relative to player craft)
</summary>

| Name | Description | Range |
|:---:|:---:|:---:|
| `TargetHeading` | Global heading to selected target (degrees) | `0` to `360` |
| `TargetElevation` | Target elevation angle above/below horizon (degrees) | `-90` to `90` |
| `TargetDistance` | Line-of-sight distance to selected target (meters) | `0` to `inf` |

</details>

## Built-in Variables
These are available for every craft, and their values 
* **Examples**: `Pitch`, `Altitude`, `GForce`, `TargetDistance`.

## Custom Variables
These are created by the user to perform specific tasks.
* **Variable Setters**: Global variables created in the designer menu.
* **Part Variables**: Specific data points from named parts (e.g., `MyEngine.RPM`).

# Data in Funky Trees
#### Understanding how the language handles different types of information.
---

There are four types of variables in Funky Trees: numbers, booleans, binary variables, and strings.

## Numbers
Numbers are by far the most common variable type. Some are restricted to a certain range, but can be any decimal value within that range; others are fully unrestricted. Number variables are the primary method of incorporating flight control inputs and craft state information into Funky Trees expressions.



## Booleans
Booleans represent "true" or "false" states. In Funky Trees, these are often treated as `1` (true) and `-1` (false), though some logical operators specifically look for non-zero values. Activation Groups and triggers like `FireGuns` are the most common sources of Boolean data.

## Binary

**This is a deprecated variable type, and has been replaced by booleans.** Variables of the binary type output either `0` or `1` depending on the state of the variable's input. Most binary variables were converted to the boolean type for consistency, but `LandingGear` persists as a binary variable to ensure legacy compatibility.

| Name | Description | Range |
|:---:|:---:|:---:|
| `LandingGear` | Landing gear toggle input | `0`, `1`|
> Although it is technically deprecated, `LandingGear` can still be used as an alternative to the boolean `GearDown` in some cases.  Note, however, that `LandingGear` behaves opposite to `GearDown` and becomes `1` when the landing gear is *retracted*, whereas `GearDown` becomes `True`/`1` when the landing gear is *extended*.
