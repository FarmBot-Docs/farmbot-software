---
title: "Building a Sequence"
slug: "building-a-sequence"
---

# Step 1: Create or select a sequence

In the **sequences** panel, click the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button to create a new sequence. Or, select an existing sequence if you would like to edit it. If you have many sequences, use the search box to find one more quickly.

Once a sequence has been created or selected, it will be loaded into the editor. Enter a unique <span class="fb-input">Sequence name</span> and optionally assign it a color by clicking the <i class='fa fa-paint-brush'></i> icon. The color will not affect FarmBot's execution of the sequence, it is only for helping you organize and recognize your own sequences.

![new sequence](_images/new_sequence.gif)

# Step 2: Add commands

Add the first command (or another sequence) to your sequence by scrolling through the options available in the command pallete or by using the search bar. Click a <span class="fb-add-command-button"><i class='fa fa-plus'></i></span> button to open the command pallete to add an additional sequence step at that location.

![add command](_images/add_command.gif)

On large screens, you may press the <i class='fa fa-expand'></i> icon to open the sequence in a full-screen editor. From the full-screen editor you can add commands by dragging and dropping them from the **commands** panel into the **edit sequence** panel. When dragging and dropping, you can add the new command to the top, bottom, or somewhere in the middle of the sequence. Alternatively, you can click a command and it will be added to the bottom of the sequence.

![dragging wait command into sequence](_images/dragging_wait_command_into_sequence.png)

{%
include callout.html
type="info"
title=""
content="The drag and drop functionality of the full editor does not work on touchscreens. However, sequence editing can be performed on-the-go with just tapping and the default interface."
%}

![phone with add command panel open](_images/phone_with_add_command_panel_open.jpeg)

# Step 3: Define step parameters

For each step (command) in the sequence, enter in your desired parameter values. Some parameters such as **SPEED** will have default values and do not need to be entered in every time. Other parameters require a value to be added or chosen every time.

{%
include callout.html
type="success"
title="We check your work"
content="If you try to save a sequence without values for all of the required parameters for each step, an error will be shown. You can then go back and provide values and try to save again."
%}

# Step 4: Use the step control icons

Each step in a sequence has a cluster of control icons in the top right:

|Icon|Function|
|----|--------|
|<i class='fa fa-question-circle'></i>|Clicking or hovering will bring up a tooltip with information about how to use the command.
|<i class='fa fa-trash'></i>|Clicking will delete the step from the sequence.
|<i class='fa fa-clone'></i>|Clicking will duplicate the step and all of its parameter values. The copy will be inserted directly below the original.
|<i class='fa fa-arrows-v'></i>|Clicking and dragging will allow you to drag and drop the step to another location in the sequence. Just clicking will show a popup with <i class='fa fa-arrow-circle-up'></i> and <i class='fa fa-arrow-circle-down'></i> icons. Clicking one of these will move the step up or down one position in the sequence. These controls are especially useful when using a touchscreen that doesn't work with drag-and-drop functionality.
|<i class='fa fa-external-link'></i>|Clicking will open the linked sequence used in an <span class="fb-step fb-execute">Execute</span> command.
|<i class='fa fa-font'></i>|Clicking toggles between the fancy and basic text editors in a <span class="fb-step fb-lua">Lua</span> command.
|<i class='fa fa-code'></i>|Clicking toggles between the default view of the command and the raw code version of the command. Only available if the **VIEW CELERSCRIPT** sequence editor option is set to <span class="fb-peripheral-on">YES</span>.
|<i class='fa fa-exclamation-triangle'></i>|Clicking will show any warnings or problems with the currently configured step.

# Step 5: Name each step

You can rename each sequence step by clicking on its name and typing in something new. While this is optional, naming each step with some descriptive text can allow you to easily remember what each step is for when you look at the sequence again tomorrow, or in a few months. It might also be useful if multiple people use the same FarmBot account, such as in a school setting, so everyone can understand what each sequence does.

![custom step name](_images/custom_step_name.png)

# Step 6: Save

Whenever a sequence has unsaved changes, an asterisk (**\***) will be shown next to the sequence name in the sequence list, and in the <span class='fb-button fb-green'>Save \*</span> button. When you are finished editing, click <span class="fb-button fb-green">Save \*</span> to save the sequence. Once saving is complete, the button will show as <span class="fb-button fb-gray">Saved <i class='fa fa-check'></i></span>.

# What's next?

 * [Example Sequences](example-sequences.md)
