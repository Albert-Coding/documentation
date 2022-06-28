---
id: how-to-get-the-result-of-a-workflow-execution-in-python
title: How to get the result of a Workflow Execution in python
sidebar_label: Workflow Execution result
description: Workflow Execution result
tags:
  - developer-guide
  - python
---

Use [`start_workflow()`](https://python.temporal.io/temporalio.client.client#start_workflow) or [`get_workflow_handle()`](https://python.temporal.io/temporalio.client.client#get_workflow_handle) to return a Workflow handle.
Then use the method, [`result`](https://python.temporal.io/temporalio.client.workflowhandle#result) to await on the result of the Workflow.

```python
handle = await client.start_workflow(
    YourWorkflow.run, "some arg", id="your-workflow-id", task_queue="your-task-queue"
)

# Wait for result
result = await handle.result()
print(f"Result: {result}")
```

You can use [`get_workflow_handle()`](https://python.temporal.io/temporalio.client.client#get_workflow_handle), or [`get_workflow_handle_for()`](https://python.temporal.io/temporalio.client.client#get_workflow_handle_for) for type safety, and to get a handle for an existing Workflow by its Id.

Then use [`describe()`](https://python.temporal.io/temporalio.client.workflowhandle#describe) to get the current status of the Workflow. This will fail if the Workflow does not exist.