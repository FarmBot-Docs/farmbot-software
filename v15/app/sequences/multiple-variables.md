---
title: "Multiple Variables"
slug: "multiple-variables"
description: "Using more than one variable in a sequence"
---

# Adding multiple variables

Sequences are not limited to a single variable. To add additional variables click the <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button in the **VARIABLES** section of the sequence editor, followed by the <span class="fb-button fb-gray">variable type</span> desired or select `Add new` in a sequence step dropdown.

![add multiple variables](_images/add_multiple_variables.png)

{%
include callout.html
type="info"
content='When adding new externally defined variables to a sequence you have been using in other sequences, regimens, or events, it is highly recommended to add **DEFAULT VALUES** for the new variables. This will allow FarmBot to run the sequence in the existing sequences, regimens, and/or events using the default values.

If you opt to not provide a default value (selecting "None"), then you will need to explicitly define the variable in all other sequences, regimens, and/or events where the sequence is already being used. If you do not provide a value then the sequence will fail when it runs.'
%}

# Removing variables

To remove a variable, click the <i class='fa fa-trash'></i> icon.

{%
include callout.html
type="info"
content="Only unused variables can be removed."
%}

![remove variable](_images/remove_variable.png)

# Renaming variables

To keep track of what each variable is used for, click the variable's title to add a custom name.

{%
include callout.html
type="pencil"
content="Variables cannot be renamed once in-use by sequence commands, so do the naming up-front."
%}

![rename variable](_images/rename_variables.png)

# Multiple externally defined variables

All `Externally defined` variables will be displayed in the run button popup, execute steps, and all other places where you can provide a value for an [externally defined variable](externally-defined-variables.md).

![multiple variable run button](_images/multiple_variable_run_button.png)

{%
include callout.html
type="warning"
title="Only one group variable is allowed per sequence"
content="When FarmBot runs a sequence with a group variable, it will actually execute the sequence multiple times - once for each member of the group. If a sequence had more than one group variable, it would not be clear what order FarmBot should execute the sequence in. Thus, at this time, multi-group execution is not allowed."
%}

# What's next?

 * [Variable Types](variable-types.md)
