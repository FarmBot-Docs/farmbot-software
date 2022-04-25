---
title: "Weeds"
slug: "weeds"
description: "Manage the weeds found in your garden\n[Open this panel in the app](https://my.farm.bot/app/designer/weeds)"
---

The **weeds panel** allows you to manage the weeds in your garden. Weeds are divided into three categories:

  * **PENDING** weeds have been detected by FarmBot's camera and are awaiting manual triage. The <span class="fb-button fb-green"><i class='fa fa-check'></i></span> and <span class="fb-button fb-green"><i class='fa fa-check'></i> ALL</span> buttons will move weeds to the **ACTIVE** category while the <span class="fb-button fb-red"><i class='fa fa-times'></i></span> and <span class="fb-button fb-red"><i class='fa fa-times'></i> ALL</span> buttons will delete the weeds.
  * **ACTIVE** weeds are weeds currently active in the garden. These weeds were either identified by FarmBot's camera and then triaged into this category, or they were manually added with the <span class="fb-button fb-red"><i class='fa fa-plus'></i></span> button.
  * **REMOVED** weeds are weeds that are no longer a concern. This category should include weeds that have been removed by FarmBot or by hand.

![Screen Shot 2020-08-24 at 11.38.34 AM.png](_images/Screen_Shot_2020-08-24_at_11.38.34_AM.png)

# Adding weeds
To manually add a weed, click the <span class="fb-button fb-red"><i class='fa fa-plus'></i></span> button in the weeds panel. This will open the **add weed** panel where you can provide a **NAME**, **COLOR**, **X**, **Y**, and **Z** coordinates, and a **RADIUS** for the weed. You can also click and drag in the map to define the coordinates and radius. Click <span class="fb-button fb-green">SAVE</span> to save the weed.

![Screen Shot 2020-08-24 at 12.07.33 PM.png](_images/Screen_Shot_2020-08-24_at_12.07.33_PM.png)

# Editing weeds
To edit a weed, click it in the panel or in the map (when the weeds panel is opened). This will open the **edit weed** panel, allowing you to change anything about the weed. Changes will be saved when you press the <i class='fa fa-arrow-left'></i> button.

![Screen Shot 2020-08-24 at 12.11.58 PM.png](_images/Screen_Shot_2020-08-24_at_12.11.58_PM.png)

# Moving to a weed
There are two ways to move FarmBot to a weed. The first way is by clicking <span class="fb-button fb-gray">MOVE DEVICE TO LOCATION</span> from the edit weed panel.

![Screen Shot 2020-08-24 at 12.13.11 PM.png](_images/Screen_Shot_2020-08-24_at_12.13.11_PM.png)

The second way is from sequences. Simply select the weed from the **LOCATION** dropdown in a <span class="fb-step fb-move">Move</span> command or location variable.

![Screen Shot 2020-08-24 at 12.21.40 PM.png](_images/Screen_Shot_2020-08-24_at_12.21.40_PM.png)

# Deleting weeds
To delete a weed, click on it to open up the edit weed panel. Then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="Weeds cannot be deleted if they are still in-use by any sequences."
%}

