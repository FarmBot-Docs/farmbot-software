---
title: "Motors"
slug: "motors"
description: ":zap: Adjust motor speed, acceleration, and power.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=motors)"
---


# Max speed

This setting controls the **MAX SPEED** in millimeters per second that FarmBot will reach after accelerating.

We recommend starting with the default values shown in the <i class='fa fa-question-circle'></i> popup, which are dependent on your FarmBot model and the axis. If tuning is necessary or desired, make small adjustments (+/- 10%) and test the new values each time before making further adjustments.

{%
include callout.html
type="arrows-v"
content="For the Z-axis, you can also set the **MAX SPEED TOWARD HOME** independently from the max speed travelling away from the home position. This is especially useful for the Z-axis because the motor will either be fighting against or working with gravity depending on the direction of movement."
%}

{%
include callout.html
type="info"
title="Using non-standard hardware"
content="The arduino firmware automatically calculates a **Motor Speed** (in steps/s) from your desired **Linear Speed** (in mm/s) and the specs of the stock FarmBot hardware. If you wish to use non-standard hardware (for example, a different leadscrew), refer to the [kinematic equations page](../..//farmbot-os/arduino-firmware/kinematic-equations.md#convert-motor-speed-into-linear-speed)."
%}

# Minimum speed

This setting controls the **MINIMUM SPEED** in millimeters per second that FarmBot will move.

{%
include callout.html
type="arrows-v"
content="For the Z-axis, you can also set the **MINIMUM SPEED TOWARD HOME** independently from the minimum speed travelling away from the home position. This is especially useful for the Z-axis because the motor will either be fighting against or working with gravity depending on the direction of movement."
%}

# Accelerate for

This setting controls the distance in millimeters that FarmBot will **ACCELERATE FOR** during each movement (as well as decelerate for).

We recommend starting with the default values shown in the <i class='fa fa-question-circle'></i> popup, which are dependent on your FarmBot model and the axis. If tuning is necessary or desired, make small adjustments (+/- 10%) and test the new values each time before making further adjustments.

{%
include callout.html
type="arrows-v"
content="For the Z-axis, you can also set the **ACCELERATE FOR TOWARD HOME** independently from the accleration for travelling away from the home position. This is especially useful for the Z-axis because the motor will either be fighting against or working with gravity depending on the direction of movement."
%}

# Always power motors

Enabling this setting will keep power applied to the motors at all times. This is most useful to prevent the z-axis from slipping down due to the force of gravity when FarmBot is idle. It can also be used to help prevent animals or children from moving one of FarmBot's axes when it is idle.

# Invert motors

This inverts the direction that the motors move for the chosen axis. Changing this setting will usually require you to change the setting of **INVERT ENCODERS** as well. You also might need to use this setting in combination with **INVERT ENDPOINTS** and **NEGATIVE COORDINATES ONLY** to set your FarmBot coordinate system exactly how you want it.

# Motor current

Motor current in milliamps. (Only available for Genesis v1.5+ and Express v1.0+ kits)

# Advanced settings

{%
include callout.html
type="info"
content="These [advanced settings](../settings/parameter-management.md#show-advanced-settings) are not shown by default."
%}

## Steps per mm

This setting tells FarmBot how many motor steps it takes to move 1mm along an axis. The default values may be changed for custom setups. Refer to the [kinematic equations page](../..//farmbot-os/arduino-firmware/kinematic-equations.md#calculate-steps-per-mm) for additional information.

## Homing speed

This setting controls the speed in millimeters per second at which FarmBot will move for coordinates past home during homing and calibration.

## Quiet mode

Toggles to enable or disable quiet motor operation. Note that quiet mode is only available for Genesis v1.5+ and Express v1.0+ kits featuring Trinamic TMC2130 stepper drivers. Quiet mode is enabled by default for new FarmBot accounts as of July, 2021.

## Enable 2nd X motor

This should be enabled for standard FarmBots that use two motors to drive the x-axis (gantry).

## Invert 2nd X motor

This setting changes the direction of the second x-axis motor in case it is wired backwards.
