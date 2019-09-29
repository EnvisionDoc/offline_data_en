# FAQs

#### Q: How to synchronize datasets when data sources are changed?

A: Open the dataset editing page and click the **Sync table structure** button. The dataset will be synchronized.

.. note:: Datasets that are created through SQL model do not support synchronizing table structure.

#### Q: How to add calculation fields (dimension/measure) in a dataset?

A: Open the dataset editing page and click **+** beside the Dimension/Measure section name. Optionally, click on any dimension/measure field and select **Create calculation field** from the menu.

In the pop-up dialog, enter customized expressions, values, or characters in the **Expression** field. Currently supported calculation logics include sum, avg, max, min, etc. See the following screen capture.

When editing the expression of the calculation field, note that only English punctuation symbols are allowed in SQL statements. Added calculation fields cannot be used as expressions in new calculation fields.

#### Q: Why is the report not refreshed after data configuration is completed?

A: After configuring data for a report in the **Chart and Control Configuration** section, you need to click the **Update** button to refresh data in the report.

#### Q: How to set the display format of measures in report?
A: Open the dataset editing page, click on a measure, navigate to **Data formatting** from the menu, and select a format for the measure.

#### Q: How to set data filter for a report?

A: Open the report editing page, create a report and complete data configuration. To set data filter, click the **Data** tab and choose a data field to be filtered from the drop-down list of the **Filter** section. Then, click the **Funnel** icon and specify the filtering conditions in the pop-up window.

.. note:: Filtering values must be separated by commas in English.

#### Q: In configuring a query condition control, why is the query result empty when it is associated with a chart and multiple fields?

A: When the query condition control is associated with a chart, usually select just one associated field. If multiple associated fields are selected, queries are made according to the unique minimum granularity filtering conditions. When there is no parent-child hierarchical logic in the associated fields, it might return empty query results.

#### Q: In configuring a query condition control, why is the query result empty when it is associated with multiple charts (with different fields)?

A: When the query condition control is associated with multiple charts, you must select a commonly associated field. Otherwise, the query result will be empty.

#### Q: When a chart is associated with a query condition control and has data filters, what is the priority of data filtering?

A: When the query condition control and the filter are associated with a same field, return the query results by the query condition control. When the query condition control and the filter are associated with different fields, both query conditions work and return query results.
