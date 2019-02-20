# About EnOS Offline Analytics

EnOS Offline Analytics Service is mainly targeted for the batch processing of _data at rest_ to obtain insights from the data. 

Batch processing is used in a variety of scenarios, from simple data transformations to a more complete ETL (extract-transform-load) pipeline. In a big data context, batch processing may operate over very large data sets, where the computation takes significant time. Batch processing typically leads to further interactive exploration, provides the modeling-ready data for machine learning, or writes the data to a data store that is optimized for analytics and visualization. One example of batch processing is to transform a large set of flat, semi-structured CSV or JSON files into a schematized and structured format that is ready for further querying. Typically the data is converted from the raw formats used for ingestion (such as CSV) into binary formats that are more performant for querying because they store data in a columnar format, and often provide indexes and inline statistics about the data.

EnOS Offline Analytics Service provides end-to-end toolset that enables you to load your data from various of data sources into a unified analytical datastore in EnOS, process the data through orchestrating workflows, and quickly and interactively analyze the data. The scalable cloud cluster of EnOS allows you to process huge amount of data on demand.

## Targeted Personas

EnOS Offline Analytics Service primarily serves the following roles:

**Data Developer & Analyst**

Whose responsibilities are to:

- Develop data structure and algorithm
- Perform data analysis and data mining
- Design BI reports based on business KPIs to assist business decisions


## Key Capabilities

**Data integration**

The service provides an data integrator that helps you synchronize data between extensive heterogeneous data sources, such as to synchronize structured data from source databases to the Hive database in EnOS Cloud and from EnOS Cloud to external target databases. [Learn more >>](data_integration/di_overview).

**ETL (extract-transform-load)**

EnOS Offline Analytics Service provides a GUI-based Data IDE that enables batch data processing based on scheduled workflows. The batch processing operations supported various from simple data transformations to complete ETL (extract-transform-load). The IDE also provides common libraries out-of-the-box for most frequently used data processing operations. [Learn more >>](data_ide/dataide_overview)

**Data exploration**

Based on the open-source Apache Zeppelin project, EnOS Offline Analytics Service provide a light-weighted, notebook based data explorer that lowers the barrier for data processing, and enables data-driven, collaborative, interactive data analytics. [Learn more >>](https://www.envisioniot.com/docs/data-explorer/en/latest/dataexplorer_overview.html)


## Related Services of EnOS Offline Analytics

**EnOS Report**

Provides interactive drag-and-drop user interface that lowers the barrier of acquiring, processing, and analyzing data and help you build data analysis reports rapidly and avoid duplicate efforts in front-end development. [Learn more >>](https://www.envisioniot.com/docs/analysis-report/en/latest/report_overview.html)


## Next Steps

Learn how to use the Offline Analytics service for batch data processing.

- [Getting Started With Offline Analytics](gettingstarted)