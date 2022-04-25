---
title: "Variable Types"
slug: "variable-types"
description: "Location, Number, Text, Peripheral, Sensor, and Sequence Variables"
---

FarmBot supports six variable types:

* [Location](#location-variables)
* [Number](#number-variables)
* [Text](#text-variables)
* [Peripheral](#resource-variables)
* [Sensor](#resource-variables)
* [Sequence](#resource-variables)

# Location variables

**Location variables** can be set to the following values:

* Externally defined
* Custom coordinates
* Tools and Seed Containers
* Plants
* Weeds
* Map Points

When a location variable is set to `Externally defined` and you are choosing a value for it in a regimen, event, execute command, or from the <span class="fb-button fb-orange">RUN</span> button, you may also select a Group of Plants, Weeds, or Map Points.

# Number variables

**Number variables** can be set to the following values:

* Externally defined
* Custom number

Custom numbers may be positive, negative, and have decimals.

{%
include callout.html
type="info"
content='Number variables are only usable from <span class="fb-step fb-lua">Lua</span> commands via the `variable()` function. Refer to the [Lua developer docs](http://lua.farm.bot/) for additional usage information.'
%}

# Text variables

**Text variables** can be set to the following values:

* Externally defined
* Custom text

Custom text may include any standard characters.

{%
include callout.html
type="info"
content='Text variables are only usable from <span class="fb-step fb-lua">Lua</span> commands via the `variable()` function. Refer to the [Lua developer docs](http://lua.farm.bot/) for additional usage information.'
%}

# Resource variables

Peripheral, sensor, and sequence variables are all grouped into one **Resource** category. To add one of these variable types, click the **VARIABLES** <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button followed by the <span class="fb-button fb-gray">RESOURCE</span> option. At this time these variable types can only be set to `Externally defined`, and then they can be set to any peripheral, sensor, or sequence from a regimen, event, execute command, or from the <span class="fb-button fb-orange">RUN</span> button.

{%
include callout.html
type="info"
content='Peripheral, sensor, and sequence variables are only usable from <span class="fb-step fb-lua">Lua</span> commands via the `variable()` function. Refer to the [Lua developer docs](http://lua.farm.bot/) for additional usage information.'
%}

# What's next?

 * [Shared Sequences](shared-sequences.md)
