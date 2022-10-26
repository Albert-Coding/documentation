---
id: task-queue
title: tctl version-next task-queue command reference
sidebar_label: task-queue
description: How to use the tctl version-next task-queue command
toc_max_heading_level: 4
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

The `tctl task-queue` commands enable <a class="tdlp" href="/tasks#task-queue">Task Queue<span class="tdlpiw"><img src="/img/link-preview-icon.svg" alt="Link preview icon" /></span><div class="tdlpc"><p class="tdlppt">What is a Task Queue?</p><p class="tdlppd">A Task Queue is a first-in, first-out queue that a Worker Process polls for Tasks.</p><p class="tdlplm"><a href="/tasks#task-queue">Learn more</a></p></div></a> operations.

Alias: `tq`

- [`tctl task-queue describe`](/tctl-next/task-queue#describe)
- [`tctl task-queue list-partition`](/tctl-next/task-queue#list-partition)

## describe

Alias: `desc`

The `tctl task-queue describe` command describes the poller information of a <a class="tdlp" href="/tasks#task-queue">Task Queue<span class="tdlpiw"><img src="/img/link-preview-icon.svg" alt="Link preview icon" /></span><div class="tdlpc"><p class="tdlppt">What is a Task Queue?</p><p class="tdlppd">A Task Queue is a first-in, first-out queue that a Worker Process polls for Tasks.</p><p class="tdlplm"><a href="/tasks#task-queue">Learn more</a></p></div></a>.

`tctl task-queue describe <modifiers>`

The Server records the last time a Worker sent a poll request.
Poll requests can last up to a minute, so a `LastAccessTime` less than a minute ago is normal.
If it's over a minute ago, then likely either the Worker is at capacity (all Workflow and Activity slots are full) or it has shut down.
Once it has been 5 minutes since the last poll request, the Worker will no longer appear on the list.

The following modifiers are supported and control the behavior of the command.
`--task-queue` is required.

- [--fields](/tctl-next/modifiers#--fields)
- [--namespace](/tctl-next/modifiers#--namespace)
- [--output](/tctl-next/modifiers#--output)
- [--task-queue](/tctl-next/modifiers#--task-queue)
- [--task-queue-type](/tctl-next/modifiers#--task-queue-type)
- [--time-format](/tctl-next/modifiers#--time-format)

## list-partition

The `tctl task-queue list-partition` command lists the partitions of a <a class="tdlp" href="/tasks#task-queue">Task Queue<span class="tdlpiw"><img src="/img/link-preview-icon.svg" alt="Link preview icon" /></span><div class="tdlpc"><p class="tdlppt">What is a Task Queue?</p><p class="tdlppd">A Task Queue is a first-in, first-out queue that a Worker Process polls for Tasks.</p><p class="tdlplm"><a href="/tasks#task-queue">Learn more</a></p></div></a> and the hostname for the partitions.

`tctl task-queue list-partition --task-queue <value>`

The following modifiers are supported and control the behavior of the command.
Always include required modifiers when executing this command.

- [--namespace](/tctl-next/modifiers#--namespace)
- [--output](/tctl-next/modifiers#--output)
- [--task-queue](/tctl-next/modifiers#--task-queue)
