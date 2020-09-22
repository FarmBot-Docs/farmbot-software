---
title: "Pin Bindings"
slug: "pin-bindings"
---

* toc
{:toc}


{%
include callout.html
type="warning"
title="Warning"
content="Binding to a pin without a physical button and pull-down resistor connected may put FarmBot into an unstable state."
%}



![pin_bindings.png](pin_bindings.png)

_v1.4 stock bindings shown_

Set or remove Raspberry Pi GPIO pin bindings to allow start of a sequence or an action by pressing a physical button (or by motion sensor output).

Select a Raspberry Pi GPIO pin number (open the GPIO diagram for assistance as shown below by pressing the <span class="fa fa-th-large"></span> icon) and select a sequence in the drop down menu.

![pin_bindings_gpio.png](pin_bindings_gpio.png)

Alternatively, select an action:

![pin_bindings_action.png](pin_bindings_action.png)

When done press <span class="fb-button fb-green">BIND</span> to save the binding.

**Notes:**
 * Sequences must be synced to the device before use in a pin binding.
 * Buttons should be connected between the selected pin and +3.3v.
