---
title: "Pin Bindings"
slug: "pin-bindings"
description: "Trigger actions and sequences with physical buttons or additional sensors\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=pin_bindings)"
---

* toc
{:toc}

**Pin bindings** allow electrical signals from a button or sensor to trigger a FarmBot **action** or **sequence**. For example, a red button could be used to trigger the <span class="fb-button fb-red">E-STOP</span> action as recommended with FarmBot Genesis v1.4+ kits. For practical examples, see our [use FarmBot's buttons](../../FarmBot-Software/how-to-guides/use-farmbots-buttons.md) how-to guide.

![Screen Shot 2020-04-22 at 4.57.08 PM.png](_images/Screen_Shot_2020-04-22_at_4.57.08_PM.png)

# Adding a pin binding

To add a pin binding, first select the Raspberry Pi GPIO **PIN NUMBER** that your button or sensor is connected to (open the GPIO diagram for assistance by pressing the <span class="fa fa-th-large"></span> icon). Next, choose the type of **BINDING** (either `Sequence` or `Action`) and then select the **TARGET** (the sequence or action desired). Press <span class="fb-button fb-green">BIND</span> to save the pin binding.

{%
include callout.html
type="success"
title=""
content="Upon saving a pin binding, the action or sequence you chose will be triggered once automatically so that you can verify the result."
%}



{%
include callout.html
type="warning"
title="Warning"
content="Binding to a pin without a physical button and pull-down resistor connected may put FarmBot into an unstable state."
%}



{%
include callout.html
type="info"
title="Notes"
content="* Sequences must be synced to the device before use in a pin binding.
* Buttons should be connected between the selected pin and +3.3v."
%}

# Deleting a pin binding
To delete a pin binding, press the <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button.
