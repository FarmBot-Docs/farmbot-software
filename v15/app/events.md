---
title: "Events"
slug: "events"
description: "Schedule FarmBot actions :calendar: :white_check_mark:\n[Open this panel in the app](https://my.farm.bot/app/designer/events)"
---

It would not be convenient for you to manually initiate sequences every time you want them to execute. This is where **events** come in to help. If you've ever used a calendar application before, you'll feel right at home with this. Let's get started

{% include youtube.html id="vwnsr8zelaY" %}

# Creating events

Navigate to the events panel on the farm designer page and press the <span class="fb-button fb-yellow"><i class='fa fa-plus'></i></span> button to create a new **event**. Choose the **SEQUENCE OR REGIMEN** that you would like to execute and provide a **START** date and time. By default, the current date and current time + 3 minutes will be input into the date and time fields.

Optionally, sequence events can be set to **REPEAT EVERY** custom interval **UNTIL** a stop date and time.

{%
include callout.html
type="info"
content="New events must be scheduled at least one minute into the future."
%}

{%
include callout.html
type="warning"
title="FarmBot performs updates at 3AM"
content="Avoid scheduling any events between 2AM and 4AM."
%}

![events panel](_images/events_panel.png)

If the sequence or regimen you selected has an [externally defined variable](sequences/externally-defined-variables.md), you will need to provide a value for that variable in the event creation panel.

![add new event panel](_images/add_new_event_panel.png)

Once you are finished, press the <span class="fb-button fb-green">SAVE</span> button to save the event. The event will now show up in the agenda.

![events panel with events](_images/events_panel_with_events.png)

# Editing events

To edit an event, hover over an event in the agenda view and press the <i class='fa fa-edit'></i> icon. Make the desired changes and press <span class="fb-button fb-green">SAVE</span>.

{%
include callout.html
type="warning"
title="Some changes aren't allowed"
content="You cannot change from executing a sequence to executing a regimen or vice versa."
%}

![edit event button](_images/edit_event_button.png)

# Deleting events

To delete an event, click on it to open up the edit event panel. Then press the <span class="fb-button fb-red">DELETE</span> button.

# What's next?

 * [Controls](controls.md)
