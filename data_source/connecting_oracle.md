# Configuring an ORACLE data source

This topic instructs how to configure the connection to a ORACLE data source.

## About this task
To synchronize data from an ORACLE data source, create a data source configuration that specifies information about the ORACLE connection.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Source** panel, click **Add Data Source**.

3. In the **Data Source** window, provide the following settings:

   - **Data source name**:  the name of the data source. the name of the data source. The name can be a combination of the following characters:
     - Chinese characters
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
     The maximum length of the data source name is 50 characters.
   - **Data source type**: ORACLE
   - **Host name or IP address**: Enter the host name or IP address where the database is hosted.     
   - **Service Name or SID**: the Service name or the SID of the ORACLE.
   - **Port**: the port number. The default port is 1521.
   - **Username**: the user name to use to access the ORACLE.
   - **Password**: the password of the user name.
   - **Data source description**: a description of the data source.

4. Click **OK** to save the configuration.

## Results

After the connection is created, the data source item is shown in the **Data Source** table.

## What to do next

When the connection is successfully established, EnOS retrieves the data from the external data source to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](https://www.envisioniot.com/docs/data-explorer/en/latest/creating_hivetable.html).

You can then configure a data integration workflow to synchronize data from the data source to the target table in EnOS. For more information, see [Data Integration](../data_integration/index).
