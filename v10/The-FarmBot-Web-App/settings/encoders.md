---
title: "Encoders"
slug: "encoders"
description: "[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=encoders)"
---


![Screen Shot 2020-04-22 at 4.57.44 PM.png](_images/Screen_Shot_2020-04-22_at_4.57.44_PM.png)

# Enable encoders
FarmBot Genesis kits have rotary encoders built-in. The rotary encoders should be enabled by using these toggles. If you are experiencing troubles with your movements you might try to disable encoders for testing purposes. If you do not have encoders hooked up, you must have encoders disabled here otherwise your FarmBot will think it is stalling with every movement. Note that Homing and Calibration can only be used if encoders (or endstops) are enabled.

{%
include callout.html
type="info"
title=""
content="See [Rotary Encoders](../../FarmBot-OS/arduino-firmware/stall-detection.md#rotary-encoders) for more information."
%}

# Use encoders for positioning
Use the encoders for calculating movements in addition to using encoders for stall detection.

# Invert encoders
This setting will reverse the direction of encoder position reading. This can be used as a software fix in the event that you wired up an encoder or motor backwards, which causes FarmBot to think it is stalling with every movement because the encoder appears to be going the opposite direction of the motor. This setting is also used in combination with **INVERT MOTOR** if you want to invert a motor's movements using software.

# Max missed steps
Rotary encoders allow your FarmBot to know when an axis has stalled either due to the FarmBot reaching its physical end point or if it hits an obstruction such as a vine, toolbay, or your hand.

The Max Missed Steps setting tells your FarmBot how many motor steps it needs to miss (as determined by the encoder feedback) before the motor is considered to have become stalled. A lower value will allow your FarmBot to stop the motors sooner when it stalls, which is desirable. However, setting the value too low could cause false alarms where FarmBot thinks it is stuck on something even though it is not.

The default value for Max Missed Steps is 5 for each axis. While we have seen successful results with values as low as 2, 1, and the fabled 0, we recommend starting with 10 and slowly bringing the values down. If you start to see false stall alarms (where FarmBot thinks it is stuck on something but it isn't) then increase the value until there are no false alarms.

# Missed step decay
FarmBot Genesis v1.2 and v1.3 utilized the Arduino MEGA 2560 chip to read and process encoder signals. When moving these FarmBots at high speeds (greater than 400 steps/s), it was possible to not detect every single encoder pulse due to limitations in the clock speed of the microprocessor. Because FarmBot counts the undetected encoder pulses as missed steps, the total number of missed steps could add up over long movements and cause a false stall alarm, even if no steps were actually missed.

The Missed Step Decay value accounts for this shortcoming of the Arduino when moving the v1.2 and v1.3 FarmBots at high speeds. It works by reducing (decaying) the total count of missed steps by the Missed Step Decay value every time there is an encoder pulse detected. This allows FarmBot to dismiss the periodic encoder pulses that go undetected (and the corresponding false missed steps) and therefore prevent false stall alarms.

Meanwhile, if the motor does stall, then a bunch of missed steps will happen consecutively without any encoder pulses detected in between. Because no encoder pulses are detected, the total count of missed steps will not decay, and so the motor will be considered stalled once the Max Missed Steps value is reached.

The default Missed Step Decay value for each axis is 5. Changing this value is only necessary if you are using much higher resolution encoders and/or a slower processor and/or driving FarmBot at very high speeds (greater than 2,000 steps/s), all of which would cause more encoder pulses to go undetected.

{%
include callout.html
type="success"
title="Improved with v1.4+"
content="Starting with FarmBot Genesis v1.4, our custom Farmduino boards feature electronics more suited to reading encoder pulses at higher speeds. This allows FarmBot to be able to detect every single encoder pulse no matter the motor speed, within other reasonable hardware limits."
%}

# Encoder scaling
The encoder scaling factor is used to match the encoder resolution with the motor resolution. The rotary encoders included with the stock FarmBots are 360 line/revolution. The stock motors are 200 step/revolution and used with full-step microstepping (a value of 1 in the equation below). For more information on microstepping, see [Microstepping](../../FarmBot-OS/arduino-firmware/microstepping.md).

The encoder scaling factor is calculated as follows, and rounded to the nearest integer.
```
Encoder scaling = 10000 x motor resolution x microsteps / encoder resolution

Encoder scaling = 10000 x 200 x 1 / 360 = 5556
```
