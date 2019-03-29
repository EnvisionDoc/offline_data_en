# Getting Started with Offline Analytics
<!--
The short description should be a single, concise paragraph that contains one or two sentences and no more than 50 words.
Briefly mention what the user's learning goal is and include the following SEO keywords in the title short description: EnOS, ServiceName, tutorial.
-->

A typical flow to use EnOS to analyze your historical data is as follows:

.. image:: media/getting_started.png
   :alt: Figure: Four steps to get started with offline data processing


## Step 1: Prepare the data connection and target  

1. Prepare the data connection.

   - If the data connection is external, you'll first need to set up connection to the source data. EnOS supports to synchronize data from MYSQL, SQL, Oracle, FTP, SFTP, and Amazon S3 data connection. For information about how to connect to a specified database, see [Data Connection](data_source/datasource_overview).
   - If the data you want to process and analyze is on EnOS, such as the device master data accumulated and stored on EnOS. You can skip this substep.

2. Prepare the target Create a hive table hosted on EnOS to store the data synchronized from the data connection. For more information, see [Creating a hive table](https://www.envisioniot.com/docs/data-explorer/en/latest/creating_hivetable.html) in *Data Explorer*.

## Step 2: Synchronize the data from your data connection to EnOS

For external data connection, you can create data integration workflows from scratch or from importing existing workflows to synchronize your data. You can schedule one-time or periodical workflows as you need. For more information, see [Data integration](data_integration/index)

For master data synchronization, you can use the Data IDE function to create a workflow that uses the `SYNC_MDM` program. For more information, see [Data IDE](data_ide/dataide_overview).

## Step 3: Process the data

Use the Data IDE function to process your data, for example, converting columns to rows. EnOS provides rich data processing library that is ready to use.

For more information, see [Data IDE](data_ide/dataide_overview).

## Step 4: (Optional) Explore the data

Optionally, you can use the Data Explorer function to help you perform interactive data analytics and visualization before you start to use the data for further purposes such as dashboard and business intelligence. For more information, see [Data Explorer](https://www.envisioniot.com/docs/data-explorer/en/latest/dataexplorer_overview.html).
