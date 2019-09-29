# Getting Started with Zeppelin Notebook

A typical flow to use Zeppelin Notebook for data analytics is as follows:

## Step 1: Create a new note

1. Click **Data Explorer** from the left navigation panel of EnOS Console.

2. Find a sandbox with *Running* status and click **Zeppelin** from the **URL** column to open the Zeppelin notebook.

3. Click the **Create new note** button, enter a name for the note (or a name with path), select the default interpreter for the note, and click **Create**.

   .. image:: ../media/zeppelin_note.png

4. In the created note, enter script or notes to start your work.

     .. image:: ../media/creating_hive_table.png

   

## Step 2: Program and run your codes with interpreter

To invoke an interpreter, enter `%<interpreter_name>` (percent). The following table lists the interpreters that Zeppelin Notebook supports and how to invoke the interpreters.

.. note:: After you select a default interpreter in Step 1, the corresponding interpreter is automatically associated so that you do not need to invoke the interpreter using the percent sign again. However, if you want to invoke another interpreter, you can use the syntax as shown in the following table.


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

.. image:: ../media/gettingstarted_2.gif

## Step 3: Visualize data

Choose the built-in types of charts to assistant you to analyze your data.

The following screenshot shows an example pie chart that visualizes the composition of a group of people in terms of education level.

You can switch other grouping criteria such as **job** or **age** or **marital**.

.. image:: ../media/data_explorer_pic_2.png

## Step 4: Save code

Your code in Zeppelin Notebook will be saved by default in EnOS internal storage, unless the data explorer sandbox is deleted.

If you do not need to use the data explorer sandbox, you can either stop or delete it. Stopping a sandbox releases the computing resource only, but not the storage resource. Your notes and code will be retained in the storage. Deleting a sandbox releases both the computing resource and storage resource, and your notes and code will also be deleted.  

Before deleting a sandbox, you can use the following methods to save your notes and code:

1. Export the notebook and save it in your local storage. When needed, you can import the notebook again. 
2. Upload your code to a GitLab repository with the shell interpreter and Git commands.

<!--end-->