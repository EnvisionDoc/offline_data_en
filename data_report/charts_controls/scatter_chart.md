# Scatter Chart

Scatter chart can be used to show the distribution and aggregation of data.

## Configuration

Scatter chart supports 1 or multiple dimensions and 2 measures.

Before creating a report, you must have datasets created. Take the following steps to configure settings for the scatter chart.

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Scatter chart** icon |scatter_icon|. The scatter chart template is added to the report display section.

3. Under the **Data** tab, select a dataset to be used from the drop-down list of the **Dataset** field.

4. From the drop-down list of the **Category (Dimension)**, **X Axis (Measure)** and **Y Axis (Measure)** fields, select the corresponding data fields to be used for the scatter chart.

5. If **Default not load data** is selected, no data will be loaded when you click the **Update** button. Only if non-empty query condition is configured, you can click **Query** to load data for the cross table. If **Default not load data** is not selected, the cross table will load date when you click the **Update** button.

6. Click the **Update** button. The scatter chart will be refreshed to display the selected data.

   .. note:: The data configuration will take effect only after you click the **Update** button.

7. If you want to set a data filter, see [Setting Filters](filter).

8. To set automatic data refresh, enter an interval value in the **Refresh** field. The minimum value supported is 5 seconds.

   .. image:: ../media/scatter_data.png

9. After data configuration is completed, you can set the layout of the scatter chart under the **Style** tab, including **Common** and **Design** configuration. The style settings take effect in real time.

   - Checkbox for displaying title

   - Checkbox for displaying border

   - Checkbox for displaying tooltip

   - Titles for the X axis and Y axis, supporting Chinese, English, and special characters with a limit of 50.

   - Setting for the position of legend (Top, Bottom, Left, or Right).

   - Configuring auxiliary lines for analyzing data in the scatter chart. Currently, the linear function (y = kx + b) is supported, where "y" is dependent variable, "x" is the parameter, "k" is the slope, and "b" is the intercept.

     .. image:: ../media/scatter_style.png

10. After style configuration is completed, you can set multi-chart association under the **Advanced** tab.

11. To view the chart data or download data, click the |chart_spread| icon in the upper right corner of the chart and click **View data** > **Download**. Optionally, click **Delete** to delete the chart.

12. After all configuration is completed, click **Save** in the tool bar to save the chart.

.. |scatter_icon| image:: ../media/scatter_icon.png

.. |chart_spread| image:: ../media/chart_spread.png

<!--end-->
