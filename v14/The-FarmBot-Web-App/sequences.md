---
title: "Sequences"
slug: "sequences"
description: "Drag-and-drop programming for your FarmBot :pager:\n[Open this page in the app](https://my.farm.bot/app/sequences)"
---

* toc
{:toc}

The web app is a platform designed to give you unlimited control over how you use your FarmBot and therefore how you grow your food. Because nobody wants to sit on their computer all day controlling their FarmBot manually, we have designed several features to help you automate your farming operation.

**Sequences** allow you to combine the most basic **commands** of FarmBot (such as moving or controlling a peripheral) into more complex actions requiring multiple **steps** (for example: picking up the watering nozzle, watering a plant, and then putting the tool away). When a sequence is initiated, FarmBot will execute all of the commands in the sequence (the steps) one after the other until the sequence is finished.

<iframe width="100%" height="450" src="https://www.youtube.com/embed/8tw6Qmu-WdI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

You can create sequences using the sequence editor as shown below. On the left of the screen is a list of all your sequences, which can be organized into folders. In the middle is the currently opened sequence. And on the right are the available commands that you can add to sequences.

![sequences page](_images/sequences_page.png)

# Organizing sequences into folders

Add a new folder in the top level by pressing the <span class="fb-button fb-green"><i class='fa fa-folder'></i></span> button next to the sequence search bar. To change the color of the folder, click the folder icon.

![folder color selection](_images/folder_color_selection.png)

Open and close a folder by clicking the <i class='fa fa-chevron-right'></i> and <i class='fa fa-chevron-down'></i> buttons, or open and close all folders by clicking the <span class="fb-button fb-gray"><i class='fa fa-chevron-right'></i></span> and <span class="fb-button fb-gray"><i class='fa fa-chevron-down'></i></span> buttons next to the sequence search bar.

Click the <i class='fa fa-ellipsis-v'></i> menu shown on the right when hovering on a folder to delete the folder, edit the folder name, add a subfolder, or add a new sequence within the folder.

![folder options menu](_images/folder_options_menu.png)

To move sequences between folders, click or click and drag the <i class='fa fa-bars'></i> menu shown on the right when hovering over the sequence.

![sequence move icon](_images/sequence_move_icon.png)

# Pinned sequences

You can **pin** frequently used sequences by pressing the <i class='fa fa-thumb-tack'></i> icon in the edit sequence header.

![pinned sequence](_images/pinned_sequence.png)

Pinned sequences will appear at the bottom of the Add Command panel so that you may quickly add them to other sequences.

![pinned sequences in add command panel](_images/pinned_sequences_in_add_command_panel.png)

Pinned sequences are also listed in a section on the controls panel with associated <span class="fb-button fb-orange">RUN</span> buttons so that you may quickly manually execute these sequences.

![pinned sequences in add controls panel](_images/pinned_sequences_in_controls_panel.png)

# Sequence editor options

You can customize how the sequence editor works with the options in the <i class='fa fa-cog'></i> menu located in the edit sequence header.

![sequence editor options](_images/sequence_editor_options.png)

* **CONFIRM STEP DELETION** - Show a confirmation dialog when deleting a sequence step.
* **CONFIRM SEQUENCE DELETION**- Show a confirmation dialog when deleting a sequence.
* **SHOW PINS** - Show raw pin lists (eg: `Pin 13`) in <span class="fb-step fb-read-pin">Read Sensor</span>, <span class="fb-step fb-write-pin">Control Peripheral</span>, and <span class="fb-step fb-if-statement">If Statement</span> steps.
* **OPEN OPTIONS BY DEFAULT** - Choose whether advanced step options are open or closed by default.
* **DISCARD UNSAVED SEQUENCE CHANGES** - Don't ask about saving sequence work before closing browser tab. Warning: may cause loss of data.
* **VIEW CELERYSCRIPT** - View raw data representation of sequence steps or the entire sequence. Useful for software developers. Once this toggle is set to <span class="fb-peripheral-on">YES</span>, you may switch between the raw celerysript and normal views of individual sequence steps or the entire sequence by clicking the <i class='fa fa-code'></i> buttons in the sequence or step headers.

# What's next?

 * [Sequence Commands](sequences/sequence-commands.md)
 * [Building a Sequence](sequences/building-a-sequence.md)
 * [Example Sequences](sequences/example-sequences.md)
 * [Variables](sequences/variables.md)
 * [Externally Defined Variables](sequences/externally-defined-variables.md)
