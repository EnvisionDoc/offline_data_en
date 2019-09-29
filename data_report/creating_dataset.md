# Creating Datasets

After data source tables are created, you can create datasets by single table model or SQL model. A dataset is a logical table connected with the data source table. It can be referenced directly in the report design phase, so that you can focus on the report design instead of caring about the underlying logical processing of the source tables.

## Prerequisites

Before creating datasets, ensure that data source tables have already been created. For details, see [Managing Data Source](managing_datasource).

## Procedure

Log in the EnOS Console, select **Data Report > Data** from the left navigation, and choose the **Data Sources** tab. Currently, you can create datasets with 2 options. Click **Switch to table** or **Switch to SQL** in the upper right corner of the page to switch the method of creating datasets.

### Single Table Model

1. On the **Data Sources** page, select a data source table from the list on the right. Then, click the |new_dataset| icon from the operation panel to create dataset.

2. Click the **Datasets** tab and view information about the created dataset under the **Mine** tab.

### SQL Model

By SQL model, you can create datasets based on multiple data source tables.

1. On the **Data Sources** page, click **Switch to SQL**.

2. In the editor, define the `Select` SQL statements.

3. Click **Syntax check** to verify the syntax validity of the SQL query statements.

4. Enter the dataset name and click **Create dataset** to complete creating the dataset.

5. Click the **Datasets** tab and view information about the created dataset under the **Mine** tab.

## Results

After the dataset is created, the system sets fields of `Int` type as the Measure field by default, and sets fields of `String` or `Datatime` type as the Dimension field by default.

## Follow-up Operations

You can create a report based on the created datasets. For details, see [Creating a Report](creating_report).

## Related Information

- [Managing Datasets](managing_dataset)

.. |new_dataset| image:: media/new_dataset.png

<!--end-->
