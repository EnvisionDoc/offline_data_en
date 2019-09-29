# About EnOS Data Analytics

EnOS Data Analytics Service is mainly targeted for the batch processing of _data at rest_ to obtain insights from the data.

Batch processing is used in a variety of scenarios, from simple data transformations to a more complete ETL (extract-transform-load) pipeline. In a big data context, batch processing may operate over very large data sets, where the computation takes significant time. Batch processing typically leads to further interactive exploration, provides the modeling-ready data for machine learning, or writes the data to a data store that is optimized for analytics and visualization. One example of batch processing is to transform a large set of flat, semi-structured CSV or JSON files into a schematized and structured format that is ready for further querying. Typically the data is converted from the raw formats used for ingestion (such as CSV) into binary formats that are more performant for querying because they store data in a columnar format, and often provide indexes and inline statistics about the data.

EnOS Data Analytics Service provides end-to-end toolset that enables you to load your data from various of data connection into a unified analytical datastore in EnOS, process the data through orchestrating workflows, and quickly and interactively analyze the data. The scalable cloud cluster of EnOS allows you to process huge amount of data on demand.


## Key Capabilities

**Data integration**

The service provides an data integrator that helps you synchronize data between extensive heterogeneous data connection, such as to synchronize structured data from source databases to the Hive database in EnOS Cloud and from EnOS Cloud to external target databases. [Learn more >>](data_integration/di_overview)

**ETL (extract-transform-load)**

EnOS Data Analytics Service provides a GUI-based Data IDE that enables batch data processing based on scheduled workflows. The batch processing operations supported various from simple data transformations to complete ETL (extract-transform-load). The IDE also provides common libraries out-of-the-box for most frequently used data processing operations. [Learn more >>](data_ide/dataide_overview)

**Data exploration**

Based on the open-source Apache Zeppelin project, EnOS Data Analytics Service provide a light-weighted, notebook based data explorer that lowers the barrier for data processing, and enables data-driven, collaborative, interactive data analytics. [Learn more >>](data_explorer/dataexplorer_overview)

**Data report**

Provides interactive drag-and-drop user interface that lowers the barrier of acquiring, processing, and analyzing data and help you build data analysis reports rapidly and avoid duplicate efforts in front-end development. [Learn more >>](data_report/report_overview)

## Targeted Personas

EnOS Data Analytics Service primarily serves the following roles:

**Data Developer & Analyst**

With the Data Analytics Service, data developers and analysts can develop data structure and algorithm, perform data analysis and data mining, and design BI reports based on business KPIs to assist business decisions.

## Related Services of EnOS Data Analytics

### Data Asset Management Service

EnOS Data Asset Management service enables you to define the asset calculation logic, subscribe to the asset data, and perform data calculations based on the predefined calculation logic for your organization. For example, calculating a 5-minute average of the measurement points or a 10-minute average, and etc. [Learn more >>](/docs/data-asset/en/2.0.9/data_asset_overview.html)


## Next Steps

Learn how to use the Data Analytics Service for batch data processing.

- [Getting Started with Data Analytics](gettingstarted)
