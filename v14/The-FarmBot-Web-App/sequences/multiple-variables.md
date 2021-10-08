---
title: "Multiple Variables"
slug: "multiple-variables"
description: "Using more than one variable in a sequence"
---

* toc
{:toc}

# Adding multiple variables

Sequences are not limited to a single variable. To add additional variables click <span class="fb-add-variable">ADD VARIABLE</span> in the sequence header as many times as needed or select `Add new` in a sequence step dropdown.

![add multiple variables](_images/add_multiple_variables.gif)

If you already have a sequence scheduled for use in regimens and events, you can still safely add additional externally defined variables and FarmBot will continue to run the sequence using the **DEFAULT VALUES** of the new variables. Any regimens or events which you want to run with a different variable value will need to be updated.

# Removing variables

To remove a variable, click the <i class='fa fa-trash'></i> icon.

{%
include callout.html
type="info"
content="Only unused variables can be removed."
%}

![remove variable](_images/remove_variable.png)

# Name each variable

To keep track of what each variable is used for, click the variable's title to add a custom name.

{%
include callout.html
type="pencil"
content="Variables cannot be renamed once in-use by sequence commands, so do the naming up-front."
%}

![rename variable](_images/rename_variables.png)

As variables are added, updated, and removed, their corresponding listing in sequence step dropdowns will be updated.

![variables with custom names](_images/variables_with_custom_names.png)

# Multiple externally defined variables

All `Externally defined` variables will be displayed in the run button popup, execute steps, and all other places where you can provide a value for an [externally defined variable](externally-defined-variables.md).

![multiple variable run button](_images/multiple_variable_run_button.png)

# Group variable limitations

{%
include callout.html
type="warning"
title="Only one group variable is allowed per sequence"
content="When FarmBot runs a sequence with a group variable, it will actually execute the sequence multiple times - once for each member of the group. If a sequence had more than one group variable, it would not be clear what order FarmBot should execute the sequence in. Thus, at this time, multi-group-variable execution is not allowed."
%}

# What's next?

 * [Shared Sequences](shared-sequences.md)
