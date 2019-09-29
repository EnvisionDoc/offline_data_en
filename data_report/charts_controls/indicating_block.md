# Indicating Block

Indicating block consists of labels and indicators. It is used to show the changes of index data, which can assist decision making.

## Configuration

Indicating block supports 0 or 1 dimension and 1 or multiple measures. When no dimension is selected, it does not support multi-chart association. When 1 dimension is selected, it supports multi-chart association.

Before creating a report, you must have datasets created. Take the following steps to configure settings for the indicating block.

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Indicating block** icon |index_icon|. The indicating block template is added to the report display section.

3. Under the **Data** tab, select a dataset to be used from the drop-down list of the **Dataset** field.

4. From the drop-down list of the **Sector Label (Dimension)** and **Sector Angle (Measure)** fields, select the corresponding data fields to be used for the indicating block.

5. Click the **Update** button. The indicating block will be refreshed to display the selected data.

   .. note:: The data configuration will take effect only after you click the **Update** button.

6. If you want to set a data filter, see [Setting Filters](filter).

7. To set automatic data refresh, enter an interval value in the **Refresh** field. The minimum value supported is 5 seconds.

   .. image:: ../media/index_data.png

8. After data configuration is completed, you can set the layout of the indicating block under the **Style** tab, including **Common** and **Design** configuration. The style settings take effect in real time.

   - Checkbox for displaying title

   - Checkbox for displaying border

   - Select the layout style

   - Set the number of blocks of each row (4 by default)

     .. image:: ../media/index_style.png

9. After style configuration is completed, you can set multi-chart association under the **Advanced** tab. Note that when no dimension is selected, indicating block does not support multi-chart association. When 1 dimension is selected, it supports multi-chart association.

10. To view the chart data or download data, click the |chart_spread| icon in the upper right corner of the chart and click **View data** > **Download**. Optionally, click **Delete** to delete the chart.

11. After all configuration is completed, click **Save** in the tool bar to save the chart.

.. |index_icon| image:: ../media/index_icon.png

.. |chart_spread| image:: ../media/chart_spread.png

<!--end-->
