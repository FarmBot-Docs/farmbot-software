---
title: "Points"
slug: "points"
description: "Create custom locations in your garden :round_pushpin:\n[Open this panel in the app](https://my.farm.bot/app/designer/points)"
---

* toc
{:toc}

If you would like to create custom locations in your garden for FarmBot to travel to that are _not_ plants, tool slots, or the home location, you can use **points**. Example uses of the points feature include:

* Points for FarmBot to move to that are out of the way when you're harvesting
* Points in each corner of the bed to serve as alternative "home" positions
* Points for FarmBot to travel to for daily photos

# Adding points
To add points, click the <span class="fb-button fb-teal"><i class='fa fa-plus'></i></span> button in the points panel. This will open the **add point** panel where you can add individual points or create a grid of points.

![empty points panel](_images/empty_points_panel.png)

## Individual points
To add an individual point to the map, provide a **name**, **color**, **X and Y coordinates**, and **radius**. Alternatively you can click and drag in the map to define the coordinates and radius. The <span class="fb-button fb-blue">USE FARMBOT'S CURRENT POSITION</span> button can be used if FarmBot is already positioned at a location of interest. Then click <span class="fb-button fb-green">SAVE</span> to save the point.

![add new point](_images/add_new_point.png)

## Soil height points
Check the **AT SOIL LEVEL** checkbox to add a special soil height point. Soil height points are automatically added to an expandable item in the points panel where they are sorted by height. Toggling soil height <span class="fb-peripheral-on">ON</span> will show the soil height values in the map.

![soil height points](_images/soil_height_points.png)

## Grid of points
To add a grid of points to the map, provide the **name**, **color**, and **radius** for all of the points in the upper portion of the panel. Then provide the grid's **STARTING X and Y** coordinates and the **# OF POINTS** and **SPACING** in each direction. Press **PREVIEW** to preview the grid in the map. If you are satisfied, then press **SAVE**.

![add point grid](_images/add_point_grid.png)

Toggling **CAMERA VIEW AREA** <span class="fb-peripheral-on">ON</span> will show the camera's field of view in the map when the FarmBot is located at each point in the grid. This is useful when creating grids for photographing large areas of the garden.

![add point grid with camera fov](_images/add_point_grid_with_camera_fov.png)

# Editing points
To edit a point, click it in the points list or in the map (when the points panel is opened). This will open the **edit point** panel, allowing you to change anything about the point. Changes will be saved when you press the <i class='fa fa-arrow-left'></i> button.

![points panel with point hovered](_images/points_panel_with_point_hovered.png)

# Moving to a point
There are two ways to move FarmBot to a point. The first way is by clicking <span class="fb-button fb-gray">MOVE DEVICE TO LOCATION</span> from the edit point panel.

![edit point panel with move to button](_images/edit_point_panel_with_move_to_button.png)

The second way is from sequences. Simply select the point from the dropdown in a <span class="fb-step fb-move-absolute">Move To</span> command or location variable.

![move to point sequence step](_images/move_to_point_sequence_step.png)

# Sorting points
Click the <i class='fa fa-search'></i> icon to change the order of points in the panel, where <i class='fa fa-calendar'></i>: age, <i class='fa fa-font'></i>: name, <i class='fa fa-sort-amount-desc'></i>: size, and <b><i>z</i></b>: height.

![point sort menu](_images/point_sort_menu.png)

# Deleting points
To delete a point, click on it to open up the edit point panel. Then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="Points cannot be deleted if they are in-use by any sequences, regimens, or events."
%}


# What's next?

 * [Weeds](weeds.md)
