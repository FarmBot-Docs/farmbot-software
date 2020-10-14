---
title: "Sensors"
slug: "sensors"
description: "Manually read FarmBot's sensors"
---

* toc
{:toc}

The **SENSORS** widget allows you to manage FarmBot's sensors and read them in real-time.

![Screen Shot 2019-05-06 at 9.25.03 PM.png](_images/Screen_Shot_2019-05-06_at_9.25.03_PM.png)

# Creating sensors
To create a new sensor, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. To define the sensor, provide a <span class="fb-input">Label</span>, choose a <span class="fb-dropdown">Pin #</span>, and specify if the sensor is analog or digital. Alternatively, press <span class="fb-button fb-green"><i class='fa fa-plus'></i> STOCK SENSORS</span> to add all of the standard FarmBot sensors.

{%
include callout.html
type="warning"
title=""
content="Note that pin numbers are required and must be unique."
%}

When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![edit_sensors.png](_images/edit_sensors.png)

# Reading sensors
## Manual readings
To manually read a sensor, press its <span class="fb-button fb-gray">READ SENSOR</span> button. FarmBot will then read the sensor and display the value in the widget. Digital sensors will provide a value of either `0` or `1`, while analog sensors will provide a value between `0` and `1023`.

![Screen Shot 2019-05-06 at 9.33.31 PM.png](_images/Screen_Shot_2019-05-06_at_9.33.31_PM.png)

## Historical readings
Use the **SENSOR HISTORY** widget to view sensor readings from the past. Optionally, you can filter by **SENSOR**, **TIME PERIOD**, and/or **X**, **Y**, and **Z** coordinates. The **DEVIATION** field can be used to filter within a range of locations around the specified coordinates.

To clear out all current filters, press <span class="fb-button fb-gray">CLEAR FILTERS</span>.

![Screen Shot 2019-05-06 at 9.48.09 PM.png](_images/Screen_Shot_2019-05-06_at_9.48.09_PM.png)

## Sequence based readings
You can also read sensors from [sequences](../sequences.md) by using the <span class="fb-step fb-read-pin">READ SENSOR</span> command. For more information, see the [read sensor command documentation](../sequences/sequence-commands.md#read-sensor).

# Deleting sensors
To delete a sensor, press <span class="fb-button fb-gray">edit</span> and then the sensor's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

{%
include callout.html
type="info"
title=""
content="Note that you cannot delete a sensor that is in-use by a sequence."
%}

