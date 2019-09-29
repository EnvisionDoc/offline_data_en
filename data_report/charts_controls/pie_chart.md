# Pie Chart

Pie chart is used to show a series of data, each of which has a unique color or pattern. Pie chart can show the size and percentage of each data item in the sum of all data items, for example, the proportion of wind turbines of different brands.

Pie chart consists of multiple sectors. The label of each sector is defined by the data dimension, and the size of each sector is defined by the data measure.

## Configuration

Pie chart supports 1 dimension and 1 measure.

Before creating a report, you must have datasets created. Take the following steps to configure settings for the pie chart.

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Pie chart** icon |pie_icon|. The pie chart template is added to the report display section.

3. Under the **Data** tab, select a dataset to be used from the drop-down list of the **Dataset** field.

4. From the drop-down list of the **Sector Label (Dimension)** and **Sector Angle (Measure)** fields, select the corresponding data fields to be used for the pie chart.

5. Click the **Update** button. The pie chart will be refreshed to display the selected data.

   .. note:: The data configuration will take effect only after you click the **Update** button.

6. If you want to set a data filter, see [Setting Filters](filter).

7. To set automatic data refresh, enter an interval value in the **Refresh** field. The minimum value supported is 5 seconds.

   .. image:: ../media/pie_data.png

8. After data configuration is completed, you can set the layout of the pie chart under the **Style** tab, including **Common** and **Design** configuration. The style settings take effect in real time.

   - Checkbox for displaying title

   - Checkbox for displaying border

   - Checkbox for pie chart style (default or hollow)

   - Setting for the label style, including "None", "Label", "Labe, value", "Lable, percentage", and "Label, value(percentage)".

   - Titles for the horizontal axis and vertical axis, supporting Chinese, English, and special characters with a limit of 50.

   - Checkbox for displaying tooltip

   - Setting for the position of legend (Top, Bottom, Left, or Right).

     .. image:: ../media/pie_style.png

9. After style configuration is completed, you can set multi-chart association under the **Advanced** tab.

10. In the report display section, click on the legend to set whether to display the measure values.

    .. image:: ../media/pie_legend.png
       

11. To view the chart data or download data, click the |chart_spread| icon in the upper right corner of the chart and click **View data** > **Download**. Optionally, click **Delete** to delete the chart.

12. After all configuration is completed, click **Save** in the tool bar to save the chart.

.. |pie_icon| image:: ../media/pie_icon.png

.. |chart_spread| image:: ../media/chart_spread.png

<!--end-->
