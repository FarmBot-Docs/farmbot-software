---
title: "Farm Designer"
slug: "farm-designer"
description: "Drag-and-drop plant placement :seedling:\n[Open this page in the app](https://my.farm.bot/app/designer)"
---

The **farm designer** allows you to graphically design the layout of your garden, monitor your FarmBot's position, and visualize data such as photos, plant spread, and points.

<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2Fvideoseries%3Flist%3DPLMhsMRlKjcNIYlDKDdKvPQuHqBjjS1ZGc&url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DGVb4fYaqy2M&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2FGVb4fYaqy2M%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allowfullscreen></iframe>

# Map menu
Click the white <i class='fa fa-arrow-left'></i> button in the top right of the map to open up the **map menu**. Here you will find <span class="fb-button fb-gray"><i class='fa fa-minus'></i></span> and <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> buttons to zoom in and out of the map, as well as a toggles to turn on and off map layers:

|Layer                         |Description                   |
|------------------------------|------------------------------|
|**PLANTS**                    |The plant icons (not including weeds or spread)
|**POINTS**                    |Points created in the [points panel](points.md)
|**WEEDS**                     |Weed icons and their spread
|**SPREAD**                    |The spread of plants and weeds
|**FARMBOT**                   |The FarmBot gantry, UTM or tool head, slots, tools, seed containers, peripheral state visualizations, and axis limit lines
|**PHOTOS**                    |Photos taken by FarmBot's onboard camera. See [camera calibration](photos/camera-calibration.md) if photos are not positioned, scaled, or rotated correctly.
|**AREAS**                     |Areas defined by [group filters](groups.md#filtering-by-location).
|**Z**                         |Graphical display of FarmBot's current z-axis position and relevant garden levels.


![farm designer with tools panel open](_images/farm_designer_with_tools_panel_open.png)

![map z-axis display](_images/map_z_display.png)

# Move mode
Pressing the <span class="fb-button fb-gray">MOVE MODE</span> button in the map menu will open the **move to location** panel. Click any spot within the map grid to mark it with an <i class='fa fa-times'></i>. Then press <span class="fb-button fb-gray">MOVE TO THIS COORDINATE</span> to send FarmBot to the selected position. You can optionally enter a new coordinate for the **Z-AXIS**.

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
 * [Gardens](gardens.md)
 * [Events](events.md)
 * [Points](points.md)
 * [Weeds](weeds.md)
 * [Controls](controls.md)
 * [Sensors](sensors.md)
 * [Photos](photos.md)
 * [Farmware](farmware.md)
 * [Tools](tools.md)
 * [Settings](settings.md)
