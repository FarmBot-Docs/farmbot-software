---
title: "Farm Designer Settings"
slug: "farm-designer-settings"
description: ":carrot: Customize your Farm Designer experience.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=farm_designer)"
---


# Plant animations

Enable or disable plant animations in the garden map. This may be useful to turn <span class="fb-peripheral-off">OFF</span> when using the app on a lower powered device such as a smartphone or chromebook.

# Virtual FarmBot trail

Display a virtual trail for FarmBot in the garden map to show movement and watering history while the map is open. Toggling this setting will clear data for the current trail.

# FarmBot motor load

Display high motor load warning indicators in the map. Requires **VIRTUAL FARMBOT TRAIL** and **STALL DETECTION** to be enabled.

# Dynamic map size

Set the garden map size based on the **AXIS LENGTH** values. A value must be input in **AXIS LENGTH** and **STOP AT MAX** must be enabled.

{%
include callout.html
type="warning"
content="When enabled, **DYNAMIC MAP SIZE** will override **MAP SIZE** values."
%}

{%
include callout.html
type="info"
content="**DYNAMIC MAP SIZE** only affects the display of the virtual garden map in the app. This setting will not affect the area in which FarmBot is allowed to move in. To change where FarmBot is allowed to move, see the settings availabe in the Axes section."
%}

# Map size

Specify custom map dimensions (in millimeters). These values set the size of the virtual garden map unless **DYNAMIC MAP SIZE** is enabled.

{%
include callout.html
type="info"
content="**MAP SIZE** only affects the display of the virtual garden map in the app. This setting will not affect the area in which FarmBot is allowed to move in. To change where FarmBot is allowed to move, see the settings availabe in the Axes section."
%}

# Rotate map

Swap map X and Y axes, making the Y axis horizontal and X axis vertical. This setting will also swap the X and Y jog control buttons <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-down'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-up'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-right'></i></span>.

{%
include callout.html
type="info"
content="**ROTATE MAP** only affects the display of the virtual garden map in the app. This setting will not affect the coordinate system of the FarmBot."
%}

# Map origin

Select a map origin by clicking on one of the four quadrants to adjust the virtual garden map to your viewing angle.

{%
include callout.html
type="info"
content="**MAP ORIGIN** only affects the display of the virtual garden map in the app. This setting will not affect the coordinate system of the FarmBot."
%}

# Crop map images

Crop images displayed in the garden map to align rotation-corrected image edges with the coordinate system. Crop amount determined by **CAMERA ROTATION** value.

# Show camera view area in map

Show the camera's field of view in the garden map. This is useful when manually positioning the FarmBot's camera directly over an object for photographing.

# Confirm plant deletion

Show a confirmation dialog when deleting a plant.
