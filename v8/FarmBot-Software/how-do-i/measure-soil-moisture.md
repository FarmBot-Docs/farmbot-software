---
title: "Measure Soil Moisture"
slug: "measure-soil-moisture"
---

* toc
{:toc}


{%
include callout.html
type="info"
title=""
content="This document and capability only applies to FarmBot Genesis kits."
%}



{%
include callout.html
type="info"
title=""
content="This section assumes you have wired up your UTM using the [pin mapping table](https://genesis.farm.bot/FarmBot-Genesis-V1-5/tools/utm#pin-mapping) and your soil sensor according to the [wiring instructions](https://genesis.farm.bot/docs/soil-sensor#step-5-wire-it-up). Furthermore, that you are familiar with [sequences](../../Web-App/sequences.md) and [sensors](../../Web-App/controls/sensors.md)."
%}

The soil sensor can be read in a similar fashion to the [tool verification pin](../how-do-i/verify-a-tool-has-been-mounted.md). This time, we will use the `Soil Moisture` sensor (pin 59, UTM pin **D**) in analog pin mode.

![read_soil_sensor.png](read_soil_sensor.png)

As before, a log message will be sent with the pin value. The value for the soil sensor will be about 250 in dry soil (or no soil), and about 850 in very wet soil (or water). You should verify these values for your soil sensor, and determine the value threshold at which you consider your soil to be dry by reading the value in soil areas with different moisture levels.

After you have calibrated your soil sensor, you can use the threshold you have determined to perform actions, such as water, using the <span class="fb-step fb-if-statement">If Statement</span> as shown in the [previous section](../how-do-i/verify-a-tool-has-been-mounted.md).

![is_soil_dry.png](is_soil_dry.png)

