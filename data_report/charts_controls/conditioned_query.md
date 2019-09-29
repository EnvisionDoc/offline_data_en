# Query Condition

When creating reports, you can use the query condition control to set filters for querying data in one or multiple charts.

Currently, the query condition control supports control types such as input box, drop down selection, date selection, tree selection, and tile selection. Detailed filtering conditions are as follows:

.. list-table::
   :widths: auto

   * - Control Type
     - Filtering Condition
   * - Input box
     - Equal to, Not equal to, Greater than, Greater or equal, Less than, Less or equal, Between, Fuzzy match, Fuzzy mismatch
   * - Drop down selection
     - Equal to, Between
   * - Tile selection
     - Equal to, Between
   * - Tree selection
     - Between
   * - Date selection
     - Day range, Week range, Month range, Year range

The following sections introduce the usage of the query condition control by taking bar chart as example.

## Prerequisites

A report has been created with at least 1 chart (with data configuration completed).

## Concept

Data field association: When configuring the query condition control, you need to select a data field (measure) of the chart to be associated. The selected query condition will be used to filter data in the associated data field. In the following examples, after you specify a data field of the bar chart, the selected query conditions will filter data of the bar chart.

## Input Box

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Bar chart** icon |bar_icon| under the **Charts** tab. The bar chart template is added to the report display section. Complete the data configuration of the bar chart under the **Data** tab.

3. Double-click the **Query condition** icon |search_icon| under the **Controls** tab. The Query condition template is added to the report display section.

4. Under the **Condition config** tab, click **Add config**, and complete the query condition configuration in the pop-up window.

5. Enter query condition name (supporting Chinese, English, and special characters, with a limit of 50 characters).

6. Select the data field to be associated. Generally, select 1 measure field for each chart.

7. Select **Input box** from the Control type drop-down list and select **Equal to** as the filtering condition.

8. Click **OK** to complete the query condition configuration.

   .. image:: ../media/search_config_input.png
      :width: 400px

9. In the query condition control, enter the filtering keywords, and click the **Query** button. The bar chart will display the queried data.

   .. image:: ../media/search_legend_input.png
      :width: 450px

10. Select the query condition control, you can then edit or delete it, or add another query condition under the **Condition config** tab.

   .. image:: ../media/search_config_tab.png
      :width: 300px

11. After the query condition configuration is completed, you can set the layout of the query condition control under the **Style** tab. The style settings take effect in real time.

   - Checkbox for displaying title
   - Checkbox for displaying border

12. To delete the image control, select it first, click the |chart_spread| icon in the upper right corner of the control, and select **Delete**.

13. After all configuration is completed, click **Save** in the tool bar to save the query condition control.

## Drop Down Selection

1. Select the query condition control template and click **Add config** under the **Condition config** tab.

2. In the **Add config** pop-up window, complete the query condition configuration.

3. Enter query condition name (supporting Chinese, English, and special characters, with a limit of 50 characters).

4. Select the data field to be associated. Generally, select 1 measure field for each chart.

5. Select **Drop down selection** from the **Control type** drop-down list and select **Equal to** as the filtering condition.

6. Select **Manual input** for the **Select value** field and set filtering conditions.

7. Enter names of the filtering conditions (supporting Chinese, English, and special characters, with a limit of 50 characters).

8. Enter values of the filtering conditions, which will be used to filter data in the associated chart.

9. Click **+** to add new filtering conditions, click the arrow to change the order of the filtering conditions, and click Delete to remove filtering conditions.

10. Click **OK** to complete the query condition configuration.

   .. image:: ../media/search_config_dropdown.png
      :width: 400px

11. In the query condition control, select a filtering condition from the drop down list, and click the **Query** button. The bar chart will display the queried data.

   .. image:: ../media/search_legend_dropdown.png
      :width: 450px

12. Select the query condition control, you can then edit or delete it, or add another query condition under the **Condition config** tab.

   .. image:: ../media/search_config_tab.png
      :width: 300px

13. After the query condition configuration is completed, you can set the layout of the query condition control under the **Style** tab. The style settings take effect in real time.

   - Checkbox for displaying title
   - Checkbox for displaying border

14. To delete the image control, select it first, click the |chart_spread| icon in the upper right corner of the control, and select **Delete**.

15. After all configuration is completed, click **Save** in the tool bar to save the query condition control.

## Tile Selection

1. Select the query condition control template and click **Add config** under the **Condition config** tab.

2. In the **Add config** pop-up window, complete the query condition configuration.

3. Enter query condition name (supporting Chinese, English, and special characters, with a limit of 50 characters).

4. Select the data field to be associated. Generally, select 1 measure field for each chart.

5. Select **Tile selection** from the **Control type** drop-down list and select **Equal to** as the filtering condition.

6. Select **Manual input** for the **Select value** field and set filtering conditions.

7. Enter names of the filtering conditions (supporting Chinese, English, and special characters, with a limit of 50 characters).

8. Enter values of the filtering conditions, which will be used to filter data in the associated chart.

9. Click **+** to add new filtering conditions, click the arrow to change the order of the filtering conditions, and click Delete to remove filtering conditions.

10. Click **OK** to complete the query condition configuration.

   .. image:: ../media/search_config_tile.png
      :width: 400px

11. In the query condition control, click on a filtering condition and click the **Query** button. The bar chart will display the queried data.

   .. image:: ../media/search_legend_tile.png
      :width: 400px

12. Select the query condition control, you can then edit or delete it, or add another query condition under the **Condition config** tab.

   .. image:: ../media/search_config_tab.png
      :width: 300px

13. After the query condition configuration is completed, you can set the layout of the query condition control under the **Style** tab. The style settings take effect in real time.

   - Checkbox for displaying title
   - Checkbox for displaying border

14. To delete the image control, select it first, click the |chart_spread| icon in the upper right corner of the control, and select **Delete**.

15. After all configuration is completed, click **Save** in the tool bar to save the query condition control.

## Tree Selection

1. Select the query condition control template and click **Add config** under the **Condition config** tab.

2. In the **Add config** pop-up window, complete the query condition configuration.

3. Enter query condition name (supporting Chinese, English, and special characters, with a limit of 50 characters).

4. Select the data field to be associated. Generally, select 1 measure field for each chart.

5. Select **Tree selection** from the **Control type** drop-down list

6. Select a dataset for the **Select value** field and complete filtering conditions. At most 4 tree levels are supported.

7. Select a data field for the name and a data field for the value. Usually, the name field and the value field  are the same.

8. Click the |search_config_tree_cleanup| icon to remove the filtering condition.

9. Click **OK** to complete the query condition configuration.

   .. image:: ../media/search_cofig_tree.png
      :width: 400px

10. In the query condition control, select a filtering condition and click the **Query** button. The bar chart will display the queried data.

   .. image:: ../media/search_legend_tree.png
      :width: 400px

11. Select the query condition control, you can then edit or delete it, or add another query condition under the **Condition config** tab.

   .. image:: ../media/search_config_tab.png
      :width: 300px

12. After the query condition configuration is completed, you can set the layout of the query condition control under the **Style** tab. The style settings take effect in real time.

   - Checkbox for displaying title
   - Checkbox for displaying border

13. To delete the image control, select it first, click the |chart_spread| icon in the upper right corner of the control, and select **Delete**.

14. After all configuration is completed, click **Save** in the tool bar to save the query condition control.

## Date Selection

1. Select the query condition control template and click **Add config** under the **Condition config** tab.

2. In the **Add config** pop-up window, complete the query condition configuration.

3. Enter query condition name (supporting Chinese, English, and special characters, with a limit of 50 characters).

4. Select the data field to be associated. Generally, select 1 measure field for each chart.

5. Select **Date selection** from the **Control type** drop-down list and select **Month range** > **Last 3 months** for the value.

6. Click **OK** to complete the query condition configuration.

   .. image:: ../media/search_config_calendar.png
      :width: 400px

7. In the query condition control, select a filtering condition and click the **Query** button. The bar chart will display the queried data.

   .. image:: ../media/search_legend_calendar.png
      :width: 400px

8. Select the query condition control, you can then edit or delete it, or add another query condition under the **Condition config** tab.

   .. image:: ../media/search_config_tab.png
      :width: 300px

9. After the query condition configuration is completed, you can set the layout of the query condition control under the **Style** tab. The style settings take effect in real time.

   - Checkbox for displaying title
   - Checkbox for displaying border

10. To delete the image control, select it first, click the |chart_spread| icon in the upper right corner of the control, and select **Delete**.

11. After all configuration is completed, click **Save** in the tool bar to save the query condition control.

   .. note:: When **Date selection** control type is selected, the data type of the associated chart measure field must be date type, such as DATA, DATATIME, TIMESTAMP, TIME, and YEAR.

.. |bar_icon| image:: ../media/bar_icon.png

.. |search_icon| image:: ../media/search_icon.png

.. |search_config_tree_cleanup| image:: ../media/search_config_tree_cleanup.png

.. |chart_spread| image:: ../media/chart_spread.png

<!--end-->
