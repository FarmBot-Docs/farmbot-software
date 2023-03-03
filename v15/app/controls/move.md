---
title: "Move"
slug: "move"
description: "Manually move your FarmBot <i class='fa fa-arrows'></i>\n[Open this panel in the app](https://my.farm.bot/app/designer/controls)"
---

The controls at the top of the panel allow you to view FarmBot's current position, manually move it in real-time, take photos, go to home or find home, and shutdown or reboot FarmBot.

![move controls panel](_images/move_controls_panel.png)

# Viewing the current position

The **CURRENT POSITION (MM)** of your FarmBot is shown in the gray fields directly below the **X AXIS**, **Y AXIS**, and **Z AXIS** labels. This information is updated in real-time.

If your FarmBot has encoders (Genesis kits only), you can also view **SCALED ENCODER (MM)** data, as well as **RAW ENCODER DATA** for each axis. Toggle the display of this additional information from the (cog) menu in the top right of the panel.

![current position display](_images/current_position_display.png)

# Movements

There are four types of movements you can perform in this panel: **relative movements**, **absolute movements**, **finding home**, and **going to home**.

## Relative movements

Move FarmBot a **relative distance** from the current location in any direction by using the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-down'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-up'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-right'></i></span> arrow buttons. The default **MOVE AMOUNT (MM)** is `100`, though you can also select `1`, `10`, `1000`, and `10000` amounts.

Depending on your [hardware settings](../settings.md), you may not be able to move beyond an axis minimum or maximum. When this is true, some arrow buttons may be disabled.

In the example below, because FarmBot is at the home position `(0, 0, 0)`, half of the arrow buttons are disabled to allow only movements *away* from the home position and not *through* it. Clicking a disabled button displays a popup indicating why the button is disabled.

![jog buttons](_images/jog_buttons.png)

### Matching the virtual controls to your real-life perspective

Depending on how you usually view your FarmBot, you may need to change which direction each arrow button sends your FarmBot so that the virtual controls match your real-life perspective. For example, if you usually view your FarmBot from the front (looking at the FarmBot logo on the tool head), you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative Y` direction. If you usually view your FarmBot from the side with the electronics box, you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative X` direction.

You can change the direction along each axis that the arrow buttons send your FarmBot by using the Invert Jog Button toggles in the (cog) menu in the top right of the panel. You can also swap the X and Y axis buttons, which will also rotate the map in the farm designer by 90 degrees.

![move settings menu](_images/move_settings_menu.png)

## Absolute movements

Move FarmBot to an **absolute position** by typing in new coordinates to the white input fields for the **X AXIS**, **Y AXIS**, and **Z AXIS** and then pressing <span class="fb-button fb-green">GO</span>.

{%
include callout.html
type="info"
title=""
content="FarmBot will operate all axes at once to get to the new position as fast as possible."
%}

![absolute movements](_images/absolute_movements.png)

If you do not type in a new value for any of the axes, then FarmBot will maintain its current position along that axis and only move the needed axis or axes.

## Finding home

The <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button with a <i class='fa fa-search'></i> icon will instruct FarmBot to **find the home position** for all axes in the order Z, Y, X.

{%
include callout.html
type="info"
title=""
content="FarmBot must have [home-finding hardware](../settings/stall-detection.md) such as encoders, stall-detecting stepper drivers, or limit switches in order to automatically find the home position."
%}

## Going to home

The <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button with a <i class='fa fa-arrow-left'></i> icon will instruct FarmBot to **go to the home position** for all axes as though you had typed in `(0, 0, 0)` to the move absolute input fields. Note that the _go to home_ behavior will move all three axes at once.

# Taking photos

The <span class="fb-button fb-gray"><i class='fa fa-camera'></i></span> button will take a photo at FarmBot's current location and provide progress updates of the capture and upload process in realtime. Photos can be viewed in the [photos panel](../photos.md).

![take photo progress](_images/take_photo_progress.gif)

# Other axis controls

In addition to the axis input fields, there are controls to <span class="fb-button fb-yellow">MOVE TO HOME</span>, <span class="fb-button fb-yellow">FIND HOME</span>, <span class="fb-button fb-yellow">SET HOME</span>, and <span class="fb-button fb-yellow">FIND LENGTH</span> for an individual axis located in the <i class='fa fa-ellipsis-v'></i> popups.

![other axis controls](_images/other_axis_controls.png)

# Motor load

View the latest, recent maximum, and recent average **MOTOR LOAD** for each each axis by clicking the load indicator bars below each axis label.

{%
include callout.html
type="info"
title=""
content="Motor load indicators are only available for FarmBot Express bots with **[STALL DETECTION](../settings/stall-detection.md)** enabled."
%}

![motor load](_images/motor_load.png)

# Motor position plot

To view a graph of motor positions over time, toggle <span class="fb-peripheral-on">ON</span> the motor position plot in the (cog) menu of the panel.

![motor position plot](_images/motor_position_plot.png)

# Power button

The <span class="fb-button fb-gray"><i class='fa fa-power-off'></i></span> button shows a popup with options to <span class="fb-button fb-yellow">RESTART</span>, <span class="fb-button fb-red">SHUTDOWN</span>, <span class="fb-button fb-red">SOFT RESET</span>, and <span class="fb-button fb-red">HARD RESET</span> FarmBot.

![power button](_images/power_button.png)

## Restart FarmBot

This will restart FarmBot's Raspberry Pi and FarmBot OS.

## Shutdown FarmBot

This will shutdown FarmBot's Raspberry Pi. To turn it back on, unplug FarmBot and plug it back in.

## Soft reset

Soft resetting your FarmBot will revoke your FarmBot's ability to connect to your web app account and your home WiFi network. **This is useful before moving FarmBot to a new location with a different WiFi network, or when switching FarmBot from one web app account to another.**

Upon soft resetting, you will need to [reconfigure FarmBot](http://configure.farm.bot) to connect it to internet and your web app account.

{%
include callout.html
type="success"
title="Your web app data is safe"
content="Soft resetting your FarmBot will not affect any of your data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account."
%}

{%
include callout.html
type="info"
title=""
content="If you are experiencing problems with your setup, we do not recommend performing a soft reset. Instead, perform a [hard reset](#hard-reset)."
%}

## Hard reset

Hard resetting your FarmBot will erase all data from the device, allowing you to start from a clean slate. **This is recommended if you are experiencing problems with your setup.**

Perform a hard reset by [reflashing the latest version of FarmBot OS onto the microSD card](../../farmbot-os/intro.md). Upon hard resetting, you will need to [reconfigure FarmBot](http://configure.farm.bot) to connect it to internet and your web app account.

{%
include callout.html
type="success"
title="Your web app data is safe"
content="Hard resetting your FarmBot will not affect any of your data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account."
%}


# What's next?

 * [Peripherals](peripherals.md)
