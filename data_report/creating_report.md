# Creating Reports

The report content can be customized in a WYSIWYG way by dragging the charts to adjust the report layout according to your business needs. The Data Report service applies flexible tiles layout to display the interaction of report data. A report may contain a variety of analysis charts and controls. Filtering, multi-chart association, and other advanced operations are also supported.

## Prerequisites

Before creating a report, ensure that the data preparation work is completed. See [Creating Datasets](creating_dataset).

## Creating a Report

1. Select **Data Report > Report** from the left navigation panel.

2. Click the **New Report** button to open the report **Editing** page.

3. Select a chart to be used from the **Charts** tab by double-clicking the chart icon.

4. Set advanced configurations like data filtering and multi-chart association.

5. Choose to publish the report within the organization or export the report as PDF.

### Using Charts

Based on business needs, use the following charts to create reports:

- [Bar Chart](charts_controls/bar_chart)
- [Line Chart](charts_controls/line_chart)
- [Pie Chart](charts_controls/pie_chart)
- [Cross Table](charts_controls/cross_table)
- [Indicating Block](charts_controls/indicating_block)
- [Gauge](charts_controls/gauge)
- [Scatter Chart](charts_controls/scatter_chart)
- [Highlight Table](charts_controls/highlight_table)

The configuration differences for the charts are as follows:

.. list-table::
   :widths: auto

   * - Chart Name
     - Number of Dimensions
     - Number of Measures
     - Supporting Multi-Chart Association
   * - Bar Chart
     - 1
     - 1 or more
     - Yes
   * - Line Chart
     - 1
     - 1 or more
     - Yes
   * - Pie Chart
     - 1
     - 1
     - Yes
   * - Cross Table
     - 0 or more
     - 0 or more
     - No
   * - Indicating Block
     - 0 or 1
     - 1 or more
     - Yes
   * - Gauge
     - 0
     - 1
     - No
   * - Scatter Chart
     - 1 or more
     - 2
     - Yes
   * - Highlight Table
     - 2 or more
     - 1
     - No


For details about configuring multi-chart association, see [Multiple Chart Association](charts_controls/multiple_chart_interlock).

If there is a large amount of data, you can set filters for a specific or several kinds of data. For details, see [Setting Filters](charts_controls/filter).

### Using Controls

Based on business needs, use the following controls to create reports:

- [Text Box](charts_controls/textbox)
- [iFrame](charts_controls/iframe)
- [Query Condition](charts_controls/conditioned_query)
- [Image](charts_controls/figure)

## Related Information

For detailed introduction to the charts and controls, see [Using Charts and Controls](charts_controls/index).
