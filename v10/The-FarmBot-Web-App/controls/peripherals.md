---
title: "Peripherals"
slug: "peripherals"
description: "Manually operate FarmBot's peripherals <i class='fa fa-toggle-on'></i>\n[Open this panel in the app](https://my.farm.bot/app/designer/controls)"
---

* toc
{:toc}

The **PERIPHERALS** section of the controls panel allows you to manage FarmBot's peripherals and control them in real-time with toggle switches and sliders.

![Screen Shot 2020-06-30 at 11.33.14 AM.png](_images/Screen_Shot_2020-06-30_at_11.33.14_AM.png)

# Creating peripherals
To create a new peripheral, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. Provide a <span class="fb-input">Name</span>, <span class="fb-input fb-dropdown">Select a pin <i class='fa fa-caret-down'></i></span>, and choose `Digital` or `Analog` to define the peripheral. Pressing <span class="fb-button fb-green"><i class='fa fa-plus'></i> STOCK</span> will add all of the standard peripherals included with your FarmBot kit.

{%
include callout.html
type="warning"
title=""
content="Pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![Screen Shot 2020-06-30 at 11.34.39 AM.png](_images/Screen_Shot_2020-06-30_at_11.34.39_AM.png)

# Controlling peripherals
## Manual control
You can press a toggle switch to manually control digital peripherals when FarmBot is connected and idle. If FarmBot is disconnected or busy, pressing a toggle switch will have no effect. Refer to the table below for all possible states of the toggle switches.

|When a toggle is              |The peripheral's state is     |Clicking the toggle will      |
|------------------------------|------------------------------|------------------------------|
|<span class="fb-peripheral-on">ON</span>|**ON**                        |Turn the peripheral **OFF**
|<span class="fb-peripheral-off">OFF</span>|**OFF**                       |Turn the peripheral **ON**
|<span class="fb-peripheral-unknown"></span>|Unknown                       |Turn the peripheral **OFF**
|<span class="fb-peripheral-on fb-peripheral-disabled">ON</span>|**ON**                        |Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-off fb-peripheral-disabled">OFF</span>|**OFF**                       |Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-unknown fb-peripheral-disabled"></span>|Unknown                       |Not have any effect (FarmBot is not connected)

Analog peripherals can be controlled with the sliders when FarmBot is connected and idle.

![Screen Shot 2020-06-30 at 11.39.07 AM.png](_images/Screen_Shot_2020-06-30_at_11.39.07_AM.png)

## Sequence based control
You can also control peripherals from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-write-pin">Control Peripheral</span> command. For more information, see the [control peripheral command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#control-peripheral).

# Deleting peripherals
To delete a peripheral, press <span class="fb-button fb-gray">edit</span> and then the peripheral's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

{%
include callout.html
type="info"
title=""
content="You cannot delete a peripheral that is in-use by a sequence."
%}


# What's next?

 * [Webcam Feeds](webcam-feeds.md)
