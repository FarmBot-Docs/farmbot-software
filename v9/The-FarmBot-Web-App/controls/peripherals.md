---
title: "Peripherals"
slug: "peripherals"
description: "Manually operate FarmBot's peripherals"
---

* toc
{:toc}

The **PERIPHERALS** widget allows you to manage FarmBot's peripherals and control them in real-time with toggle switches.

![Screen Shot 2019-07-10 at 4.16.20 PM.png](_images/Screen_Shot_2019-07-10_at_4.16.20_PM.png)

# Creating peripherals
To create a new peripheral, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. Provide a <span class="fb-input">Name</span> and <span class="fb-input fb-dropdown">Select a pin <i class='fa fa-caret-down'></i></span> to define the peripheral. Alternatively, press <span class="fb-button fb-green"><i class='fa fa-plus'></i> FARMDUINO</span> to add all of the [standard Farmduino peripherals](https://genesis.farm.bot/docs/farmduino-peripheral-pin-numbers).

{%
include callout.html
type="warning"
title=""
content="Note that pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![Screen Shot 2019-07-10 at 4.19.50 PM.png](_images/Screen_Shot_2019-07-10_at_4.19.50_PM.png)

# Controlling peripherals
## Manual control
You can press a toggle switch to manually control a peripheral when FarmBot is connected and idle. If FarmBot is disconnected or busy, pressing a toggle switch will have no effect. Refer to the table below for all possible states of the toggle switches.

|When a toggle is              |The peripheral's state is     |Clicking the toggle will      |
|------------------------------|------------------------------|------------------------------|
|<span class="fb-peripheral-on">ON</span>|**ON**                        |Turn the peripheral **OFF**
|<span class="fb-peripheral-off">OFF</span>|**OFF**                       |Turn the peripheral **ON**
|<span class="fb-peripheral-unknown"></span>|Unknown                       |Turn the peripheral **OFF**
|<span class="fb-peripheral-on fb-peripheral-disabled">ON</span>|**ON**                        |Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-off fb-peripheral-disabled">OFF</span>|**OFF**                       |Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-unknown fb-peripheral-disabled"></span>|Unknown                       |Not have any effect (FarmBot is not connected)

> 📘 Coming soon
>
> In the future we plan to offer slider controls for analog peripherals.

## Sequence based control
You can also control peripherals from [sequences](../../The-FarmBot-Web-App/sequences.md) by using the <span class="fb-step fb-write-pin">Control Peripheral</span> command. For more information, see the [control peripheral command documentation](../../The-FarmBot-Web-App/sequences/sequence-commands.md#control-peripheral).

# Deleting peripherals
To delete a peripheral, press <span class="fb-button fb-gray">edit</span> and then the peripheral's <span class="fb-button fb-red"><i class='fa fa-minus'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

> 📘 Coming soon
>
> You cannot delete a peripheral that is in-use by a sequence.

# What's next?

 * [Webcam Feeds](../controls/webcam-feeds.md)
