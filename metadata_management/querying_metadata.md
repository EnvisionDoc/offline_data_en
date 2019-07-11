# Metadata Explorer 

Metadata Explorer provides a unified view of EnOS data warehouse metadata information. You can query the metadata of the Report DB tables and Hive tables. During development, data developers can centrally view the schema and attribute information of tables, thus assisting with the data development work.

## Querying Metadata of a Report DB Table

1. Log in EnOS Console and click **Metadata Explorer** from the left navigation panel.

2. In the navigation tree, click **Mysql** to extend the list of Report DB tables.

3. Select a table from the list, the metadata of the table is displayed in the right, including:

    - Table name

    - Path: Location of the table in the MySQL Report DB

    - Schema of the table, such as column identifiers, data type of each column, etc.

    - Properties of the table, such as identifier of the table, when the table is created, whether the table is compressed, etc. See the following example:

      .. image:: media/mysql_schema.png

## Querying Metadata of a Hive Table

1. Log in EnOS Console and click **Metadata Explorer** from the left navigation panel.

2. In the navigation tree, click **Hive** to extend the list of Hive tables.

3. Select a table from the list, the metadata of the table is displayed in the right, including:

   - Table name

   - Path: Location of the table in the Hive DB

   - Schema of the table, such as column identifiers, data type of each column, etc.

   - Properties of the table, such as identifier of the table, when the table is created, whether the table is compressed, etc. See the following example:

     .. image:: media/hive_schema.png