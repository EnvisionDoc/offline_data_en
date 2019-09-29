# Configuring an Azure BLOB Data Connection

This topic instructs how to configure the connection to an Azure BLOB data connection.


## About This Task
To synchronize data from an external Azure BLOB database for analysis, create a data connection configuration that specifies the cloud region where the database sits in Azure, with the storage account and password to access the BLOB database, and other information about the data connection.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Connection** panel, click **Add Data Source**.

3. In the **Data Sources** window, provide the following settings:

   - **Data source**: Name of the data source. The maximum length of the data source name is 50 characters. The name can be a combination of the following characters:
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)
   - **Data source type**: BLOB
   - **Region**: the cloud region of the BLOB database.
   - **Storage Account**: the storage account to access the BLOB database.
   - **Password**: the password of the storage account.
   - **Data Source Description**: the description of the data connection.

4. Click **OK** to save the configuration.


## Results

After the connection is created, the data connection item is shown in the **Data Connection** table.

## What to Do Next

When the connection is successfully established, EnOS retrieves the data from the external data source to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](/docs/offline-data/en/2.0.8/data_explorer/creating_hivetable.html) .

<!--

You can then configure a data integration workflow to synchronize data from the connection to the target table in EnOS. For more information, see [Data Integration](../data_integration/index).

-->
