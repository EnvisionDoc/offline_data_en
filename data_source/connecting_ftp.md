# Configuring an FTP Data Connection

This topic instructs how to configure the connection to an FTP data connection.

## About This Task
To synchronize data from an external FTP data connection, create a data connection configuration that specifies information about the FTP connection.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Connection** panel, click **Add Data Source**.

3. In the **Data Sources** window, provide the following settings:

   - **Data source**: Name of the data source. The maximum length of the data source name is 50 characters. The name can be a combination of the following characters:
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
   - **Data source type**: FTP
     - **Type**: Whether to use FTP or FTPS as the protocol to connect to the data connection.   
     - **Mode**: The connection mode.
       - When you select the active mode, the FTP server initiates the connection.
       - When you select the passive mode, EnOS initiates the connection.
   - **IP Address**: The IP address of the FTP server.
   - **Encryption Mode**: When you select FTPS as the protocol, select whether to use explicit or implicit encryption mode.
   - **Encryption Type**: When you select FTPS as the protocol, select whether the FTP connection is over TLS or SSL.
   - **Port**: The port number to use for connection.
     - For FTP connection, the default port is 21.
     - For FTPS connection, the default port type for explicit transmission is 21 and for implicit transmission, 990.
   - **Username**: the user name to use to access the FTP server.
   - **Password**: the password of the user name.
   - **Data Source Description**: Enter description of the data connection.

4. Click **Test** to test the data source connection.

5. Click **OK** to save the configuration.

## Results

After the connection is created, the data connection item is shown in the **Data Connection** table.

## What to Do Next

When the connection is successfully established, EnOS retrieves the data from the external data connection to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](/docs/offline-data/en/latest/data_explorer/creating_hivetable.html).

You can then configure a data integration workflow to synchronize data from the data connection to the target table in EnOS. For more information, see [Data Integration](../data_integration/index).
