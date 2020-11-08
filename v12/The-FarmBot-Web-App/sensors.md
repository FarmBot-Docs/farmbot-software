---
title: "Sensors"
slug: "sensors"
description: "Manually read FarmBot's sensors 🌡️\n[Open this panel in the app](https://my.farm.bot/app/designer/sensors)"
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



![sensors panel](_images/sensors_panel.png)

# Creating sensors
To create a new sensor, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. To define the sensor, provide a <span class="fb-input">Name</span>, choose a <span class="fb-dropdown">Pin #</span>, and specify if the sensor is `Digital` or `Analog`. Pressing <span class="fb-button fb-green"><i class='fa fa-plus'></i> STOCK SENSORS</span> will add all of the standard sensors included with your FarmBot kit.

{%
include callout.html
type="warning"
title=""
content="Pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![edit sensors](_images/edit_sensors.png)

# Reading sensors
To manually read a sensor, press its <span class="fb-button fb-gray">READ SENSOR</span> button. FarmBot will then read the sensor and display the value in the widget. Digital sensors will provide a value of either `0` or `1`, while analog sensors will provide a value between `0` and `1023`.

![read sensors](_images/read_sensors.png)

You can also read sensors from [sequences](sequences.md) by using the <span class="fb-step fb-read-pin">READ SENSOR</span> command. For more information, see the [read sensor command documentation](sequences/sequence-commands.md#read-sensor).

## Historical readings
Use the **SENSOR HISTORY** section of the panel to view sensor readings from the past. Optionally, you can filter by **SENSOR**, **TIME PERIOD**, and/or **X**, **Y**, and **Z** coordinates. The **DEVIATION** field can be used to filter within a range of locations around the specified coordinates. To remove all current filters, press <span class="fb-button fb-gray">CLEAR FILTERS</span>.

![sensor reading history](_images/sensor_reading_history.png)

# Deleting sensors
To delete a sensor, press <span class="fb-button fb-gray">edit</span> and then the sensor's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

{%
include callout.html
type="info"
title=""
content="You cannot delete a sensor that is in-use by a sequence."
%}

# Hiding sensors
If you do not plan to use any sensors, use the **HIDE SENSORS** toggle in the [app settings panel](settings/account-settings.md) to remove the sensors panel.


# What's next?

 * [Photos](photos.md)
