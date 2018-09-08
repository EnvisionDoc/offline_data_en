# Creating a hive table

This topic instructs how to create a hive table through Data Explorer.


## About this task
The data retrived from external data sources needs to be stored as Hive tables to be consumed by other EnOS data processing functions. You'll need to create the Hive table by using the Data Explorer.

## Procedure

1. In the EnOS Console, click **Data Explorer** from the left navigation panel.

2. In the **Data Explorer** panel, import or create a note.
   - If you already have a note created with table creation script included, click **Import Note**.
   - If you want to create a note, click **Create New Note**.

3. In the notebook, enter the commands to create the table. For example,
```
create table if not exists dpdw_dim_site_full(
	site_id string,
	site_name string,
	capacity string,
	equipment_amount string,
	air_denity string,
	area string,
	state_name string
) comment 'wind domain dimension table'
```
For more information about the commands, see [Apache Hive documentation on table creation](https://cwiki.apache.org/confluence/display/Hive/LanguageManual+DDL#LanguageManualDDL-CreateTable).


4. Click **OK** to save the configuration.


## Results
<!---
可选，描述完成procedure以后的正确结果，以及如何verify结果正确。简单task可省略该部分
-->



## What to do next
<!---
可选，若该操作结束通常伴有下一操作，则简要描述后续操作，并提供链接到后续操作对应的task topic
-->
If you are creating the Hive table to store data from external data source, you'll then need to map columns in data source to the Hive table through the Data Integration function.

## Reference information
<!---
可选，若该操作结束通常伴有下一操作，则简要描述后续操作，并提供链接到后续操作对应的task topic
-->
