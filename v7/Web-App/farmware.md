---
title: "Farmware"
slug: "farmware"
description: "Plugin system for FarmBot OS [my.farm.bot/app/farmware](https://my.farm.bot/app/farmware)"
---

* toc
{:toc}

Farmware is our plugin system that allows for 3rd party developers to add custom functionality to FarmBot OS. Once a Farmware has been installed onto the FarmBot, it will show up in the list on the left side of the **Farmware page**. Selecting a Farmware from this list will load its options and controls into the middle column, as well as additional information in the right side column when available.

![Screen Shot 2019-05-02 at 5.28.47 PM.png](_images/Screen_Shot_2019-05-02_at_5.28.47_PM.png)



# Installing farmware

To install new Farmware, use the **INSTALL NEW FARMWARE** form in the left column. Installation is performed by entering the URL of the `manifest.json` file for the Farmware.

# Running farmware

Run a Farmware by selecting it from the list and using the buttons provided.

You can also run Farmware systematically by using the <span class="fb-step fb-take-photo">Run Farmware</span> sequence command in your sequences.

# Advanced options

Press the <span class="fa fa-gear"></span> icon to open the Farmware advanced menu. To show first-party Farmware (pre-installed Farmware) in the Farmware list, enable the **SHOW IN LIST** setting. If a pre-installed Farmware is accidentally deleted, press the **REINSTALL** <i class='fa fa-download'></i> button.

{%
include callout.html
type="info"
title="Interested in developing farmware?"
content="Please see our [developer documentation](https://developer.farm.bot/docs/farmware) for more details."
%}


# What's next?

 * [Take Photo](../Web-App/farmware/take-photo.md)
 * [Camera Calibration](../Web-App/farmware/camera-calibration.md)
 * [Weed Detection](../Web-App/farmware/weed-detection.md)
