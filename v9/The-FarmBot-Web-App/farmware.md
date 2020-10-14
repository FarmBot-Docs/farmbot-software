---
title: "Farmware"
slug: "farmware"
description: "Plugin system for FarmBot OS :electric_plug:\n[Open this page in the app](https://my.farm.bot/app/farmware)"
---

* toc
{:toc}

**Farmware** is our plugin system that allows for 3rd party developers to add custom functionality to FarmBot OS. Once a Farmware has been installed onto the FarmBot, it will show up in the list on the left side of the **Farmware page**. Selecting a Farmware from this list will load its options and controls into the middle column, as well as additional information in the right side column when available.

{%
include callout.html
type="info"
title="Interested in developing farmware?"
content="See our [developer documentation](https://developer.farm.bot/docs/farmware) for more details."
%}



<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DvKuOQ5MTb5Q&src=http%3A%2F%2Fwww.youtube.com%2Fembed%2FvKuOQ5MTb5Q&type=text%2Fhtml&key=f2aa6fc3595946d0afc3d76cbbd25dc3&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allow="autoplay; fullscreen" allowfullscreen="true"></iframe>

# Installing farmware

To install new Farmware, use the **INSTALL NEW FARMWARE** form in the left column. Installation is performed by entering the URL of the `manifest.json` file for the Farmware.

# Running farmware

Run a Farmware by selecting it from the list and using the buttons provided.

You can also run Farmware systematically by using the <span class="fb-step fb-take-photo">Run Farmware</span> sequence command in your sequences.

# Advanced options

Press the <span class="fa fa-gear"></span> icon to open the Farmware advanced menu. To show first-party Farmware (pre-installed Farmware) in the Farmware list, enable the **SHOW IN LIST** setting. If a pre-installed Farmware is accidentally deleted, press the **REINSTALL** <i class='fa fa-download'></i> button.

# What's next?

 * [Take Photo](farmware/take-photo.md)
 * [Camera Calibration](farmware/camera-calibration.md)
 * [Weed Detection](farmware/weed-detection.md)
