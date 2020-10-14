---
title: "Weed Detection"
slug: "weed-detection"
description: "Computer vision software to detect weeds"
---

* toc
{:toc}


{%
include callout.html
type="success"
title="1st party farmware"
content="This farmware comes pre-installed with FarmBot OS."
%}

FarmBot is designed to remove weeds early and often, so that the weeds are always small, young, and fragile, and therefore easily removed by the [weeding tool](https://genesis.farm.bot/docs/weeder). FarmBot finds weeds by using computer vision software to detect all plants in the bed and then mark any detected plant that was not planted by FarmBot as a weed.

<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D_Qko08YBP2o&src=http%3A%2F%2Fwww.youtube.com%2Fembed%2F_Qko08YBP2o&type=text%2Fhtml&key=f2aa6fc3595946d0afc3d76cbbd25dc3&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allow="autoplay; fullscreen" allowfullscreen="true"></iframe>

# Using the weed detector

> 📘Calibration required
>
> To use the weed detection feature, you must first [calibrate the camera](camera-calibration.md).

![Screen Shot 2019-05-02 at 6.15.16 PM.png](_images/Screen_Shot_2019-05-02_at_6.15.16_PM.png)

## Select a color range
The weed detector software needs a range of color to look for when determining what is a plant and what is soil or other background. Use the sliders for **HUE**, **SATURATION**, and **VALUE** to select a range of colors you want to detect. The color boxes will give an indication of the range selected. For the hue slider, a green color range is approximately `30` to `90`.

## Tune processing parameters
Once an image has been taken with the camera, the weed detector software will process it. There are several processing parameters available (**BLUR**, **MORPH**, and **ITERATION**) that can help you fine tune the system to perform the best in your environment. It is recommended to use the default values at first, run a test, and then experiment with the processing parameter values to see how the results change.

## Detect weeds
Move the FarmBot over a section of soil. Press <span class="fb-button fb-green">detect weeds</span> to instruct FarmBot to take a photo and then process that image with the weed detector software. Any weeds found in the image will appear in the [farm designer](../../The-FarmBot-Web-App/farm-designer.md) as a pair of red circles. The small center circle will represent the center of the weed, while the larger outer circle will represent the size of the weed. Press <span class="fb-button fb-red">clear weeds</span> to delete all weed points from the map.

<span class="fb-button fb-green">scan image</span> can be used to run weed detection on an image already taken, instead of taking a new photo.

## Scan the entire garden
Detect weeds across FarmBot's entire bed by creating a sequence of movements in a grid pattern with a <span class="fb-step fb-run-farmware">Run Farmware</span> step at each grid point, set to run the `Weed Detector` farmware.

## Remove weeds with FarmBot
Weed removal can be performed by creating a weed removal sequence that uses the weeding tool on weeds (points) in the farm designer.

# How it works

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
