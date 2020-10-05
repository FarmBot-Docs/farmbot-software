---
title: "Move"
slug: "move"
description: "Manually move your FarmBot <i class='fa fa-arrows'></i>\n[Open this panel in the app](https://my.farm.bot/app/designer/controls)"
---

* toc
{:toc}

The controls at the top of the panel allow you to view FarmBot's current position, manually move it in real-time, take photos, and go to home or find home.

![Screen Shot 2020-06-30 at 10.51.06 AM.png](_images/Screen_Shot_2020-06-30_at_10.51.06_AM.png)

# Viewing the current position
The current position of your FarmBot (**MOTOR COORDINATES (MM)**) is shown in the gray fields directly below the **X-AXIS**, **Y-AXIS**, and **Z-AXIS** labels. This information is updated in real-time.

If your FarmBot has encoders (Genesis kits only), you can also view **SCALED ENCODER (MM)** data, as well as **RAW ENCODER DATA** for each axis. Toggle the display of this additional information from the <i class='fa fa-gear'></i> menu in the top right of the panel.

![Screen Shot 2019-05-06 at 3.20.00 PM.png](_images/Screen_Shot_2019-05-06_at_3.20.00_PM.png)

# Movements
There are three types of movements you can perform in this panel: **relative movements**, **absolute movements**, and **finding home**.

## Relative movements
Move FarmBot a **relative distance** from the current location in any direction by using the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-down'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-up'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-right'></i></span> arrow buttons. The default **MOVE AMOUNT** is `100mm`, though you can also select `1`, `10`, `1000`, and `10000mm` amounts.

Depending on your [hardware settings](../../The-FarmBot-Web-App/settings.md), you may not be able to move to negative coordinates or past the specified axis maximums. When this is true, some arrow buttons may be disabled. In the example below, because FarmBot is at the home position (0, 0, 0), half of the arrow buttons are disabled to allow only movements *away* from the home position and not *through* it.

![Screen Shot 2019-05-06 at 3.29.57 PM.png](_images/Screen_Shot_2019-05-06_at_3.29.57_PM.png)

### Matching the virtual controls to your real-life perspective
Depending on how you usually view your FarmBot, you may need to change which direction each arrow button sends your FarmBot so that the virtual controls match your real-life perspective. For example, if you usually view your FarmBot from the front (looking at the FarmBot logo on the tool head), you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative Y` direction. If you usually view your FarmBot from the side with the electronics box, you would want the <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> button to send FarmBot in the `negative X` direction.

You can change the direction along each axis that the arrow buttons send your FarmBot by using the Invert Jog Button toggles in the <i class='fa fa-gear'></i> menu in the top right of the panel. You can also swap the X and Y axis buttons, which will also rotate the map in the farm designer by 90 degrees.

![Screen Shot 2020-06-30 at 11.18.21 AM.png](_images/Screen_Shot_2020-06-30_at_11.18.21_AM.png)

### Sequence based relative movements
You can also perform relative movements from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-move-relative">Move Relative</span> command. For more information, see the [move relative command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#move-relative).

## Absolute movements
Move FarmBot to an **absolute position** by typing in new coordinates to the white input fields for the **X-AXIS**, **Y-AXIS**, and **Z-AXIS** and then pressing <span class="fb-button fb-green">GO</span>.

{%
include callout.html
type="info"
title=""
content="FarmBot will operate all axes at once to get to the new position as fast as possible."
%}



![Screen Shot 2019-05-06 at 4.00.10 PM.png](_images/Screen_Shot_2019-05-06_at_4.00.10_PM.png)

If you do not type in a new value for any of the axes, then FarmBot will maintain its current position along that axis and only move the needed axis or axes.

### Sequence based absolute movements
You can also perform absolute movements from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-move-absolute">Move To</span> command. For more information, see the [move to command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#move-to).

## Finding home
The <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button will instruct FarmBot to **automatically find the home position** for all axes in the order Z, Y, X.

{%
include callout.html
type="info"
title=""
content="FarmBot must have [home-finding hardware](../../FarmBot-OS/arduino-firmware/stall-detection.md) such as encoders, stall-detecting stepper drivers, or limit switches in order to automatically find the home position."
%}

If you do not have home-finding hardware, you can change the behavior of the <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button to instead instruct FarmBot to **go to the home position**. This will instruct FarmBot to go to `(0, 0, 0)` as though you had used the move absolute input fields. Change the home button behavior by setting the **PERFORM HOMING (FIND HOME)** setting to <span class="fb-peripheral-off">OFF</span> in the <i class='fa fa-gear'></i> menu of the panel. Note that the _go to home_ behavior will move all three axes at once.

### Sequence based homing
You can also perform homing from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-find-home">Find Home</span> command. For more information, see the [find home command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#find-home).

## Motor position plot
To view a graph of motor positions over time, toggle <span class="fb-peripheral-on">ON</span> the motor position plot in the <i class='fa fa-gear'></i> menu of the panel.

![Screen Shot 2020-06-30 at 11.53.25 AM.png](_images/Screen_Shot_2020-06-30_at_11.53.25_AM.png)

# Other controls

## Take photo
The <span class="fb-button fb-gray"><i class='fa fa-camera'></i></span> button will take a photo at FarmBot's current location. Photos can be viewed in the [photos panel](../../The-FarmBot-Web-App/photos.md).

### Sequence based photo taking
You can also take photos from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-wait">Take Photo</span> command. For more information, see the [take photo command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#take-photo).

# What's next?

 * [Peripherals](../controls/peripherals.md)
