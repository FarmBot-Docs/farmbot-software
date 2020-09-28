---
title: "Weeds"
slug: "weeds"
excerpt: "Manage the weeds found in your garden\n[Open this panel in the app](https://my.farm.bot/app/designer/weeds)"
---

* toc
{:toc}

The **weeds panel** allows you to keep track of the weeds in your garden that your FarmBot has detected or that you have manually entered.

# Adding weeds
To add a weed, click the <span class="fb-button fb-red"><i class="fa fa-plus"></i></span> button in the weeds panel.

![Screen Shot 2019-11-30 at 10.38.56 PM.png](Screen_Shot_2019-11-30_at_10.38.56_PM.png)

This will open the **create weed** panel where you can provide the **name**, **X and Y coordinates**, **radius**, and **color** for the weed. You can also click and drag in the map to define the coordinates and radius. Click <span class="fb-button fb-green">SAVE</span> to save the weed.

![Screen Shot 2019-11-30 at 10.43.37 PM.png](Screen_Shot_2019-11-30_at_10.43.37_PM.png)

# Editing weeds
To edit a weed, click it in the weeds list or in the map (when the weeds panel is opened). This will open the **edit weed** panel, allowing you to change anything about the weed. Changes will be saved when you press the <i class="fa fa-arrow-left"></i> button.

![Screen Shot 2019-11-30 at 10.45.20 PM.png](Screen_Shot_2019-11-30_at_10.45.20_PM.png)

# Moving to a weed
There are two ways to move FarmBot to a weed. The first way is by clicking <span class="fb-button fb-gray">MOVE DEVICE TO LOCATION</span> from the edit weed panel.

![Screen Shot 2019-11-30 at 10.46.34 PM.png](Screen_Shot_2019-11-30_at_10.46.34_PM.png)

The second way is from sequences. Simply select the weed from the dropdown in a <span class="fb-step fb-move-absolute">Move To</span> command or location variable.

![Screen Shot 2019-11-30 at 10.47.21 PM.png](Screen_Shot_2019-11-30_at_10.47.21_PM.png)

# Deleting weeds
To delete a weed, click on it to open up the edit weed panel. Then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="Weeds cannot be deleted if they are still in-use by any sequences."
%}

