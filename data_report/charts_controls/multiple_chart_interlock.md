# Multiple Chart Association

Under the **Advanced** tab of chart configuration, you can configure multi-chart association to realize associated query between charts.

**Prerequisites**

At least 2 reports that support multi-chart association have been created (with data configuration completed).

Taking the bar chart and pie chart as example, instructions on configuring multi-chart association are as follows.

1. Log in EnOS Console and select **Data Report** > **Report** > **New Report** to open the report editing page.

2. Double-click the **Bar chart** icon |bar_icon|. The bar chart template is added to the report display section. Under the **Data** tab, complete the data configuration for the bar chart.

3. Double-click the **Pie chart** icon |pie_icon|. The pie chart template is added to the report display section. Under the **Data** tab, complete the data configuration for the pie chart.

4. Select the bar chart, click the **Advanced** tab, and select the measure data field of the pie chart to be associated.

   .. image:: ../media/multi_correlation.png
      :width: 300px

.. |bar_icon| image:: ../media/bar_icon.png

.. |pie_icon| image:: ../media/pie_icon.png

.. note:: that when configuring multi-chart association, the measure data field of the chart that initiates the association will be the source field. The value of the source field will be used as filtering condition to query data in the chart that is associated. In this example, when selecting a measure value in the bar chart, the value will be used to filter data in the pie chart. The value in the pie chart that meets the filtering condition will be displayed.

**Results**

1. The bar chart initiates the association, and the measure is the source field. The pie chart is the associated chart, and the associated field is month. The multi-chart association is configured.

   .. image:: ../media/multi_correlation_before.png
      :width: 400px


2. In the bar chart, select 2017-12. The pie chart will display data for the month of 2017-12. See the following sample.

   .. image:: ../media/multi_correlation_after.png
      :width: 400px


<!--end-->
