# Configuring an Amazon S3 data source

This topic instructs how to configure the connection to an Amazon S3  data source.


## About this task
To retrieve data from an external Amazon S3 database for analysis, Create a data source configuration that specifies the cloud region where the database sits in AWS, the credentials to use to access the S3 database, and other information about the data source.

## Procedure

1. In the EnOS Console, click **Data Source** from the left navigation panel.

2. In the **Data Source** panel, click **Add Data Source**.

3. In the **Data Source** window, provide the following settings:

   - **Data source name**:  the name of the data source. The name can be a combination of the following characters:
     - Chinese characters
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
     The maximum length of the data source name is 50 characters.
   - **Data source type**: S3
   - **Region**: the cloud region of the S3 database.
   - **Access key ID**: the access key ID of the S3 database.
   - **Secret access key**: the access key to use to sign the requests sent to the S3 database.
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
