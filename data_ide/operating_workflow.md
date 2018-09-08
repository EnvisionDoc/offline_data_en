# Operating a workflow

## Pre-running a workflow

After creating a task, you can run the **Pre-run** action to check the operations and results of the code.

- In a periodic task, pre-run is designed to test code logic.
- In a one-time task, each operation needs to be manually triggered, that is, to be realized by pre-run.


1. Click **Pre-run** and the following page will pop up. You need to select the task trigger time; or rather, you must select the desired task execution time.

   **Note:**

   - If a time before the current system time is selected as the trigger time, the task will be executed immediately to generate a running instance (viewable through the task operation and maintenance). When the task instance is running, the trigger time is regarded as the business time and transmitted to the time parameter for business computing.
   - Only one instance for the same workflow is allowed to run at a time. If the pre-run instance conflicts with the running instance, you need to wait for executions in sequence.


2. Click **OK**, and the workflow instance ID will be displayed in the upper right corner of the page.


3. You can then view the instance information in the task monitor.


## Exporting a workflow

From the directory tree, select the workflow and click **Export**.

A file with the `.workflow` extension is downloaded to your local file system. An exported configuration file contains the configuration information, scheduling information, and resource packages that are used in the workflow.




## Monitor time
