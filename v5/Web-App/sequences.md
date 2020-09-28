---
title: "Sequences"
slug: "sequences"
excerpt: "Drag-and-drop programming for your FarmBot [my.farmbot.io/app/sequences](http://my.farmbot.io/app/sequences)"
---

* toc
{:toc}


# Sequence building

The web app is a platform designed to give you unlimited control over how you use your FarmBot and therefore how you grow your food. Because nobody wants to sit on their computer all day controlling their FarmBot manually, we have designed several features to help you automate your farming operation.

The sequence builder allows you to combine the most basic operations of FarmBot into more complex actions composed of many different steps. When a sequence is initiated, FarmBot will execute all of the steps in the sequence one after the other until it is done.

# Sequence commands (aka 'steps')

These are the basic operations we can use in sequences that FarmBot can execute:
* <span class="fb-step fb-move-absolute">Move Absolute</span> - Moves the device to an absolute coordinate position at any speed. This is useful for moving to tool, plant, and home locations.
* <span class="fb-step fb-move-relative">Move Relative</span> - Moves the device a specific distance in any direction at any speed, relative from the last position. This is useful for movements after a absolute movement to a dynamically loaded location. Eg: Moving in a square relative to a plant after the device moved absolutely to the plant.
* <span class="fb-step fb-write-pin">Write Pin</span> - Writes a value to any pin on the Arduino. This is used for operating tools that use peripherals, such as the vacuum pump and water valve.
* <span class="fb-step fb-read-pin">Read Pin</span> - Reads the value from any pin on the Arduino. This is used for [tool verification and sensors](../Additional-Information/reading-pins.md).
* <span class="fb-step fb-wait">Wait</span> - Causes a delay before executing the next operation in the sequence. This could be used to water for a certain amount of time.
* <span class="fb-step fb-send-message">Send Message</span> - Sends a message to the web app. This is useful for error and success notifications and debugging. `{{ x }}` can be used as a variable for FarmBot's current x axis position (`y` and `z` can also be used). `{{ pin13 }}` can be used to write the current value of pin 13 (pins 0 through 69 can also be used).
* <span class="fb-step fb-find-home">Find Home</span> - Perform a homing operation to set zero for one axis or all axes.
* <span class="fb-step fb-if-statement">If Statement</span> - Executes another sequence if a condition is true. This is useful for error detection and smarter, condition based farming.
* <span class="fb-step fb-execute">Execute Sequence</span> - Use existing sequences as steps in a new, larger sequence. This technique allows you to re-use smaller sequences in different combinations to create far more complex sequences that are easier to modify, manage, and mashup. You can then use the individual sequences in other ways without having to recreate them each time.
* <span class="fb-step fb-take-photo">Run Farmware</span> - Run the `plant-detection` farmware. Support for other farmwares coming soon.
* <span class="fb-step fb-wait">Take Photo</span> - Takes a picture with a USB webcam or the Raspberry Pi camera (select your camera in the [Device](../Web-App/device.md#device) widget) and sends it to the web app.

{%
include callout.html
type="info"
title=""
content="While using the web app, hover over the `?` icon in a sequence step to view usage information."
%}



# Building a sequence

The general overview of creating a sequence is:

1. In the **Sequences** panel, click <span class="fb-button fb-green">+</span>
2. In the **Sequence Editor** panel, enter a name for your sequence and assign it a color
2. Drag and drop blocks from the **Commands** panel into the **Sequence Editor** panel
3. For each operation, enter in your desired parameter values. Some parameters such as *speed* can use default values for your device and do not need to be entered in every time.
4. Reorder, copy, and delete operations as needed
5. Click <span class="fb-button fb-green">Save</span>

In the next sections, several sequences are built as examples.

# Create a tool mounting sequence

Let's create a sequence to mount the watering nozzle as an example.

First, add the [watering tool](https://genesis.farmbot.io/docs/watering-nozzle) to the toolbay and follow the [Tools](../Web-App/tools.md) instructions to add it to the web app.

Navigate to the **Sequences** page of the web app, and press the <span class="fb-button fb-green">+</span> button in the right column to add a new sequence.

![sequence_overview.png](sequence_overview.png)

You will see the new sequence appear in the sequence editor in the middle column.

Give the sequence a descriptive name.

![s2.png](s2.png)

Begin the sequence with a movement to home. Add a **Move Absolute** step by clicking <span class="fb-step fb-move-absolute">Move Absolute</span> in the commands (left) column. You may also click and drag the command into your sequence.

![s3.png](s3.png)

Next, add a step to move above the tool we want mounted, in this case, the watering nozzle. Add another <span class="fb-step fb-move-absolute">Move Absolute</span> command as we did in the last step, or press the copy icon (<span class="fa fa-copy"></span>) in the existing step (second icon from the right in the step's info bar).

Select the `Watering Nozzle` (added in the tools page) in the `Import Coordinates From` dropdown.

We want to move to the location directly above the tool before descending down to connect to the tool, so we'll add a `100` mm Z-Offset.

![s4.png](s4.png)

Next we'll want FarmBot to descend directly down to make contact with the tool. Add another `Move Absolute` command and select the `Watering Nozzle` in the `Import Coordinates From` dropdown as before. This time, there will not be an offset.

![s5.png](s5.png)

At this point, FarmBot's UTM would be attached to the tool in the toolbay. The next step will be to pull the tool out of the toolbay. Add another <span class="fb-step fb-move-absolute">Move Absolute</span> command and select the `Watering Nozzle` as the coordinates, this time adding a `100` mm X-Offset.

![s6.png](s6.png)

That's it! Now press the <span class="fb-button fb-green">SAVE</span> button.

To recap, the steps are move to home, move directly above the tool, descend directly down to make contact with the tool, and move the tool out of the toolbay. Now you can use this sequence any time you would like to use the watering tool!

![s7.png](s7.png)

Don't forget to <span class="fb-button fb-yellow">SYNC</span> before pressing <span class="fb-button fb-orange">TEST</span> to test your new sequence!

{%
include callout.html
type="success"
title="Your turn"
content="Now that you've created a tool mounting sequence, try creating a sequence to return the tool to the toolbay."
%}



# Create a watering sequence

Now that we've created a sequence to mount the watering tool, we can create a sequence to use the tool. As an example, we have a Spinach plant at coordinates `(100, 200, -600)` that we would like to water.

1. **Mount the Watering Tool** - Mount the watering nozzle by using the <span class="fb-step fb-execute-sequence">Execute Sequence</span> step and selecting the `Mount Watering Tool` sequence created in the previous section.
2. **Move to 100mm above the Spinach plant** - Move the watering nozzle above the plant to be watered (`(100, 200, -600)` in this example) by making use of the Z-Offset input in the <span class="fb-step fb-move-absolute">Move Absolute</span> step.
3. **Open the solenoid valve to start the flow of water** - Add a <span class="fb-step fb-write-pin">Write Pin</span> step to write `Pin 10` with a value of `1`  (The pin number should correspond to the pin you have attached the solenoid valve to on the RAMPS board. See the [peripherals widget instructions](https://software.farmbot.io/docs/controls#peripherals) in order to test valve operation.)
4. **Wait** - Use the <span class="fb-step fb-wait">Wait</span> step to continue watering the Spinach plant for 4000 milliseconds (4 seconds).
5. **Cose the solenoid valve** - Use another <span class="fb-step fb-write-pin">Write Pin</span> step to write `Pin 10` with a value of `0`, turning off the flow of water.

![watering_sequence.png](watering_sequence.png)

Press the <span class="fb-button fb-green">SAVE</span> button and then <span class="fb-button fb-yellow">SYNC NOW</span> at the top of the page to sync your new sequence with the device, and press <span class="fb-button fb-orange">TEST</span> to try out your new sequence!

# Alternative watering sequence methods

The watering steps in the sequence shown above can be made into their own sequence, which increases re-usability and makes it easier to make changes to the watering action.

![light_water.png](light_water.png)

Then, the new water dispensing sequence can be added by using an **Execute Sequence** step after movement to each plant location.

![water_spinach_2.png](water_spinach_2.png)

As you can see in this sequence, we have imported coordinates from plant locations in the **Move Absolute** step. These plant locations are defined in the [Farm Designer](../Web-App/farm-designer.md).

As always, don't forget to <span class="fb-button fb-green">SAVE</span> and <span class="fb-button fb-yellow">SYNC NOW</span> before pressing <span class="fb-button fb-orange">TEST</span> to test the sequence!
