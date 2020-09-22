---
title: "Sensors"
slug: "sensors"
excerpt: "Manually read FarmBot's sensors 🌡️\n[Open this panel in the app](https://my.farm.bot/app/designer/sensors)"
---

* toc
{:toc}

The **sensors panel** allows you to manage FarmBot's sensors, take measurements, and view historical sensor readings.

{%
include callout.html
type="info"
title="Not shown for all bots"
content="If your FarmBot kit did not include any sensors (Express v1.0 kits), then the sensors panel will not be shown in the app. You can override this using the **HIDE SENSORS** setting."
%}



![Screen Shot 2020-06-30 at 12.28.34 PM.png](Screen_Shot_2020-06-30_at_12.28.34_PM.png)

# Creating sensors
To create a new sensor, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green">:fa-plus:</span> button. To define the sensor, provide a <span class="fb-input">Name</span>, choose a <span class="fb-dropdown">Pin #</span>, and specify if the sensor is `Digital` or `Analog`. Pressing <span class="fb-button fb-green">:fa-plus: STOCK SENSORS</span> will add all of the standard sensors included with your FarmBot kit.

{%
include callout.html
type="warning"
title=""
content="Pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![Screen Shot 2020-06-30 at 12.30.24 PM.png](Screen_Shot_2020-06-30_at_12.30.24_PM.png)

# Reading sensors
To manually read a sensor, press its <span class="fb-button fb-gray">READ SENSOR</span> button. FarmBot will then read the sensor and display the value in the widget. Digital sensors will provide a value of either `0` or `1`, while analog sensors will provide a value between `0` and `1023`.

![Screen Shot 2020-06-30 at 12.35.58 PM.png](Screen_Shot_2020-06-30_at_12.35.58_PM.png)

You can also read sensors from [sequences](sequences.md) by using the <span class="fb-step fb-read-pin">READ SENSOR</span> command. For more information, see the [read sensor command documentation](doc:sequence-commands#section-read-sensor).

## Historical readings
Use the **SENSOR HISTORY** section of the panel to view sensor readings from the past. Optionally, you can filter by **SENSOR**, **TIME PERIOD**, and/or **X**, **Y**, and **Z** coordinates. The **DEVIATION** field can be used to filter within a range of locations around the specified coordinates. To remove all current filters, press <span class="fb-button fb-gray">CLEAR FILTERS</span>.

![Screen Shot 2020-06-30 at 12.39.50 PM.png](Screen_Shot_2020-06-30_at_12.39.50_PM.png)

# Deleting sensors
To delete a sensor, press <span class="fb-button fb-gray">edit</span> and then the sensor's <span class="fb-button fb-red">:fa-times:</span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

{%
include callout.html
type="info"
title=""
content="You cannot delete a sensor that is in-use by a sequence."
%}

# Hiding sensors
If you do not plan to use any sensors, use the **HIDE SENSORS** toggle in the [app settings panel](settings/account-settings.md) to remove the sensors panel.
