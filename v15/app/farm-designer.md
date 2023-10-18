---
title: "Farm Designer"
slug: "farm-designer"
description: "Drag-and-drop plant placement :seedling:\n[Open this page in the app](https://my.farm.bot/app/designer)"
---

The **farm designer** allows you to graphically design the layout of your garden, monitor your FarmBot's position, and visualize data such as photos, plant spread, and points.

{% include youtube.html id="GVb4fYaqy2M" %}

# Map menu

Click the white <i class='fa fa-arrow-left'></i> button in the top right of the map to open up the **map menu**. Here you will find <span class="fb-button fb-gray"><i class='fa fa-minus'></i></span> and <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> buttons to zoom in and out of the map, as well as toggles to turn on and off map layers. Some map layers have <i class='fa fa-caret-down'></i> submenus with additional options.

![farm designer with tools panel open](_images/farm_designer_with_tools_panel_open.png)

## Plants

The **PLANTS** toggle displays or hides plant icons and their current size shadow. Within the plants submenu:

- **PLANT ANIMATIONS** enables or disables plant animations in the garden map. This may be useful to turn off when using the app on a lower powered device such as a smartphone or chromebook, or if experiencing performance issues.
- **CONFIRM PLANT DELTION** shows a confirmation dialog when deleting a plant.

## Points

The **POINTS** toggle displays or hides all points created from the [points panel](points.md).

## Soil

The **SOIL** toggle displays an interpolated map of soil levels based on [soil height measurements](../app/photos/measure-soil-height.md).

![soil interpolation](_images/soil_interpolation.png)

## Weeds

The **WEEDS** toggle displays weed icons and their current size shadow. Within the weeds submenu:

- **SHOW REMOVED** displays weeds with a status of `Removed`.

## Spread

The **SPREAD** toggle displays the spread of plants as a ring around the plant. This ring represents the space that the plant will occupy once fully grown. Plants with a spread value provided by OpenFarm will have a green spread ring. If a spread value from OpenFarm was not available when the plant was created, the spread ring will be white and have a fallback diameter of 250mm.

{%
include callout.html
type="info"
content="Once a plant is created in the app, the spread value will not be updated if the plant's spread value changes in OpenFarm."
%}

If a plant has an assigned [spread curve](../app/curves.md), then the expected spread of the plant at a certain age can be visualized by hovering over the spread curve.

![spread curve](_images/spread_curve.png)

## FarmBot

The **FARMBOT** toggle displays the FarmBot gantry, UTM or tool head, slots, tools, seed containers, peripheral state visualizations, and axis limit lines. Within the FarmBot submenu:

- **TRAIL** displays a virtual trail for FarmBot in the garden map to show movement and watering history while the map is open. Toggling this setting will clear data for the current trail.
- **FARMBOT MOTOR LOAD** displays high motor load warning indicators in the map. Requires **TRAIL** and **STALL DETECTION** to be enabled.

## Photos

The **PHOTOS** toggle displays photos taken by FarmBot's onboard camera. Within the photos submenu:

- **NEWER THAN/OLDER THAN** filters the display of photos by date and time.
- **CROP MAP IMAGES** crops images displayed in the garden map to align rotation-corrected image edges with the coordinate system. Crop amount determined by **CAMERA ROTATION** value.
- **CLIP PHOTOS OUT OF BOUNDS** removes portions of images that extend beyond the garden map boundaries.
- **CAMERA VIEW** displays the camera's field of view in the garden map. This is useful when manually positioning the FarmBot's camera directly over an object for photographing.
- **UNCROPPED CAMERA VIEW** displays the camera's uncropped and unrotated field of view in the garden map when **CROP MAP IMAGES** is enabled.

{%
include callout.html
type="info"
content="See [camera calibration](photos/camera-calibration.md) if photos are not positioned, scaled, or rotated correctly."
%}

## Areas

The **AREAS** toggle displays areas defined by [group filters](groups.md#filtering-by-location).

## Readings

The **READINGS** toggle displays sensor readings.

## Moisture

The **MOISTURE** toggle displays an interpolated map of soil moisture based on recent [soil moisture readings](../docs/how-to-guides/measure-soil-moisture.md).

## Z

The **Z** toggle shows FarmBot's current z-axis position and relevant garden levels in a graphical display next to the map menu.

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
