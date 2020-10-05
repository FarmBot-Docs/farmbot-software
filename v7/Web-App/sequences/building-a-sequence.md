---
title: "Building a Sequence"
slug: "building-a-sequence"
---

* toc
{:toc}

The general overview of creating a sequence is:

1. In the **Sequences** panel, click <span class="fb-button fb-green">+</span>
2. In the **Sequence Editor** panel, enter a name for your sequence and assign it a color
2. Drag and drop blocks from the **Commands** panel into the **Sequence Editor** panel
3. For each operation, enter in your desired parameter values. Some parameters such as *speed* can use default values for your device and do not need to be entered in every time.
4. Reorder, copy, and delete operations as needed
5. Click <span class="fb-button fb-green">Save</span>

In the next sections, several sequences are built as examples.

# Example 1: Create a tool mounting sequence

Let's create a sequence to mount the watering nozzle as an example.

First, add the [watering tool](https://genesis.farm.bot/docs/watering-nozzle) to the toolbay and follow the [Tools](../../Web-App/tools.md) instructions to add it to the web app.

Navigate to the **Sequences** page of the web app, and press the <span class="fb-button fb-green">+</span> button in the left column (**Sequences**)  to add a new sequence.

![empty_sequences.png](_images/empty_sequences.png)

You will see the new sequence appear in the sequence editor in the middle column.

Give the sequence a descriptive name.

![sequence_named.png](_images/sequence_named.png)

Begin the sequence with a movement to home. Add a <span class="fb-step fb-find-home">Find Home</span> command by clicking it or dragging it into the sequence from the commands (right) column.

![sequence_home.png](_images/sequence_home.png)



{%
include callout.html
type="warning"
title="If you are not using encoders or endstops..."
content="You may use a **Move Absolute** step to (0, 0, 0) instead of **Find Home**."
%}

Next, add a step to move above the tool we want mounted, in this case, the watering nozzle. Add a <span class="fb-step fb-move-absolute">Move Absolute</span> command by clicking it or dragging it into the sequence.

Select the `Watering Nozzle` (added in the tools page) in the `Import Coordinates From` dropdown.

We want to move to the location directly above the tool before descending down to connect to the tool, so we'll add a `100` mm Z-Offset.

![sequence_above.png](_images/sequence_above.png)

Next we'll want FarmBot to descend directly down to make contact with the tool. Add another <span class="fb-step fb-move-absolute">Move Absolute</span> command as we did in the last step and select the `Watering Nozzle` in the `Import Coordinates From` dropdown as before. This time, there will not be an offset.

*(Alternatively, press the copy icon (<span class="fa fa-copy"></span>) in the existing <span class="fb-step fb-move-absolute">Move Absolute</span> step (second icon from the right in the step's info bar) and clear the offset.)*

![sequence_move_to_step.png](_images/sequence_move_to_step.png)

At this point, FarmBot's UTM would be attached to the tool in the toolbay. The next step will be to pull the tool out of the toolbay. Add another <span class="fb-step fb-move-absolute">Move Absolute</span> command and select the `Watering Nozzle` as the coordinates, this time adding a `100` mm X-Offset.

![sequence_complete.png](_images/sequence_complete.png)

That's it! Now press the <span class="fb-button fb-green">SAVE</span> button.

To recap, the steps are move to home, move directly above the tool, descend directly down to make contact with the tool, and move the tool out of the toolbay. Now you can use this sequence any time you would like to use the watering tool!

![sequence_saved.png](_images/sequence_saved.png)

Don't forget to <span class="fb-button fb-yellow">SYNC</span> before pressing <span class="fb-button fb-orange">TEST</span> to test your new sequence!

{%
include callout.html
type="success"
title="Your turn"
content="Now that you've created a tool mounting sequence, try creating a sequence to return the tool to the toolbay."
%}



{%
include callout.html
type="info"
title="Additional considerations"
content="* It can be helpful to add an additional <span class=\"fb-step fb-move-absolute\">Move Absolute</span> command at the end of the tool mounting sequence copying the inputs in the last step but with a positive z-offset. This can help prepare FarmBot for the next movement by moving above any nearby objects.
* It may be desirable to omit the `Find Home` at the beginning of the sequence if the sequence is being used within a larger sequence that already has a `Find Home` at the beginning."
%}



# Example 2: Create a watering sequence

Now that we've created a sequence to mount the watering tool, we can create a sequence to use the tool. As an example, we have a Spinach plant at coordinates `(200, 960, 0)` that we would like to water.

1. **Mount the Watering Tool** - Mount the watering nozzle by using the <span class="fb-step fb-execute">Execute Sequence</span> step and selecting the `Mount Watering Tool` sequence created in the previous section.
2. **Move to above the Spinach plant** - Move the watering nozzle above the plant to be watered (`(200, 960, 0)` in this example) by making use of the Z-Offset input in the <span class="fb-step fb-move-absolute">Move Absolute</span> step.
3. **Open the solenoid valve to start the flow of water** - Add a <span class="fb-step fb-write-pin">Write Pin</span> step to write `Pin 8` with a value of `ON`  (The pin number should correspond to the pin you have attached the solenoid valve to on the RAMPS board. See the [peripherals widget instructions](https://software.farmbot.io/docs/controls#peripherals) in order to test valve operation.)
4. **Wait** - Use the <span class="fb-step fb-wait">Wait</span> step to continue watering the Spinach plant for 4000 milliseconds (4 seconds).
5. **Cose the solenoid valve** - Use another <span class="fb-step fb-write-pin">Write Pin</span> step to write `Pin 8` with a value of `OFF`, turning off the flow of water.

![spinach_1.png](_images/spinach_1.png)

Press the <span class="fb-button fb-green">SAVE</span> button and then <span class="fb-button fb-yellow">SYNC NOW</span> at the top of the page to sync your new sequence with the device, and press <span class="fb-button fb-orange">TEST</span> to try out your new sequence!

# Example 3: Alternative watering sequence

The watering steps in the sequence shown above can be made into their own sequence, which increases re-usability and makes it easier to make changes to the watering action.

![light_water.png](_images/light_water.png)

Then, the new water dispensing sequence can be added by using an <span class="fb-step fb-execute">Execute Sequence</span> step after movement to each plant location.

![water_all_spinach.png](_images/water_all_spinach.png)

As you can see in this sequence, we have imported coordinates from plant locations in the <span class="fb-step fb-move-absolute">Move Absolute</span> step. These plant locations are defined in the [Farm Designer](../../Web-App/farm-designer.md).

As always, don't forget to <span class="fb-button fb-green">SAVE</span> and <span class="fb-button fb-yellow">SYNC NOW</span> before pressing <span class="fb-button fb-orange">TEST</span> to test the sequence!

# Sequence building tips
## Rearranging steps
Click and drag a step in the sequence editor to the empty space above or below any other step to drop it into that new position.
