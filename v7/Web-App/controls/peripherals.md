---
title: "Peripherals"
slug: "peripherals"
description: "Manually operate FarmBot's peripherals"
---

The **PERIPHERALS** widget allows you to manage FarmBot's peripherals and control them in real-time with toggle switches.

![peripherals.png](_images/peripherals.png)

# Creating peripherals
To create a new peripheral, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. Provide a <span class="fb-input">Label</span> and <span class="fb-input">Pin #</span> to define the peripheral. Alternatively, press <span class="fb-button fb-green"><i class='fa fa-plus'></i> FARMDUINO</span> to add all of the [standard Farmduino peripherals](https://genesis.farm.bot/docs/farmduino-peripheral-pin-numbers).

{%
include callout.html
type="warning"
title=""
content="Note that pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![edit_peripherals.png](_images/edit_peripherals.png)

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



{%
include callout.html
type="info"
title="Coming soon"
content="In the future we plan to offer slider controls for analog peripherals."
%}

## Sequence based control
You can also control peripherals from [sequences](../sequences.md) by using the <span class="fb-step fb-write-pin">Control Peripheral</span> command. For more information, see the [control peripheral command documentation](../sequences/sequence-commands.md#control-peripheral).

# Deleting peripherals
To delete a peripheral, press <span class="fb-button fb-gray">edit</span> and then the peripheral's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

{%
include callout.html
type="info"
title=""
content="Note that you cannot delete a peripheral that is in-use by a sequence."
%}


# What's next?

 * [Webcam Feeds](webcam-feeds.md)
