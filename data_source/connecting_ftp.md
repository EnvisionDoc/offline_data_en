# Configuring an FTP data source

This topic instructs how to configure the connection to an FTP data source.

## About this task
To retrieve data from an external FTP data source, create a data source configuration that specifies information about the FTP connection.

## Procedure

1. In the EnOS Console, click **Data Source** from the left navigation panel.

2. In the **Data Source** panel, click **Add Data Source**.

3. In the **Data Source** window, provide the following settings:

   - **Data source name**:  The name of the data source. the name of the data source. The name can be a combination of the following characters:
     - Chinese characters
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
     The maximum length of the data source name is 50 characters.
   - **Data source type**: FTP
     - **Protocol**: Whether to use FTP or FTPS as the protocol to connect to the data source.   
     - **Mode**: The connection mode.
       - When you select the active mode, the FTP server initiates the connection.
       - When you select the passive mode, EnOS initiates the connection.
   - **IP address**: The IP adderss of the FTP server.
   - **Encryption mode**: When you select FTPS as the protocol, select whether to use explicit or implicit encrytion mode.
   - **Encryption type**: When you select FTPS as the protocol, select whether the FTP connection is over TLS or SSL.
   - **Port**: The port number to use for connection.
     - For FTP connection, the default port is 21;
     - For FTPS connection, the default port type for explicit transmission is 21 and for implicit transmission, 990.
   - **Username**: the user name to use to access the FTP server.
   - **Password**: the password of the user name.
   - **Data source description**: a description of the data source.

4. Click **OK** to save the configuration.

## Results
<!---
可选，描述完成procedure以后的正确结果，以及如何verify结果正确。简单task可省略该部分
-->

After the connection is created, the data source item is shown in the **Data Source** table.

## What to do next
<!---
可选，若该操作结束通常伴有下一操作，则简要描述后续操作，并提供链接到后续操作对应的task topic
-->
When the connection is successfully established, EnOS retrieves the data from the external data source to the EnOS internal Hive database. You must create the Hive table to store the retrived data. For more information, see [Creating Hive table](../data_explorer/creating_hivetable).
