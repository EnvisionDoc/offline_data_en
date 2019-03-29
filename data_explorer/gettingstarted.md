# Getting started with Data Explorer

A typical flow to use Data Explorer to explorer data is as follows:

## Step 1: Create a new note

1. Click **Data Explorer** from the left navigation panel of EnOS Console.

2. Click **New note**.

3. In the **New Note** window, enter the name of the notebook and select the note type.

4. Click |enter_note| to enter the note and begin your work.

.. image:: media/gettingstarted_1.gif

## Step 2: Program and run your codes with interpreter

To invoke an interpreter, enter `%<interpreter_name>` (percent). The following table lists the supported interpreters and how to invoke.

.. note:: After you select a note type in Step 1, the corresponding interpreter is automatically associated so that you don't need to invoke the interpreter using the percent sign again. However, if you want to invoke another interpreter other than what you specified in Step 1, you can use the syntax as shown in the following table.


.. list-table::
   :widths: auto

   * - Interpreter
     - `%<interpreter_name>`
   * - hive
     - %hive
   * - spark
     - %livy.spark
   * - pyspark
     - %livy.pyspark
   * - markdown
     - %md
   * - mysql
     - %mysql_report
   * - python
     - %python
   * - shell
     - %sh

.. image:: media/gettingstarted_2.gif

## Step 3: Visualize data

Choose the built-in types of charts to assistant you to analyze your data.

The following screenshot shows an example pie chart that visualizes the composition of a group of people in terms of education level.

You can switch other grouping criteria such as **job** or **age** or **marital**.

.. image:: media/data_explorer_pic_2.png

.. |enter_note| image:: media/enter_note.png

<!--end-->
