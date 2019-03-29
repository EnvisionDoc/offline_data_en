# Configuring an Amazon S3 data connection

This topic instructs how to configure the connection to an Amazon S3  data connection.


## About this task
To synchronize data from an external Amazon S3 database for analysis, Create a data connection configuration that specifies the cloud region where the database sits in AWS, the credentials to use to access the S3 database, and other information about the data connection.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Connection** panel, click **Add Data Connection**.

3. In the **Data Connection** window, provide the following settings:

   - **Data Connection name**:  the name of the data connection. The name can be a combination of the following characters:
     - Chinese characters
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
     The maximum length of the data connection name is 50 characters.
   - **Data Connection type**: S3
   - **Region**: the cloud region of the S3 database.
   - **Access key ID**: the access key ID of the S3 database.
   - **Secret access key**: the access key to use to sign the requests sent to the S3 database.
   - **Data Connection description**: a description of the data connection.

4. Click **OK** to save the configuration.


## Results

After the connection is created, the data connection item is shown in the **Data Connection** table.

## What to do next

When the connection is successfully established, EnOS retrieves the data from the external data connection to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](https://www.envisioniot.com/docs/data-explorer/en/latest/creating_hivetable.html) .

You can then configure a data integration workflow to synchronize data from the connection to the target table in EnOS. For more information, see [Data Integration](../data_integration/index).
