# Creating a Hive Table

This topic instructs how to create a Hive table through Data Explorer.


## About This Task
The data integrated from external data sources needs to be stored as Hive tables to be consumed by other EnOS data processing functions. You will need to create the Hive table by using the Data Explorer.

## Procedure

1. In the EnOS Console, click **Data Explorer** from the left navigation panel.

2. In the **Data Explorer** panel, import or create a note.

   - If you already have a note created with table creation script included, click **Import Note**.
   - If you want to create a note, click **New Note**.

3. If you chose to create a note in step 2, enter the URL of the note and select **hive** as the note type. For example, if you entered `yourname/hive/tablename` as the URL, a hive table with the name `tablename` is created under the `yourname/hive` directory.

3. Click the **Enter note** icon |Enter_note| from the directory tree. In the notebook, enter the commands to create the table. For example,

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


4. Click the **Run this paragraph** icon |Run_this_paragraph| . You will see your table created successfully as shown in the following screen capture:

   .. image:: media/create_hive.png


## Results
A table is created, and you can run a query to test the result.

```
%hive
select * from dw_meter_1h_demo limit 2
```

Run the query and you will get a result like this:

.. image:: media/test_query.png

## What to Do Next

If you are creating the Hive table to store data from external data source, you will then need to specify the table as a target and map columns from the data source to the target through Data Integration. For more information, see [Data Integration](../data_integration/index.html).

.. |Enter_note| image:: media/enter_note.png

.. |Run_this_paragraph| image:: media/run.png

<!--end-->
