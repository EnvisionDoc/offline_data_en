# Data Report overview

EnOS Data Report is a lightweight intelligent analysis servicethat is oriented to the energy sector. It aims to lower the threshold for user data analysis and to quickly complete visual presentation.

Primarily intended for data analysts and developers, Data Report provides full lifecycle functions from data connection, dataset generation, to data visualization. Data Reports can be inserted to your operation system or can exist as independent portals. You can quickly build data analysis reports through interactive drag-and-drop operation. Its reporting platform helps lower the cost and threshold to acquire, process, and analyze data, and thereby avoid duplicate efforts in front-end development.

## Key benefits

The built-in Data report function of EnOS brings the following benefits:

- **Seamless data integration**: seamlessly integrates EnOS cloud databases and supports multiple data sources such as MySQL and postgreSQL.
- **Seamless component integration**: seamlessly interfaces with EnOS energy component libraries to provide abundant data visualization charts and controls that meet visualization requirements for different business scenarios.
- **Front-end integration**: rapidly integrated into the EnOS built-in front-end framework or business portal for rapid creation of data portals.
- **Security**: provide control over data security on the basis of the platform’s sound IAM authority system.

## Key concepts

The basic objects in a reporting platform include data sources, datasets and reports, as described below:

- **Data source**: Before making a report, you need to prepare the data or specify the data source where raw data is located. Data Report automatically associates corresponding data sources according to your permissions in the EnOS System. Currently, the supported data source is MySQL. For more information about data source, see [Data source management](/docs/offline-data/en/latest/data_source/datasource_overview.html).

- **Dataset**: Once a data source is connected, simple logical processing based on one or more data source tables can be performed to get a logic table that has a connection to the source tables. The logical table is a dataset. The dataset can be referenced directly in the report design. So that you can focus on the design instead of caring about the underlying logical processing of the source tables.

- **Report**: Your report contents can be customized in a WYSIWYG way by dragging the chart to adjust the layout according to business needs. A report may contain a variety of analysis charts and controls. Filtering, multi-chart association, and other advanced operations are also supported.

	.. image:: media/101.png

<!--end-->
