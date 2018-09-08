# Data integration overview

The data integration function supports synchronizing data between extensive heterogeneous data sources.

The major use case of data integration is to help data developers to synchronize structured data from source databases to the Hive Library in EnOS.

The data integration function only supports synchronization of structured data, that is data which can be abstracted as two-dimensional tables. Unstructured data such as MP3 is not supported by data integration. However, you can schedule SHELL tasks in a workflow to synchronize the unstructured data. For information about unstructured data synchronization, see [xxx](.../data_ide/...)

The data integration function does not provide complex data logic processing or data flow consumption.

## Scenarios

The typical scenarios of data integration are as follows:
- One-time synchronization of full set of data
- Periodical synchronization of incremental data
