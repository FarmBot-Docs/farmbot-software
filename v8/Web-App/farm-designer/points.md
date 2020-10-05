---
title: "Points"
slug: "points"
---

* toc
{:toc}

If you would like to create custom locations in your garden for FarmBot to travel to that are _not_ plants, tool slots, or the home location, you can use **points**. Example uses of the points feature include:

* Points for FarmBot to move to that are out of the way when you're harvesting
* Points in each corner of the bed to serve as alternative "home" positions
* Points for FarmBot to travel to for daily photos

# Adding points
To add a point, click the <span class="fb-button fb-teal"><i class='fa fa-plus'></i></span> button in the points panel.

![Screen Shot 2019-11-30 at 5.00.05 PM.png](_images/Screen_Shot_2019-11-30_at_5.00.05_PM.png)

This will open the **create point** panel where you can provide the **name**, **X and Y coordinates**, **radius**, and **color** for the point. You can also click and drag in the map to define the coordinates and radius. Click <span class="fb-button fb-green">SAVE</span> to save the point.

![Screen Shot 2019-11-30 at 5.01.10 PM.png](_images/Screen_Shot_2019-11-30_at_5.01.10_PM.png)

# Editing points
To edit a point, click it in the points list or in the map (when the points panel is opened). This will open the **edit point** panel, allowing you to change anything about the point. Changes will be saved when you press the <i class='fa fa-arrow-left'></i> button.

![Screen Shot 2019-11-30 at 5.01.21 PM.png](_images/Screen_Shot_2019-11-30_at_5.01.21_PM.png)

# Moving to a point
There are two ways to move FarmBot to a point. The first way is by clicking <span class="fb-button fb-gray">MOVE DEVICE TO LOCATION</span> from the edit point panel.

![Screen Shot 2019-11-30 at 6.16.55 PM.png](_images/Screen_Shot_2019-11-30_at_6.16.55_PM.png)

The second way is from sequences. Simply select the point from the dropdown in a <span class="fb-step fb-move-absolute">Move To</span> command or location variable.

![Screen Shot 2019-11-30 at 6.17.04 PM.png](_images/Screen_Shot_2019-11-30_at_6.17.04_PM.png)

# Deleting points
To delete a point, click on it to open up the edit point panel. Then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="Points cannot be deleted if they are still in-use by any sequences."
%}


# What's next?

 * [Weeds](../farm-designer/weeds.md)
