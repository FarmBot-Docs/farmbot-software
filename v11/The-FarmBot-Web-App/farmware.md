---
title: "Farmware"
slug: "farmware"
description: "Plugin system for FarmBot OS <i class='fa fa-puzzle-piece'></i>\n[Open this panel in the app](https://my.farm.bot/app/designer/farmware)"
---

**Farmware** is FarmBot's plugin system allowing 3rd party developers to add custom functionality to FarmBot OS. Once a Farmware has been installed onto your FarmBot, it will show up in the **Farmware panel**. Selecting a Farmware from this list will show its options and controls.

![Screen Shot 2020-06-29 at 10.08.06 PM.png](_images/Screen_Shot_2020-06-29_at_10.08.06_PM.png)



{%
include callout.html
type="info"
title="Interested in developing farmware?"
content="See our [developer documentation](https://developer.farm.bot/docs/farmware) for more details."
%}

# Installing Farmware

{%
include callout.html
type="warning"
title="Only install Farmware from developers you trust"
content="Installing a Farmware onto your FarmBot will allow it to add, modify, and delete any resources from your FarmBot account every time it is run, including your Plants, Weeds, Sequences, Regimens, Events, Settings, and more. **Exercise caution when installing Farmware**, and only install Farmware from developers you trust."
%}

To install a new Farmware, press the <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button on the Farmware panel. Enter the **FARMWARE MANIFEST URL** (link to the `manifest.json` file for the Farmware) and press <span class="fb-button fb-green">install</span>.

![Screen Shot 2020-06-29 at 9.36.08 PM.png](_images/Screen_Shot_2020-06-29_at_9.36.08_PM.png)

# Running Farmware

You can run a Farmware *manually* by selecting it in the Farmware panel and pressing the <span class="fb-button fb-green">RUN</span> button. If the Farmware accepts **PARAMETERS**, it will run using the default values as shown in the panel, which can be edited as needed.

![Screen Shot 2020-06-29 at 9.55.17 PM.png](_images/Screen_Shot_2020-06-29_at_9.55.17_PM.png)

You can also run Farmware *systematically* by using the <span class="fb-step fb-run-farmware">Run Farmware</span> command in sequences. By default, the Farmware will use values for all **PARAMETERS** as listed in the Farmware panel, but you can override those values on a per-command basis using the checkboxes and input fields in the sequence command.

![Screen Shot 2020-06-29 at 9.53.16 PM.png](_images/Screen_Shot_2020-06-29_at_9.53.16_PM.png)

# Removing Farmware
To remove a Farmware from your FarmBot, press the <span class="fb-button fb-red">REMOVE</span> button at the bottom of the Farmware details panel. Note that if the Farmware is still used in any of your sequences, those sequences will fail when they try to run the Farmware that is no longer available.

{%
include callout.html
type="info"
title=""
content="Currently you must restart your FarmBot for a removed Farmware to stop being displayed in the web app."
%}

