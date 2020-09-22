---
title: "Device"
slug: "device"
excerpt: "Manage your FarmBot's settings: [my.farm.bot/app/device](https://my.farm.bot/app/device)"
---

* toc
{:toc}

Widgets on this page:
 * [Device](#section-device-widget)
 * [Connectivity](#section-connectivity-widget)
 * [Hardware](#section-hardware-widget)
 * [Pin Bindings](#section-pin-bindings-widget)

<div class="nav-image">
  <img class="nav-image" src="device_page.png" alt="Device" />
  <a href="#section-device-widget" style="top: 9.14%; left: 2.32%; width: 46.47%; height: 49.01%;"></a>
  <a href="#section-connectivity-widget" style="top: 61.33%; left: 2.37%; width: 46.47%; height: 37.54%;"></a>
  <a href="#section-hardware-widget" style="top: 9.21%; left: 51.32%; width: 46.31%; height: 27.55%;"></a>
  <a href="#section-pin-bindings-widget" style="top: 39.80%; left: 51.32%; width: 46.36%; height: 19.55%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>



<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2Fvideoseries%3Flist%3DPLMhsMRlKjcNIYlDKDdKvPQuHqBjjS1ZGc&url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D3pJeOXuOUbg&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2F3pJeOXuOUbg%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allowfullscreen></iframe>



# Device Widget



![device_widget.png](device_widget.png)

## Name
Give your device a name

## Time Zone
Set the device's timezone

## Last Seen
View when FarmBot was last connected to the cloud. Refresh the time by pressing the <span class="fa fa-refresh"></span> icon.

## FarmBot OS
View the FarmBot OS version, release notes, and update

## FarmBot OS auto update
Enable FarmBot OS auto-update

## Auto sync
Option to enable auto-syncing between the Web App (cloud) and FarmBot OS, instead of choosing when to manually sync data. This feature is useful for getting small stable changes to FarmBot quickly, but it is recommended to use manual sync when making large changes that are not yet ready to be executed by FarmBot.

## Camera
Select the type of camera you are using in the camera selection dropdown. Choices are `USB Camera` and `Raspberry Pi Camera`. Defaults to `USB camera`. Test by using the `Take Photo` button in the [Take Photo](doc:farmware#section-take-photo) widget.

## Firmware
Select firmware board type: `Arduino/RAMPS (Genesis v1.2)` or `Farmduino (Genesis v1.3)`

## Restart FarmBot
This will restart FarmBot's Raspberry Pi and FarmBot OS.

## Shutdown FarmBot
This will shutdown FarmBot's Raspberry Pi. To turn it back on, unplug FarmBot and plug it back in.

## Factory Reset
Factory resetting your FarmBot will destroy all data on the device, revoking your FarmBot's abilily to connect to your web app account and your home wifi. Upon factory resetting, your device will restart into Configurator mode. Factory resetting your FarmBot will not affect any data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account.

## Automatic factory reset

Automatically factory reset when the WiFi network cannot be detected. Useful for network changes. Disable this setting to allow FarmBot to wait indefinitely for the configured WiFi network to come back online if it disconnects.

## Connection attempt period
For use with automatic factory reset: set the time in minutes to attempt connecting to WiFi before a factory reset.

# Connectivity widget



![connectivity_widget.png](connectivity_widget.png)

Shows connection information. If a connection goes offline, the relevant link will turn red and a diagnosis message will display.

# Hardware widget



![hardware_widget.png](hardware_widget.png)



{%
include callout.html
type="info"
title="Settings"
content="Press the `+` (for example, in `Motors [+]`) to expand the settings section."
%}

## Homing and Calibration

![calibration.png](calibration.png)

### Homing
Homing an axis instructs FarmBot to find the home (minimum) position by moving towards home until an endstop or encoder signals that the end of the axis has been reached. Homing can only be performed if endstops or encoders are enabled. See [Calibration and Homing](../Extras/calibration-and-homing.md) for further details.

{%
include callout.html
type="info"
title="\"Homing\" is different than \"Going to Home\""
content="Homing is the act of _finding_ the home (zero) position by using endstops or encoders. _Going to Home_ is the act of moving to (0, 0, 0). The button on the Controls widget with the home icon instructs FarmBot to _Go to Home_."
%}


### Calibration
Calibrating an axis instructs FarmBot to find the minimum (home) position, then find the maximum position, and also measure the distance between the two positions, which is the length of the axis. Calibration can only be performed if either endstops or encoders are enabled. See [Calibration and Homing](../Extras/calibration-and-homing.md) for further details.

{%
include callout.html
type="info"
title="Coming soon"
content="We're going to switch the order in which calibration is done so that FarmBot first moves to the maximum point, and then to the minimum (home) position. That way your FarmBot is homed and ready to rumble when calibration is completed."
%}



{%
include callout.html
type="info"
title="Calibration speed"
content="Calibration speed is currently determined by the **HOMING SPEED** setting."
%}


### Set zero position
Pressing the <span class="fb-button fb-yellow">Zero X</span>, <span class="fb-button fb-yellow">Zero Y</span>, and <span class="fb-button fb-yellow">Zero Z</span> buttons allows you to *manually* set FarmBot's current location as zero for that axis. This is used for *manually* setting the Home position (0, 0, 0) when you do not have endstops or encoders enabled.

However, because stock FarmBots have encoders, it is recommended to instead use the [Homing](#section-homing) function for *automatically* finding the Home position of each axis and setting that position to zero.

So in general, the Set Zero buttons should not be regularly used because it does not make sense to change your zero position once you have your garden growing, and because all FarmBots should have either encoders or endstops enabled which allows for automatically finding and setting the Home position.

These buttons may come in handy though when playing around with experimental sequences or exploring alternate coordinate system configurations for your FarmBot.

### Find home on boot
Enabling this setting will run a homing command for each axis upon boot. This is most useful for allowing FarmBot to recover and resume operations after a power outage. Note that this requires encoders or endstops to be enabled.

### Stop at Home
Enabling software limits for an axis will prevent FarmBot from moving through zero. For example, if an axis is normally moving in positive coordinates, then the software limit will prevent it from moving through zero into negative coordinates. If an axis has **NEGATIVE COORDINATES ONLY** enabled, then it normally moves in negative coordinates and the software limit will prevent it from moving through zero into positive coordinates.

{%
include callout.html
type="success"
title="Recommended"
content="We recommend turning software limits on for all axes so that FarmBot will never try to move through the home (0, 0, 0) position."
%}

### Stop at Max
If values are inputted using the **Length** setting, FarmBot will stop at the axis maximum.

### Negative coordinates only
This setting will allow movements to only occur in negative coordinates for the chosen axis. This is most useful for the z-axis if you want your home position to be at the highest point and for FarmBot to move down into negative coordinates.

### Length
With these inputs you can manually specify the length in mm of each axis. This is useful if you want to limit your FarmBot's movements along an axis with software rather than a physical hardware stop such as a belt clip or an endstop. For example: you may occasionally want to prevent movements at the far end of your garden because you put a seasonal garden gnome there, but you don't want to adjust the belts and belt clips. You must enable **Stop at Max** for FarmBot to stop at the values inputted.

{%
include callout.html
type="info"
title="Reminder:"
content="The length values of each axis are measured and auto-filled whenever your use the [Calibration](#section-calibration) function."
%}


### Timeout after
This is the amount of time in seconds that the firmware will wait until a movement command times out, or stops executing. The default value for each axis is 120 seconds.

{%
include callout.html
type="warning"
title="Use reasonable timeout values"
content="Do not set the timeout times to extremely high values (such as 20,000 seconds). Under certain circumstances, such as when endstops and encoders are disabled and you send an extremely long movement command, this could cause your FarmBot to stall at the end of an axis for a very long time, requiring an e-stop or system reboot."
%}


## Motors

![motors.png](motors.png)

### Max retries
The number of times that FarmBot will try to move to a position before stopping and reporting that the movement has failed.

### E-Stop on movement error
Emergency stop if movement is not complete after the maximum number of retries. If enabled and the retries are exhausted, you will need to unlock the device by pressing the <span class="fb-button fb-yellow">UNLOCK</span> button in the main navbar.

### Max speed
This setting controls the maximum speed in motor steps per second that FarmBot will reach after accelerating.

We recommend using a value between 200 and 1,000 steps/s for each axis. Start with a slower speed and work your way up as you become more comfortable operating your FarmBot. If your FarmBot begins to stutter or stall at higher speeds, reduce the max speed. To achieve higher speeds you may need to adjust some of your hardware, tune your stepper drivers, and/or adjust some additional software parameters such as **ACCELERATE FOR**. Remember though that FarmBot has 24 hours in the day to complete its tasks, so moving rapidly is not necessary.

{%
include callout.html
type="info"
title="Convert Motor Speed into Linear Speed with the following equations"
content="For belt-driven axes (X and Y)
**Linear Speed** = **Motor Speed** / **Motor Resolution** x **Microstepping** x **Pulley Size** x **Belt Pitch**

For leadscrew-driven axes (Z)
**Linear Speed** = **Motor Speed** / **Motor Resolution** x **Microstepping** x **Leadscrew Lead**

For stock FarmBot kits,
**Motor Resolution** = 200 steps/revolution
**Microstepping** = 1 (full steps)
**Pulley Size** = 20 teeth/revolution
**Belt Pitch** = 2mm/tooth
**Leadscrew Lead** = 8mm/revolution

For a Motor Speed of 500 steps/second on the stock belt-driven (X and Y) axes, the equation works out to:
**Linear Speed (mm/second)** = 500 / 200 x 1 x 20 x 2 = **100 mm/s**

For a Motor Speed of 500 steps/second on the stock leadscrew-driven (Z) axis:
**Linear Speed (mm/second)** = 500 / 200 x 1 x 8 = **20 mm/s**"
%}

### Homing speed
This setting controls the speed in steps per second at which FarmBot will move for coordinates past home during homing and calibration. The recommended default value for each axis is 50 steps/s.

### Minimum speed
This setting controls the minimum speed in steps per second that FarmBot will move. The recommended default value for each axis is 50 steps/s.

### Accelerate for
This setting controls the number of steps used for the acceleration and deceleration periods of each movement. The recommended default value for each axis is 500 steps. If your FarmBot stutters or stalls during acceleration, you should increase the value of **ACCELERATE FOR** so that FarmBot uses more steps to accelerate and decelerate.

### Steps per mm
This setting tells FarmBot how many motor steps it takes to move 1mm along an axis. The default value is 5 steps/mm for the belt-driven (X and Y) axes, and 25 steps/mm for the leadscrew-driven (Z) axis.

{%
include callout.html
type="info"
title="Steps per mm is calculated with the following equations"
content="For belt-driven axes (X and Y)
**Steps per mm** = **Motor Resolution** x **Microstepping** / **Pulley Size** / **Belt Pitch**

For leadscrew-driven axes (Z)
**Linear Distance** = **Motor Resolution** x **Microstepping** / **Leadscrew Lead**

For stock FarmBot kits,
**Motor Resolution** = 200 steps/revolution
**Microstepping** = 1 (full steps)
**Pulley Size** = 20 teeth/revolution
**Belt Pitch** = 2mm/tooth
**Leadscrew Lead** = 8mm/revolution

For the stock belt-driven (X and Y) axes, the equation works out to:
**Steps per mm** = 200 x 1 / 20 / 2 = **5 steps/mm**

For the stock leadscrew-driven (Z) axis:
**Steps per mm** = 200 x 1 / 8 = **25 steps/mm**"
%}


### Always power motors
Enabling this setting will keep power applied to the motors at all times. This is most useful to prevent the z-axis from slipping down due to the force of gravity when FarmBot is idle. It can also be used to help prevent animals or children from moving one of FarmBot's axes when it is idle.

### Invert motors
This inverts the direction that the motors move for the chosen axis. Changing this setting will usually require you to change the setting of **INVERT ENCODERS** as well. You also might need to use this setting in combination with **INVERT ENDPOINTS** and **NEGATIVE COORDINATES ONLY** to set your FarmBot coordinate system exactly how you want it.

### Enable second x-axis motor
This should be enabled for standard FarmBots that use two motors to drive the x-axis (gantry).

### Invert the second x-axis motor
This setting changes the direction of the second x-axis motor in case you wired it backwards.

## Encoders and Endstops

![encoders.png](encoders.png)

### Enable encoders
Stock FarmBot kits have rotary encoders built-in. The rotary encoders should be enabled by using these toggles. If you are experiencing troubles with your movements you might try to disable encoders for testing purposes. If you do not have encoders hooked up, you must have encoders disabled here otherwise your FarmBot will think it is stalling with every movement. Note that Homing and Calibration can only be used if encoders (or endstops) are enabled. See [Rotary Encoders](../Extras/rotary-encoders.md) for more information.

### Use encoders for positioning
(Alpha) Use the encoders for calculating movements in addition to using encoders for stall detection.

### Invert encoders
This setting will reverse the direction of encoder position reading. This can be used as a software fix in the event that you wired up an encoder or motor backwards, which causes FarmBot to think it is stalling with every movement because the encoder appears to be going the opposite direction of the motor. This setting is also used in combination with **INVERT MOTOR** if you want to invert a motor's movements using software.

### Max missed steps
Rotary encoders allow your FarmBot to know when an axis has stalled either due to the FarmBot reaching its physical end point or if it hits an obstruction such as a vine, toolbay, or your hand.

The Max Missed Steps setting tells your FarmBot how many motor steps it needs to miss (as determined by the encoder feedback) before the motor is considered to have become stalled. A lower value will allow your FarmBot to stop the motors sooner when it stalls, which is desirable. However, setting the value too low could cause false alarms where FarmBot thinks it is stuck on something even though it is not.

The default value for Max Missed Steps is 5 for each axis. While we have seen successful results with values as low as 2, 1, and the fabled 0, we recommend starting with 10 and slowly bringing the values down. If you start to see false stall alarms (where FarmBot thinks it is stuck on something but it isn't) then increase the value until there are no false alarms.

### Encoder missed step decay
While moving FarmBot at high speeds (greater than 400 steps/s), FarmBot may not detect every single encoder pulse due to limitations in the clock speed of the Arduino and the speed at which the encoders can be read. Because FarmBot counts the undetected encoder pulses as missed steps, the total number of missed steps can add up over long movements and cause a false stall alarm, even if no steps were actually missed.

The Encoder Missed Step Decay value accounts for this shortcoming of the Arduino when moving FarmBot at high speeds. It works by reducing (decaying) the total count of missed steps by the Encoder Missed Step Decay value every time there is an encoder pulse detected. This allows FarmBot to dismiss the periodic encoder pulses that go undetected (and the corresponding false missed steps) and therefore prevent false stall alarms.

Meanwhile, if the motor does stall, then a bunch of missed steps will happen consecutively without any encoder pulses detected in between. Because no encoder pulses are detected, the total count of missed steps will not decay, and so the motor will be considered stalled once the Max Missed Steps value is reached.

The default Encoder Missed Step Decay value for each axis is 5. Changing this value is only necessary if you are using much higher resolution encoders and/or a slower processor and/or driving FarmBot at very high speeds (greater than 2,000 steps/s), all of which would cause more encoder pulses to go undetected.

{%
include callout.html
type="success"
title="Better electronics coming soon"
content="In future versions of FarmBot electronics we will implement dedicated chips for reading the encoder pulses at a much higher frequency so that FarmBot will be able to detect every single encoder pulse no matter the motor speed."
%}

### Encoder scaling
The encoder scaling factor is used to match the encoder resolution with the motor resolution. The rotary encoders included with the stock FarmBots are 360 line/revolution. The stock motors are 200 step/revolution and used with full-step microstepping (a value of 1 in the equation below). For more information on microstepping, see [Microstepping](../FarmBot OS/arduino-firmware/microstepping.md).

The encoder scaling factor is calculated as follows, and rounded to the nearest integer.
Encoder scaling = 10000 x motor resolution x microsteps / encoder resolution
Encoder scaling = 10000 x 200 x 1 / 360 = 5556.

### Enable endstops
If using endstops instead of rotary encoders, enable them here. If you do not have endstops hooked up, do not enable this setting.

### Swap endstops
This switches the zero end of an axis to the other end of the axis. This allows you to set your home (0, 0, 0) position to any of the eight corners of FarmBot's working volume. You might need to use this setting in combination with **INVERT MOTORS**, **INVERT ENCODERS**, and **NEGATIVE COORDINATES ONLY** to set your FarmBot coordinate system exactly how you want it.

### Invert endstops
This switches endstop operation from normally open (NC) to normally closed (NC).

## Danger Zone

![reset.png](reset.png)

### Reset Hardware Parameter Defaults
This will restore all settings to their default values, as shown in the table below.

|Homing and Calibration Parameter|Default Value                 |
|------------------------------|------------------------------|
|Find Home on Boot             |No (cannot be changed unless encoders or endstops are enabled)
|Stop at Home                  |No
|Stop at Max                   |No
|Negative Coordinates Only     |No for `X`, and `Y` axes. Yes for `Z`
|Axis Length (steps)           |0 (undefined)



|Motor Parameter               |Default Value                 |
|------------------------------|------------------------------|
|Max Retries                   |3
|E-stop on Movement Error      |No
|Max Speed (steps/s)           |400
|Homing Speed (steps/s)        |50
|Minimum Speed (steps/s)       |50
|Accelerate For (steps)        |300
|Steps per mm                  |5 for `X` and `Y` axes, 25 for `Z`
|Always Power Motors           |No for `X` and `Y` axes, Yes for `Z`
|Invert Motors                 |No
|Enable 2nd X Motor            |Yes
|Invert 2nd X Motor            |Yes



|Encoders and Endstops Parameter|Default Value                 |
|------------------------------|------------------------------|
|Enable Encoders               |No
|Use Encoders for Positioning  |No
|Invert Encoders               |No
|Max Missed Steps              |5
|Encoder Missed Step Decay     |5
|Encoder Scaling               |5556
|Enable Endstops               |No
|Invert Endstops               |No

All Pin Guard settings will be set to Pin 0, 60 seconds, Low.

# Pin Bindings Widget



{%
include callout.html
type="warning"
title="Warning"
content="Binding to a pin without a physical button and pull-down resistor connected may put FarmBot into an unstable state."
%}



![pin_bindings.png](pin_bindings.png)

_v1.4 stock bindings shown_

Set or remove Raspberry Pi GPIO pin bindings to allow start of a sequence or an action by pressing a physical button (or by motion sensor output).

Select a Raspberry Pi GPIO pin number (open the GPIO diagram for assistance as shown below by pressing the <span class="fa fa-th-large"></span> icon) and select a sequence in the drop down menu.

![pin_bindings_gpio.png](pin_bindings_gpio.png)

Alternatively, select an action:

![pin_bindings_action.png](pin_bindings_action.png)

When done press <span class="fb-button fb-green">BIND</span> to save the binding.

**Notes:**
 * Sequences must be synced to the device before use in a pin binding.
 * Buttons should be connected between the selected pin and +3.3v.
