---
title: "Peripherals"
slug: "peripherals"
description: "Manually operate FarmBot's peripherals <i class='fa fa-toggle-on'></i>\n[Open this popup in the app](https://my.farm.bot/app/designer/controls)"
---

The **PERIPHERALS** tab of the controls popup allows you to manage FarmBot's peripherals and control them in real-time with toggle switches and sliders. Here you can also manage the actions associated with the electronics box push buttons, and interact with a virtual representation of the buttons and LED indicators.

![controls popup peripherals tab](_images/controls_popup_peripherals_tab.png)

# Editing peripherals

To create a new peripheral, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. Provide a <span class="fb-input">Name</span>, <span class="fb-input fb-dropdown">Select a pin <i class='fa fa-caret-down'></i></span>, and choose `Digital` or `Analog` to define the peripheral. Pressing <span class="fb-button fb-green"><i class='fa fa-plus'></i> STOCK</span> will add all of the standard peripherals included with your FarmBot kit.

{%
include callout.html
type="warning"
title=""
content="Pin numbers are required and must be unique."
%}

To delete a peripheral, press the peripheral's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. You cannot delete a peripheral that is in-use by a sequence.

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![edit peripherals](_images/edit_peripherals.png)

# Controlling peripherals

You can press a toggle switch to manually control digital peripherals when FarmBot is connected and idle. If FarmBot is disconnected or busy, pressing a toggle switch will have no effect. Refer to the table below for all possible states of the toggle switches.

|When a toggle is                                                  |The peripheral's state is     |Clicking the toggle will      |
|------------------------------------------------------------------|------------------------------|------------------------------|
|<span class="fb-peripheral-on">ON</span>                          |**ON** |Turn the peripheral **OFF**
|<span class="fb-peripheral-off">OFF</span>                        |**OFF**|Turn the peripheral **ON**
|<span class="fb-peripheral-unknown"></span>                       |Unknown|Turn the peripheral **OFF**
|<span class="fb-peripheral-on fb-peripheral-disabled">ON</span>   |**ON** |Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-off fb-peripheral-disabled">OFF</span> |**OFF**|Not have any effect (FarmBot is busy)
|<span class="fb-peripheral-unknown fb-peripheral-disabled"></span>|Unknown|Not have any effect (FarmBot is not connected)

Analog peripherals can be controlled with the sliders when FarmBot is connected and idle.

![analog peripheral control](_images/analog_peripheral_control.png)

# Push buttons

To change a push button's behavior, press <span class="fb-button fb-gray">EDIT</span>, and then select a new **Action** or **Sequence** in the push button's dropdown. When finished editing, press <span class="fb-button fb-gray">BACK</span>.

Once synced, you can press the physical push button on top of the FarmBot electronics box or click the virtual button in the app to activate the chosen action or sequence.

![edit push button](_images/edit_push_button.png)


# What's next?

 * [Webcam Feeds](webcam-feeds.md)
