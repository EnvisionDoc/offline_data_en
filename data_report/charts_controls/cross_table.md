# Cross Table

Cross table consists of rows and columns, and it can be used to display and group the aggregated values of a field in a table.

## Configuration

Cross table supports 0 or multiple dimensions and 0 or multiple measures. Cross table does not support multi-chart association.

Before creating a report, you must have datasets created. Take the following steps to configure settings for the cross table.

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Cross Table** icon |crosstable_icon|. The cross table template is added to the report display section.

3. Under the **Data** tab, select a dataset to be used from the drop-down list of the **Dataset** field.

4. From the drop-down list of the **Row (Dimension)** and **Column (Measure)** fields, select the corresponding data fields to be used for the cross table. For the Measure filed, click the eye icon to hide the selected measure field.

5. For the **Page Set** field, select the page size for the cross table. Available options are 50, 100, 200, and 500.

6. If **Default not load data** is selected, no data will be loaded when you click the **Update** button. Only if non-empty query condition is configured, you can click **Query** to load data for the cross table. If **Default not load data** is not selected, the cross table will load date when you click the **Update** button.

7. Click the **Update** button. The cross table will be refreshed to display the selected data.

   .. note:: The data configuration will take effect only after you click the **Update** button.

8. If you want to set a data filter, see [Setting Filters](filter).

9. To set automatic data refresh, enter an interval value in the **Refresh** field. The minimum value supported is 5 seconds.

   .. image:: ../media/crosstable_data.png

10. After data configuration is completed, you can set the layout of the cross table under the **Style** tab, including **Common** and **Design** configuration. The style settings take effect in real time.

    - Checkbox for displaying title

    - Checkbox for displaying border

    - Checkbox for displaying serial number

      .. image:: ../media/cross_style.png

11. Cross table does not support multi-chart association.

12. In the report display section, you can set the sequencing order of fields, rows and columns to be displayed, column width, and page size of the table.

13. To view the chart data or download data, click the |chart_spread| icon in the upper right corner of the chart and click **View data** > **Download**. Optionally, click **Delete** to delete the chart.

14. After all configuration is completed, click **Save** in the tool bar to save the chart.

.. |crosstable_icon| image:: ../media/crosstable_icon.png

.. |chart_spread| image:: ../media/chart_spread.png

<!--end-->
