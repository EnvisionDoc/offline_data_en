# Preparing Data Exploring Environment

Before using EnOS Data Explorer with Zeppelin Notebook and Jupyter Notebook, you need to request the data explorer sandbox resource on EnOS Console.

## Requesting Sandbox Resource

Take the following steps to request data explorer sandbox resource:

1. Log in EnOS Console with OU administrator account and click **Resource Management** from the left navigation panel.

2. Under the **Data Analytics** tab, click the **Request Resource** button for Data Explorer.

3. Enter the sandbox name, select the appropriate CPU, memory, and storage based on business needs, and click the **Request** button.

   .. image:: media/sandbox.png

After the sandbox resource request is approved, and the status of the request becomes to *Allocated*, you can start using the data explorer.

## Managing Sandbox Resource

After the data explorer sandbox resource is allocated, select **Data Explorer** from the left navigation panel of EnOS Console. Find the requested sandbox and click the **Start** icon from the **Operations** column. When the status of the sandbox becomes to *Running*, you can click Zeppeline or Jupyter in the **URL** column to open the corresponding notebook.

If you do not need to use the data explorer sandbox resource, you can click the **Stop** icon in the **Operations** column to stop the sandbox. When the sandbox is stopped, delete the requested sandbox resource on the **Resource Management** page on EnOS Console.

<!--end-->