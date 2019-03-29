# Data Processing

Data developers can use Data IDE to process data through scheduling workflows.

## Key Concepts

The following key concepts are involved in the data development process.

### Workflow

A workflow is an automatic data processing flow that comprises  _tasks_, _references_, and _relations_. A workflow is a directed acyclic graph (DAG), ring is not accepted in a workflow.
A workflow can be scheduled to run for one time only or periodically.

### Task

A task is the fundamental element of the workflow. A task defines how to process the data. By running a task, the  _resource_ associated with the task is run. Data IDE function provides two types of tasks:
- Data integration task: a data integration task will synchronize external data connection into EnOS hive library. For more information, see [Data integration](../data_integration/index).
- SHELL task: a task that runs SHELL script.

### Reference

A reference is a task or workflow that plays as the prerequisite of its succeeding tasks. A reference must be the root node of a workflow. A workflow can have more than one reference. Regardless of the scheduling settings of a task, the task is not run until its reference is run.

### Relation

An upstream task connects to a downstream task through relation. The relation is uni-directional.

### Resource

A resource is the script that is run by the SHELL-type of task. The supported resource formats are: `sh`, `jar`, `sql`, `hql`, `xml`, `zip`, `tar`, and `tar.gz`.

## Stages of Data Development

The data development process falls into the following stages.

### Configuration Time  

At the configuration time, you create a workflow that comprises tasks to run, and pre-run the workflow to verify whether the workflow works as designed.

### Run Time  

At the run time, workflow runs according to the scheduling parameters.

### Monitor Time  

At the monitor time, you can re-run a single task node or re-run a node and its subsequent nodes to pinpoint issues with the workflow.

The following figure shows an example workflow with reference. In this example, the following facts are true:

1. Task 1 and Task 2 are not run untill the reference is run.

2. If the workflow is periodic, all tasks are run at each cycle as defined by the scheduling parameters.

3. `True` and `False` applies only at the monitor time when you re-run a task.

   - When `True`, the subsequent task is run.
   - When `Faulse`, the subsequent task is not run.

   .. image:: media/workflow_reference.png
      :alt: Figure: Workflow concepts



## Major Functionalities

The Data IDE toolkit provides the following major functionalities:

### Workflow Development

According to your business requirements, your can design a workflow that comprises multiple tasks, and each task performs certain actions on your data.

### Job Resource

You can register your scripts as resources and manage the version of the resources. The resources can then be referenced by tasks in a workflow.

## Usage Scenarios

The typical user scenarios of using Data IDE for data development are as follows:

### Running a Built-in Script

EnOS provides built-in scripts for the most frequently used data processing activities, such as synchronizing the master data from HDFS to an external S3 database, or converting columns to rows. For a complete list of built-in scripts that EnOS provides, see [Common library](../common_library).

The major procedure of running a built-in script is as follows:

1. Browse the Common Library tree and locate the script that you want to run.

2. Double-click the version of the script and review the details about the script.

   .. image:: ../media/scenario_built-in.png
      :alt: Figure: Built-in script


3. Click **Use the Program**.

4. In the pop-out window, provide settings about the workflow.

   .. image:: ../media/built-in_workflow.png
      :alt: Figure: Workflow with bulit-in script


5. Provide the scheduling settings. For more information, see [Creating a one-time workflow](creating_workflow_onetime) or [Creating a periodic workflow](creating_workflow_periodic).


### Running an External Script

The major procedure of running an external script is as follows:
1. Upload your script as a resource on EnOS. For more information, see [Creating a resource](creating_resource).

2. Create a workflow with a SHELL-type of task that references the resource. For more information, see [Creating a one-time workflow](creating_workflow_onetime) or [Creating a periodic workflow](creating_workflow_periodic) according to your needs.

EnOS provides sample code to help you streamline this procedure, for more information, see [https://github.com/EnvisionBigdata/dataide_external_script](https://github.com/EnvisionBigdata/dataide_external_script).
