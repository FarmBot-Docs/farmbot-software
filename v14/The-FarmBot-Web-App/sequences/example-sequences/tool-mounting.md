---
title: "Tool Mounting Sequence"
slug: "tool-mounting"
description: "An example sequence to mount the watering nozzle tool"
---

* toc
{:toc}

{%
include callout.html
type="info"
title=""
content="This example sequence is only applicable to FarmBot Genesis kits, which have a universal tool mounting system and interchangeable tools."
%}

## Step 1: Add the tool to a slot

If you haven't already, [create the watering nozzle tool in the web app and add it to a slot](../../tools.md). Then place the real tool in the physical slot to ensure your real-life configuration matches the web app.

## Step 2: Create the sequence

Navigate to the **Sequences** page of the web app and press the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button to add a new sequence. The new sequence will appear in the sequence editor in the middle column. Give the sequence a descriptive name and optionally assign it a color.

![mount nozzle sequence empty](_images/mount_nozzle_sequence_empty.png)

## Step 3: Start from home

Begin the sequence with a movement to the home position. Add a <span class="fb-step fb-find-home">Find Home</span> command by clicking it or dragging it into the sequence from the **Commands** column.

{%
include callout.html
type="info"
title="If you are not using encoders, endstops, or stall detection..."
content="You may use a <span class='fb-step fb-move-absolute'>Move</span> step to (0, 0, 0) instead of <span class='fb-step fb-find-home'>Find Home</span>."
%}

![mount nozzle sequence find home](_images/mount_nozzle_sequence_find_home.png)

## Step 4: Move above the tool

Next, we want to move FarmBot to a position directly above the tool to prepare it for descending and mounting the tool. Add a <span class="fb-step fb-move">Move</span> command by clicking it or dragging it into the sequence. Select the `Watering Nozzle` tool in the **LOCATION** dropdown and add a `100` mm **Z-OFFSET**.

![mount nozzle sequence move above](_images/mount_nozzle_sequence_move_above.png)

## Step 5: Mount the tool

Now we want FarmBot to descend directly down to mount the tool. Add another <span class="fb-step fb-move">Move</span> command and select the `Watering Nozzle` in the **LOCATION** dropdown as before. This time, we will not add any offsets.

![mount nozzle sequence move to](_images/mount_nozzle_sequence_move_to.png)

## Step 6: Pull the tool out of the slot

At this point, FarmBot's UTM would be mounted to the watering nozzle tool in the slot. The next step will be to pull the tool out of the slot. Add another <span class="fb-step fb-move">Move</span> command and select the `Watering Nozzle` as before. Then add a `100` mm **X-OFFSET**.

![mount nozzle sequence move out](_images/mount_nozzle_sequence_move_out.png)

## Step 7: Save and test the sequence

Press the <span class="fb-button fb-green">SAVE</span> button to save the sequence. Then use the <span class="fb-button fb-orange">RUN</span> button to try out your new sequence.

{%
include callout.html
type="success"
title="Your turn"
content="Now that you've created a tool mounting sequence, try creating a sequence to return the tool to the toolbay."
%}

## Additional considerations

### Prepare for subsequent movements

It can be helpful to add a <span class="fb-step fb-move">Move</span> command with **offset from current location** selected in the **LOCATION** dropdown at the end of the sequence to move FarmBot in the positive Z direction. This will help reduce the likelihood of subsequent movements impacting any nearby objects (such as plants).

### Omit the homing step

You may consider omitting the <span class="fb-step fb-find-home">Find Home</span> command at the beginning of the sequence if the sequence is being used within a larger sequence that already has a <span class="fb-step fb-find-home">Find Home</span> at the beginning.

### Use a location variable

This example sequence can only be used to mount the watering nozzle tool, meaning you will need to make additional sequences to mount other tools. Consider using a [location variable](../variables.md) to make this a generic _mount tool_ sequence that can be used to mount any of your tools.

# What's next?

 * [Watering Sequence](watering.md)
 * [Variables](../variables.md)
