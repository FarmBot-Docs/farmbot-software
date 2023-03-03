---
title: "Farm Designer"
slug: "farm-designer"
description: "Drag-and-drop plant placement :seedling:\n[Open this page in the app](https://my.farm.bot/app/designer)"
---

The **farm designer** allows you to graphically design the layout of your garden, monitor your FarmBot's position, and visualize data such as photos, plant spread, and points.

{% include youtube.html id="GVb4fYaqy2M" %}

# Map menu

Click the white <i class='fa fa-arrow-left'></i> button in the top right of the map to open up the **map menu**. Here you will find <span class="fb-button fb-gray"><i class='fa fa-minus'></i></span> and <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> buttons to zoom in and out of the map, as well as a toggles to turn on and off map layers. Some map layers have <i class='fa fa-caret-down'></i> submenus with additional options.

|Layer/Submenu item            |Description                   |
|------------------------------|------------------------------|
|**PLANTS**                    |Display plant icons (not including weeds or spread).
|Plant animations              |Enable or disable plant animations in the garden map. This may be useful to turn off when using the app on a lower powered device such as a smartphone or chromebook.
|Confirm plant deletion        |Show a confirmation dialog when deleting a plant.
|**POINTS**                    |Display points created in the [points panel](points.md)
|**SOIL**                      |Display an interpolated map of soil levels based on soil height measurements.
|**WEEDS**                     |Display weed icons and their spread.
|Show removed                  |Display weeds with a status of `Removed`.
|**SPREAD**                    |Display the spread of plants and weeds.
|**FARMBOT**                   |Display the FarmBot gantry, UTM or tool head, slots, tools, seed containers, peripheral state visualizations, and axis limit lines.
|Trail                         |Display a virtual trail for FarmBot in the garden map to show movement and watering history while the map is open. Toggling this setting will clear data for the current trail.
|FarmBot motor load            |Display high motor load warning indicators in the map. Requires **TRAIL** and **STALL DETECTION** to be enabled.
|**PHOTOS**                    |Photos taken by FarmBot's onboard camera. See [camera calibration](photos/camera-calibration.md) if photos are not positioned, scaled, or rotated correctly.
|Newer than/Older than         |Filter the display of photos by date and time.
|Crop map images               |Crop images displayed in the garden map to align rotation-corrected image edges with the coordinate system. Crop amount determined by **CAMERA ROTATION** value.
|Clip photos out of bounds     |Remove portions of images that extend beyond the garden map boundaries.
|Camera view                   |Display the camera's field of view in the garden map. This is useful when manually positioning the FarmBot's camera directly over an object for photographing.
|Uncropped camera view         |Display the camera's uncropped and unrotated field of view in the garden map when **CROP MAP IMAGES** is enabled.
|**AREAS**                     |Display areas defined by [group filters](groups.md#filtering-by-location).
|**READINGS**                  |Display sensor readings.
|**MOISTURE**                  |Display an interpolated map of soil moisture based on recent soil moisture readings.
|**Z**                         |Graphical display of FarmBot's current z-axis position and relevant garden levels.

![farm designer with tools panel open](_images/farm_designer_with_tools_panel_open.png)

![map z-axis display](_images/map_z_display.png)

# Map settings

![map settings](_images/map_settings.png)

## Dynamic map size

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

## Map size

Specify custom map dimensions (in millimeters). These values set the size of the virtual garden map unless **DYNAMIC MAP SIZE** is enabled.

{%
include callout.html
type="info"
content="**MAP SIZE** only affects the display of the virtual garden map in the app. This setting will not affect the area in which FarmBot is allowed to move in. To change where FarmBot is allowed to move, see the settings availabe in the Axes section."
%}

## Rotate map

Swap map X and Y axes, making the Y axis horizontal and X axis vertical. This setting will also swap the X and Y jog control buttons <span class="fb-button fb-gray"><i class='fa fa-arrow-left'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-down'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-up'></i></span> <span class="fb-button fb-gray"><i class='fa fa-arrow-right'></i></span>.

{%
include callout.html
type="info"
content="**ROTATE MAP** only affects the display of the virtual garden map in the app. This setting will not affect the coordinate system of the FarmBot."
%}

## Map origin

Select a map origin by clicking on one of the four quadrants to adjust the virtual garden map to your viewing angle.

{%
include callout.html
type="info"
content="**MAP ORIGIN** only affects the display of the virtual garden map in the app. This setting will not affect the coordinate system of the FarmBot."
%}

# Move mode

Click anywhere within the map grid to mark the location with crosshairs and open up the location panel for the selected coordinates. Then press <span class="fb-button fb-green">GO</span> to send FarmBot to the selected position. Before moving to the new location, you may optionally enter a new coordinate for the **Z AXIS**, adjust the **SPEED**, or toggle on **SAFE Z** option.

![farm designer move mode](_images/farm_designer_move_mode.png)

# Select mode

To select multiple plants, click anywhere in the map and drag the mouse cursor to create a **box selection**. All plants located within the box will be displayed in the **select** panel. Alternatively, you may press the <span class="fb-button fb-gray">SELECT</span> button located in the map menu, and then use the box-selection technique.

Once the select panel is open, you can click-to-add additional plants to the selection, or click an already selected plant to remove it from the selection. Once you are satisfied with your selection, use one of the **SELECTION ACTIONS**.

You may also change the **SELECTION TYPE** to allow for selecting other objects in the map, such as weeds or points.

![farm designer select mode](_images/farm_designer_select_mode.png)

# Profile viewer

Press the <span style="color: white; background: #a64d79; border-radius: 50%; font-size: 0.75rem; padding: 3px 5px"><i class='fa fa-area-chart'></i></span> icon at the bottom of the screen to open the profile viewer.

![profile viewer choose a location](_images/profile_viewer_choose_a_location.png)

Click anywhere in the farm designer map to view a profile of that location.
A shaded area will appear across the map to indicate the region the profile represents: any items within the region will appear in the profile.

![profile viewer](_images/profile_viewer.png)

![profile viewer (x-axis profile)](_images/profile_viewer_x.png)

The selected **SAFE HEIGHT** (from [axis settings](settings/axes.md#safe-height)) is shown as a horizontal <span style="color: #3377dd">blue</span> line, and the selected **SOIL HEIGHT** is shown as a horizontal <span style="color: #ccaa88">brown</span> line.
Points and soil height points are shown as dots with lines connecting them according to their color.

Use the **AXIS** toggle to switch between X and Y axis profiles.
Input a different **WIDTH** to narrow or broaden the profile search area.
Enable **FOLLOW** to use FarmBot's current location as the profile position.
Click the <i class='fa fa-chevron-up'></i> icon to switch between quick and full profile views.

# What's next?

 * [Plants](plants.md)
 * [Groups](groups.md)
 * [Events](events.md)
 * [Points](points.md)
 * [Weeds](weeds.md)
 * [Controls](controls.md)
 * [Sensors](sensors.md)
 * [Photos](photos.md)
 * [Tools](tools.md)
 * [Settings](settings.md)
