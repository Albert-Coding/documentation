---
id: terminate
title: tctl workflow terminate
sidebar_label: terminate
description: How to terminate a Workflow Execution using tctl.
tags:
  - tctl
---

The `tctl workflow terminate` command terminates a [Workflow Execution](/concepts/what-is-a-workflow-execution).

Terminating a running Workflow Execution records a `WorkflowExecutionTerminated` event as the closing event in the History.
No more command tasks will be scheduled.

See also [`tctl workflow cancel`](/tctl/workflow/cancel).

`tctl workflow terminate <modifiers>`

The following modifiers control the behavior of the command.

<!--WorkflowId-->

import WorkflowId from '../../tctl/modifiers/workflow-id.md'

<WorkflowId />

<!--RunId-->

import RunId from '../../tctl/modifiers/run-id.md'

<RunId />

<!--Reason-->

import Reason from '../../tctl/modifiers/reason.md'

<Reason />