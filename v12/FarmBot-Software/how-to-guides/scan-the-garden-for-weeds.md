---
title: "Scan the Garden for Weeds"
slug: "scan-the-garden-for-weeds"
description: "**In this guide:** Learn how to scan the whole garden for weeds using a group of points."
---


{%
include callout.html
type="info"
title=""
content="This guide assumes you have already [calibrated your FarmBot's camera](../../The-FarmBot-Web-App/photos/camera-calibration.md)."
%}

# Step 1: Create a point grid
Create a grid of **points** for every location you want FarmBot to take a photo at by using the **Grid** feature in the **Add point** panel. Toggling **CAMERA VIEW AREA** <span class="fb-peripheral-on">ON</span> will allow you to visualize the camera's field of view in the map. Adjust the horizontal and vertical **SPACING** between points in the grid until there will be minimal overlap between photos. Then press **SAVE**.

{%
include callout.html
type="success"
title=""
content="Use a unique color for these points - it will come in handy in the next step!"
%}



![point grid creation](_images/point_grid_creation.png)

# Step 2: Group the points
Create a **group** with all of the points in the point grid by first **Selecting all** `Points` and then checking the **Color** that you used in the previous step. Give the group a unique name such as `Photo Scan Point Grid`.

![point group creation](_images/point_group_creation.png)

# Step 3: Create sequences
You will need to create two sequences to scan the whole garden. The first sequence will simply <span class="fb-step fb-move-absolute">MOVE TO</span> one of the points (via a location variable) and then <span class="fb-step fb-run-farmware">DETECT WEEDS</span>. We'll call this sequence `Detect weeds at one point`.

![detect weeds at point sequence](_images/detect_weeds_at_point_sequence.png)

The second sequence will <span class="fb-step fb-execute">EXECUTE</span> the `Detect weeds at one point` sequence for every point in the `Photo Scan Point Grid` group. We'll call this sequence `Scan entire garden for weeds`.

![scan entire garden for weeds sequence](_images/scan_entire_garden_for_weeds_sequence.png)

# Step 4: Scan the garden
You're now ready to <span class="fb-button fb-orange">RUN</span> the `Scan entire garden for weeds` sequence and view the results in the farm designer.

![garden scan](_images/garden_scan.gif)

After the first test run, you may need to:

  * Adjust the locations, spacing, and number of points in the grid
  * Adjust the color range or other weed detection parameters

# What's next?

 * [Weeds](../../The-FarmBot-Web-App/weeds.md)
