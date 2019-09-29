# Managing Datasets

Log in the EnOS Console, select **Data Report > Data** from the left navigation, and choose the **Datasets**. You can view the information of datasets to which you have access. You can edit, rename, copy, or delete datasets. For datasets that are created by the SQL model, you can modify the SQL statements.

## Datasets

### Querying Datasets

Under the **Datasets** tab, you can view information about datasets that are classified by groups of **Mine** and **All**. See the following screen capture.

.. image:: media/dataset_list.png

- Under the **Mine** tab, you can view datasets that you created and datasets that you copied from the **All** tab, which are created by other users in the organization. You can edit, rename, copy, and delete datasets under the **Mine** tab.
- Under the **All** tab, you can view all datasets that you created and datasets that are created by other users in the organization. You can only view and copy datasets that are created by other users.

.. note:: You cannot rename or delete datasets that that are created by other users in the organization. To edit and create reports based on these datasets, you can copy them and operate on the copy.

### Renaming Datasets

Dataset name can be letters and special characters, with a limit of 50 characters. A dataset name can used repeatedly.

You have the following 2 options to rename a dataset:

- On the page of dataset list, click the **Rename** icon |rename_dataset|, enter the new name in the pop-up dialog, and click **Confirm**.
- Open the dataset editing page, enter the new name on the toolbar, and click **Save**.

### Deleting Datasets

On the page of dataset list, select **Delete** from the extended operation list |dataset_menu_extend| and click **Confirm** in the pop-up dialog.

.. note:: Reports that are associated with the deleted dataset will also be deleted. That is, the associated report will have empty data.

.. |rename_dataset| image:: media/rename_dataset.png

.. |dataset_menu_extend| image:: media/dataset_menu_extend.png

### Copying Datasets

On the page of dataset list, select **Copy** from the extended operation list |dataset_menu_extend|. The system will create a copy of the dataset, with `_copy` as suffix of the new dataset name.

### Editing Datasets

On the page of my dataset list, click the Edit |edit_dataset| button, and edit the dataset information. See the following screen capture.

.. |edit_dataset| image:: media/edit_dataset.png

.. image:: media/dataset_edit_overview.png


The dataset editing page can be divided into 3 sections:
- **Dimension / Measure editing section**

  The fields in a dataset can be classified as dimension and measure types. You can edit the dimensions and measures based on the requirements of creating reports.

- **Toolbar section**

  After the dataset editing is completed, click **Save** or **Save as** to save the dataset information.

  - **Preview data**: Preview data of the dataset in the data preview section.
  - **Sync table structure**: Synchronize new table fields from the data source tables. When the data source table changes, if new fields are added, the new fields can be easily synchronized. If fields in the data source table are deleted or changed, they will not be synchronized.

    .. note:: The "sync table structure" function supports datasets that are created by single table model, but does not support datasets that are created by SQL model.

- **Data preview section**

  Display data preview of the dataset, with a limit of 20 records.

#### Editing Dimensions

From the list of dimensions, click on the target dimension field, and select the operation to perform from the menu.

- **Edit**
  - For native fields generated when creating datasets, you can update the name and comment.
  - For dimension fields created when editing datasets, you can update the name, statement, data type, and comment.

  Dimension name supports multiple language letters and special characters, with a limit of 50 characters.

- **Delete**

  Delete the selected dimension field.

  .. note:: Reports associated with the deleted dimension will also be deleted.

- **Clone dimension**

  Copy a dimension quickly. Generated dimension will have `_copy` as suffix in its name.

- **Create calculation field (Dimension)**

  There are 2 options to create a dimension field:
  - Click **+** beside the Dimension section name.
  - Click **Create calculation field (Dimension)** from the extended menu.

  In the pop-up dialog, enter customized expressions, values, or characters in the **Expression** field. Currently supported calculation logics include sum, avg, max, min, etc. See the following screen capture.

  .. image:: media/new_dimension.png


- **Convert to measure**

  Convert the selected dimension field to a measure field.

- **Switch the dimension type**

  Supporting the switch of default and date types. Supported date formats are as follows:

  .. image:: media/edit_dimension.png


#### Editing Measures

From the list of measures, click on the target measure field, and select the operation to perform from the menu.

- **Edit**
  - For native fields generated when creating datasets, you can update the name and comment.
  - For measure fields created when editing datasets, you can update the name, statement, data type, and comment.

  Measure name supports multiple language letters and special characters, with a limit of 50 characters.

- **Delete**

  Delete the selected measure field.

  .. note:: Reports associated with the deleted measure will also be deleted.

- **Create calculation field (Measure)**

  There are 2 options to create a measure field:

  - Click **+** beside the Measure section name.
  - Click **Create calculation field (Measure)** from the extended menu.

  In the pop-up dialog, enter customized expressions, values, or characters in the **Expression** field. Currently supported calculation logics include sum, avg, max, min, etc.

- **Convert to dimension**

  Convert the selected measure field to a dimension field.

- **Data formatting**

  Specify the data format of the measure field.

- **Default aggregation method**

  Select the default aggregation method for the measure field. The supported aggregation methods include sum, count, max, min, and avg.

  .. image:: media/edit_measure.png


### Modifying SQL Statements

For datasets that are created with the SQL model, you can modify the SQL statements.

1. On the page of dataset list, select **Modify SQL** from the extended operation list |dataset_menu_extend|.

2. In the editor, modify the SQL statements, and click **Syntax check**.

3. If there are no syntax errors, click **Save dataset** to complete modifying SQL statements.

## Related Information

- [Creating Datasets](creating_dataset)
