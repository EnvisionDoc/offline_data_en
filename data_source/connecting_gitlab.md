# Configuring a GitLab Data Connection

This topic instructs how to configure the connection to a GitLab data connection.


## About This Task

To synchronize data from a GitLab project, create a data connection configuration that specifies information about the GitLab server and token.

## Procedure

1. In the EnOS Console, click **Data Connection** from the left navigation panel.

2. In the **Data Connection** panel, click **Add Data Source**.

3. In the **Data Sources** window, provide the following settings:

   - **Data source**: Name of the data source. The maximum length of the data source name is 50 characters. The name can be a combination of the following characters:
     - a through z
     - A through Z
     - 0 through 9
     - _ (underscore)  
   - **Data source type**: GitLab
   - **Token**: Enter the Access Token for visiting the GitLab repository. Steps for getting the Access Token are as follows:
     - Login GitLab project, click the **User** drop-down list in the upper right corner, and select **Settings**.
     - On the **User Settings** page, select **Access Tokens** from the left navigation bar.
     - Enter a name for the Access Token to be created, select an expiring date, select the `api`, `read_user`, `read_repository` permission options, and click **Create personal access token**.
     - In the **Your New Personal Access Token** field, copy the generated Access Token.
   - **Git URL**: Enter the URL of the GitLab project, with the format of `http://git.{domain-name}.com`.
   - **Data Source Description**: Enter description of the data connection.

4. Click **Test** to test the data source connection.

   .. image:: ../media/gitlab_connection.png

5. Click **OK** to save the configuration.

## Results

After the connection is created, the data connection item is shown in the **Data Connection** table.


## What to Do Next

When the connection is successfully established, you can retrieve data from the external data connection to the EnOS internal Hive database. You must create the Hive table to store the retrieved data. For more information, see [Creating Hive table](/docs/offline-data/en/latest/data_explorer/creating_hivetable.html).
