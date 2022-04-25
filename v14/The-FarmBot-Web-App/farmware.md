---
title: "Farmware"
slug: "farmware"
description: "DEPRECATED plugin system for FarmBot OS <i class='fa fa-puzzle-piece'></i>"
---

{%
include callout.html
type="warning"
title="Farmware is being phased out"
content="As of January 2021 the farmware panel has been hidden from the app for all FarmBot users that did not have any 3rd party farmware installed. The panel remains accessible for now for users with pre-existing 3rd party farmware installed, though we will no longer be maintaining this capability moving forwards. Farmware users are suggested to find alternatives now."
%}

**Farmware** is FarmBot's plugin system allowing 3rd party developers to add custom functionality to FarmBot OS. Once a Farmware has been installed onto your FarmBot, it will show up in the **Farmware panel**. Selecting a Farmware from this list will show its options and controls.

![farmware panel](_images/farmware_panel.png)

# Removing Farmware
To remove a Farmware from your FarmBot, select it in the [Farmware panel](https://my.farm.bot/app/designer/farmware) and press the <span class="fb-button fb-red">REMOVE</span> button at the bottom of the Farmware details panel. Note that if the Farmware is still used in any of your sequences, those sequences will fail when they try to run the Farmware that is no longer available.

{%
include callout.html
type="info"
title=""
content="You must restart your FarmBot for a removed Farmware to stop being displayed in the web app."
%}

