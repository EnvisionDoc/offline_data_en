# Setting Filters

If there is a large amount of data, you can set filter conditions to filter out a specific or several kinds of data from the measure fields of the selected dataset. Multiple measures can be selected for filtering data.

The filter supports data of string or numeric type but does not support data of date type. To filter data of date type, you can use the **Query condition** control widget and select the "Date selection" control type.

The  following section introduces how to set filters using bar chart as example:

## String data type

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the bar chart |bar_icon| icon. The bar chart template is added to the report display section. Complete the data configuration under the **Data** tab.

3. For the **Filter** field, the drop-down list shows all the measure fields (except fields of date type) in the selected dataset.

4. Select a measure field of string type (taking "site name" as example).

5. Click the funnel |funnel| icon and complete the filtering condition in the pop-up dialog.

   .. image:: ../media/data_filter_string.png
      :width: 300px

6. After the filtering condition is set, click **OK**. The funnel icon will become a solid one |funnel_config| to indicate that the filter is set.

7. Click the **Update** button, and the system will refresh the data in the bar chart with the configured filter.

   .. note:: The data configuration will take effect only after you click the **Update** button.

8. After all configuration is completed, click **Save** in the tool bar to save the chart.

   .. note:: For data fields of character type, supported filtering conditions include equal to, not equal to, fuzzy match, and fuzzy dismatch.

## Numeric data type

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the bar chart |bar_icon| icon. The bar chart template is added to the report display section. Complete the data configuration under the **Data** tab.

3. For the **Filter** field, the drop-down list shows all the measure fields (except fields of date type) in the selected dataset.

4. Select a measure field of numeric type (taking "wind speed" as example).

5. Click the funnel |funnel| icon and complete the filtering condition in the pop-up dialog.

6. After the filtering condition is set, click **OK**. The funnel icon will become a solid one |funnel_config| to indicate that the filter is set.

7. Click the **Update** button, and the system will refresh the data in the bar chart with the configured filter.

   .. note:: The data configuration will take effect only after you click the **Update** button.

8. After all configuration is completed, click **Save** in the tool bar to save the chart.

   .. note:: For data fields of character type, supported filtering conditions include equal to, not equal to, greater than, greater than or equal to, less than, less than or equal to, and between.

.. |bar_icon| image:: ../media/bar_icon.png

.. |funnel| image:: ../media/funnel.png

.. |funnel_config| image:: ../media/funnel_config.png

<!--end-->
