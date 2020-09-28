---
title: "Weed Detection"
slug: "weed-detection"
excerpt: "Computer vision software to detect weeds"
---

* toc
{:toc}


{%
include callout.html
type="warning"
title="Under Development"
content="Weed detection functionality will be available in alpha soon. The [weed detector widget](https://software.farmbot.io/docs/farmware#weed-detector) can be previewed in the [farmbot web app](https://my.farmbot.io)."
%}

FarmBot is designed for removing weeds early and often such that the weeds are always small, young, and fragile, and therefore easily removed by the [Weeder Tool](https://genesis.farmbot.io/docs/weeder).

### How does FarmBot determine which plants are weeds?

Using computer vision, FarmBot detects all plants in the bed. Any detected plant that was not planted by FarmBot is considered a weed and marked for removal with the Weeder tool.



# Overview

### **Prerequisites:**
* **Calibrate camera**: determine pixel location to coordinate conversion parameters
* **Get data**: locations and sizes of known plants

### **Begin Weeding Process:**
* **Move**: to first location in bed to begin taking photos to cover the planting area

### **Repeat:**
_Execute `Plant Detection`_:
***
* **Take photo**
* **Detect plants in photo**: use OpenCV
* **Convert plant pixel locations to coordinates**: use parameters previously calibrated
* **Identify plants**:
  * **Desired plants** are plants within radius of known plants
  * **Weeds** are plants outside known plant regions
* **Save plants**:
  * **Save weed locations**: coordinates to database for removal

***
* **Move**: to next location for next photo and plant detection using sequence builder

### **End:**
* **Remove weeds**: use sequence builder with weeder

# What's a weed?

If we process a photo of our garden bed without providing any information, we would detect all the plants in the image:

![1](https://cloud.githubusercontent.com/assets/12681652/23282676/1e3a6786-f9d7-11e6-8996-c1b1f3914d8a.jpg)

However, we want to determine what is a weed, and the locations of those weeds.

So we feed the plant detection software some calibration parameters, letting it determine the location of the objects in the image. Based on the known locations of desired plants in the image, we can determine which plants are desired plants, and which ones are weeds.

Known (desired) plants are marked with a green circle, the detected plants that match the desired plants are marked with a blue circle, and the detected plants that do not match desired plants are marked with a red circle (those are weeds):

![2](https://cloud.githubusercontent.com/assets/12681652/23282677/1e4de202-f9d7-11e6-8fa5-8c18e9b8f763.jpg)
You can see a grid overlay showing the coordinate system and that the image has been rotated slightly to adjust for camera rotation.

_But wait!_ Our weeding tool is a certain size, and disrupts the soil within a certain area, its region of influence. We can represent that disrupted region with a grey circle:

![3](https://cloud.githubusercontent.com/assets/12681652/23282511/54ca2c92-f9d6-11e6-82f5-e63d5e831bb4.jpg)
We see that the weeder might affect the lower left plant when weeding weed number `1`, since its region of influence is intersecting the desired plant's circle. We also see that we wouldn't be able to weed `2` without significantly disrupting the upper right plant. We can weed `3` safely.

The software takes the weeding tool size into consideration with a feature called __Safe Remove__.

It adjusts the location to be weeded for weed `1` away from the lower left plant, removes weed `2` from the list since it can't be removed safely, and keeps `3` on the list of weeds to remove since there are no conflicts. You can see the weeds to remove and the weeder location represented with the red and grey circles as before, and cyan circles drawn for weeds that may not be removed completely (or at all) because the action might harm a desired plant:

![4](https://cloud.githubusercontent.com/assets/12681652/23282510/54c85e8a-f9d6-11e6-9b46-3dcd304c4e3d.jpg)

You may now instruct the machine to remove the weeds marked in red, and remove the weeds marked in cyan by hand.

Program text output:
```
7 plants detected in image.

4 known plants inputted.
Plants at the following machine coordinates ( X Y ) with R = radius are to be saved:
    (   600   400 ) R = 45
    (   600   500 ) R = 45
    (   700   400 ) R = 25
    (   700   500 ) R = 25

2 plants marked for removal.
Plants at the following machine coordinates ( X Y ) with R = radius are to be removed:
    (   743   541 ) R = 6
    (   654   447 ) R = 6

2 plants marked for safe removal.
Plants at the following machine coordinates ( X Y ) with R = radius were too close to the known plant to remove completely:
    (   651   446 ) R = 7
    (   676   512 ) R = 3

4 detected plants are known or have escaped removal.
Plants at the following machine coordinates ( X Y ) with R = radius have been saved:
    (   700   410 ) R = 31
    (   596   396 ) R = 53
    (   698   485 ) R = 29
    (   600   499 ) R = 42
```
