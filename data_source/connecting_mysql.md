# Configuring an SQL or MySQL Server Data Connection

This topic instructs how to configure the connection to an SQL or MySQL Server data connection.


## About This Task
To synchronize data from an external SQL or MySQL database for analysis, create a data connection configuration that specifies information about the data connection and the JDBC connection to the source database.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Connection** panel, click **Add Data Source**.

3. In the **Data Sources** window, provide the following settings:

   - **Data source**: Name of the data source. The maximum length of the data source name is 50 characters. The name can be a combination of the following characters:
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
   - **Data source type**: MYSQL   
   - **Host Name or IP Address**: Enter the host name or IP address where the database is hosted.
   - **Database Name**: the name that uniquely identifies to the database to connect.
   - **Port**: the port to access the database.
     EnOS uses the address, database name, and port to establish the JDBC connection from EnOS to the database.
   - **Username**: the user name to use to access the database.
   - **Password**: the password of the user name.
   - **Data Source Description**: a description of the data connection.

4. Click **OK** to save the configuration.


## Results

After the connection is created, the data connection item is shown in the **Data Connection** table.

## What to Do Next

When the connection is successfully established, EnOS retrieves the data from the external data connection to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](/docs/offline-data/en/latest/data_explorer/creating_hivetable.html).

You can then configure a data integration workflow to synchronize data from the data connection to the target table in EnOS. For more information, see [Data Integration](../data_integration/index).
