---
title: "Move"
slug: "move"
description: "Manually move your FarmBot <i class='fa fa-arrows'></i>\n[Open this panel in the app](https://my.farm.bot/app/designer/controls)"
---

The controls at the top of the panel allow you to view FarmBot's current position, manually move it in real-time, take photos, and go to home or find home.

![move controls panel](_images/move_controls_panel.png)

# Viewing the current position

The current position of your FarmBot (**MOTOR COORDINATES (MM)**) is shown in the gray fields directly below the **X-AXIS**, **Y-AXIS**, and **Z-AXIS** labels. This information is updated in real-time.

If your FarmBot has encoders (Genesis kits only), you can also view **SCALED ENCODER (MM)** data, as well as **RAW ENCODER DATA** for each axis. Toggle the display of this additional information from the (cog) menu in the top right of the panel.

![current position display](_images/current_position_display.png)

# Movements

There are three types of movements you can perform in this panel: **relative movements**, **absolute movements**, and **finding home**.

## Relative movements

Move FarmBot a **relative distance** from the current location in any direction by using the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-down'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-up'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-right'></i></span> arrow buttons. The default **MOVE AMOUNT** is `100mm`, though you can also select `1`, `10`, `1000`, and `10000mm` amounts.

Depending on your [hardware settings](../settings.md), you may not be able to move to negative coordinates or past the specified axis maximums. When this is true, some arrow buttons may be disabled. In the example below, because FarmBot is at the home position (0, 0, 0), half of the arrow buttons are disabled to allow only movements *away* from the home position and not *through* it.

![jog buttons](_images/jog_buttons.png)

### Matching the virtual controls to your real-life perspective

Depending on how you usually view your FarmBot, you may need to change which direction each arrow button sends your FarmBot so that the virtual controls match your real-life perspective. For example, if you usually view your FarmBot from the front (looking at the FarmBot logo on the tool head), you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative Y` direction. If you usually view your FarmBot from the side with the electronics box, you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative X` direction.

You can change the direction along each axis that the arrow buttons send your FarmBot by using the Invert Jog Button toggles in the (cog) menu in the top right of the panel. You can also swap the X and Y axis buttons, which will also rotate the map in the farm designer by 90 degrees.

![move settings menu](_images/move_settings_menu.png)

### Sequence based relative movements

You can also perform relative movements from [sequences](../sequences.md) by using the <span class="fb-step fb-move">Move</span> command and selecting **offset from current location** in the **LOCATION** dropdown. For more information, see the [move command documentation](../sequences/sequence-commands/movements.md#move).

## Absolute movements

Move FarmBot to an **absolute position** by typing in new coordinates to the white input fields for the **X-AXIS**, **Y-AXIS**, and **Z-AXIS** and then pressing <span class="fb-button fb-green">GO</span>.

{%
include callout.html
type="info"
title=""
content="FarmBot will operate all axes at once to get to the new position as fast as possible."
%}

![absolute movements](_images/absolute_movements.png)

If you do not type in a new value for any of the axes, then FarmBot will maintain its current position along that axis and only move the needed axis or axes.

### Sequence based absolute movements

You can also perform absolute movements from [sequences](../sequences.md) by using the <span class="fb-step fb-move">Move</span> command. For more information, see the [move command documentation](../sequences/sequence-commands/movements.md#move).

## Finding home

The <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button will instruct FarmBot to **automatically find the home position** for all axes in the order Z, Y, X.

{%
include callout.html
type="info"
title=""
content="FarmBot must have [home-finding hardware](../settings/stall-detection.md) such as encoders, stall-detecting stepper drivers, or limit switches in order to automatically find the home position."
%}

If you do not have home-finding hardware, you can change the behavior of the <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button to instead instruct FarmBot to **go to the home position**. This will instruct FarmBot to go to `(0, 0, 0)` as though you had used the move absolute input fields. Change the home button behavior by setting the **PERFORM HOMING (FIND HOME)** setting to <span class="fb-peripheral-off">OFF</span> in the (cog) menu of the panel. Note that the _go to home_ behavior will move all three axes at once.

### Sequence based homing

You can also perform homing from [sequences](../sequences.md) by using the <span class="fb-step fb-find-home">Find Home</span> command. For more information, see the [find home command documentation](../sequences/sequence-commands/movements.md#find-home).

# Taking photos

The <span class="fb-button fb-gray"><i class='fa fa-camera'></i></span> button will take a photo at FarmBot's current location. Photos can be viewed in the [photos panel](../photos.md).

### Sequence based photo taking

You can also take photos from [sequences](../sequences.md) by using the <span class="fb-step fb-take-photo">Take Photo</span> command. For more information, see the [take photo command documentation](../sequences/sequence-commands/image-processing.md#take-photo).

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


# What's next?

 * [Peripherals](peripherals.md)
