# Monitoring Manual Workflow Instances

For a manual worflow, you can perform the following monitoring actions:
- Viewing the workflow instance
- Pre-running the workflow
- Pre-running a selected task in the workflow
- Pre-running a selected task and the subsequent tasks of the task

## Viewing a Manual Workflow

You can view general information about a workflow and the detailed information about each task that is run in the workflow.

To view a manual workflow, do the following steps:
1. From the navigation panel, click **Workflow Operation** > **Manual Scheduling**. A table of all workflows that you have access to is shown in the right panel.

2. (Optional) In the search field above the table, enter the task ID or name to filter to result shown in the table.

3. Click the name of the workflow that you want to inspect details for from the table. A workflow panel is shown.

4. For each task node in the workflow, you can double-click the task node to view the following details:

   - Attributes: settings of the task that is defined at the design time

   .. image:: media/workflow_attributes.png
      :alt: Figure: Task attributes in the workflow monitor


   - Task contents: what's run in the task. What's shown in the Task Contents tab varies according to the task type. The content of a data integration task might look something like this:

   .. image:: media/workflow_taskcontents.png
      :alt: Figure: Task contents in the workflow monitor


   While an SHELL task content would be something like this:

   .. image:: media/workflow_taskcontents2.png
      :alt: Figure: Task contents in the workflow monitor


## Pre-running a Manual Workflow

To manually trigger a workflow, click **Pre-run** from the **Operations** column of the workflow and set the triggering time.

## Pre-running a Task

To manually trigger a task within the manual workflow:

1. Click the name of the workflow from the table.

2. In the workflow panel, right-click the task and click **Pre-run** and set the triggering time.
