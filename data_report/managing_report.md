# Managing Reports

After a report is created, it will be listed in the table on the **Report** page. Select **Data Report > Report** from the left navigation panel and manage your reports as needed. You can preview, edit, rename, copy, publish/offline, delete a report, or view published reports.

## Report List

Reports are classified and displayed as **Mine** and **All**, according to the creator of reports.

Reports created by the current user are listed under the **Mine** tab.

Reports created by the current user and by other users in the organization (also published as open within the organization) are listed under the **All** tab. You can view the published reports created by other users in the organization. See the following screen capture.

.. image:: media/report_operation.png


## Report Editing Page

From the list of created reports, click the **Edit** icon of a report to open the report editing page. See the following screen capture.

.. image:: media/report_edit.png


The report editing page consists of 3 parts, the chart and control configuration section, the report display section, and the tool bar.

**Chart and Control Configuration Section**

Based on your business needs, select a chart or control to be used by double-clicking the chart icon or control icon. You can also edit the chart title, set data filters, and configure multi-chart association.

Data Report service provides a rich set of charts, including bar charts, line charts, pie charts, cross tables, scatter charts, indicating blocks, gauges, and highlight tables, which can satisfy various data visualization requirements. After adding a chart to the report display section, click the **Data** tab and select a dataset and the corresponding values for the dimension and measure. Then, click the **Style** tab and configure the layout and display of the table. Optionally, click the **Advanced** tab and configure multi-chart association (if application) for the report.

**Report Display Section**

In the report display section, you can change the position of a chart or control by drag and drop the chart or control, and adjust the size by dragging the |modify_component_size| icon in the lower right corner of a chart or control.

.. |modify_component_size| image:: media/modify_component_size.png

To quickly change the type of a chart/control in the report display section, simply select the chart/control and click another chart/control in the configuration section. The selected chart/control will be replaced.

Click on the white area of the report display section, you can complete global settings of whether to show the paging line when exporting the report to PDF.

**Tool Bar**

On the tool bar, you can save, save as, preview, publish, rename, publish the report, and export the report as PDF.

The report name supports English and Chinese, with a limit of 50 characters.

## Previewing a Report

Before publishing a report, you can have a preview of the report to check its display effect. Save the report and click the **Preview** button. The report preview page is open. You can check the preview result and choose to export the report as PDF.

You have 2 options to preview a report:

- On the page of report list, click the **Preview** icon of a report.
- On the report editing page, click the **Preview** button in the tool bar.

.. image:: media/report_preview.png


## Publishing / Offline a Report

**Publishing a Report**

When report editing is completed, you can publish the report as visible to the whole organization or to the owner only. After the report is published, a URL is generated for it. With the URL and user account verification, users can view the report online without logging in to the EnOS Console and entering the Data Report service.

If "Only the user" is selected, the published report is visible to the report owner only; if "Organization public" is selected, the report is visible to all users in the organization.

.. image:: media/report_publish.png
   :width: 400px


To view a published report, click the report name in the report list. To view reports that are public in the organization, click the **All** tab on the Report page.

You have 2 options to publish a report:

- On the report list page, expand the |rdataset_menu_extend| icon for a report draft and select **Publish**.
- On the report editing page, click the **Publish** button on the tool bar.

**Making a Report Offline**

You can make a published report offline if needed. When a report is offline, the URL that was generated for accessing the report will expire automatically.

On the report list page, expand the |rdataset_menu_extend| icon for a published report and select **Offline**. When a report is offline, accessing the report with the report URL will get a message indicating that the link has expired.

.. |rdataset_menu_extend| image:: media/dataset_menu_extend.png

## Reverting to Published Version

To avoid impact of editing on published reports, each published report has the following two versions of configuration:

- Version in editing mode: A version being edited and saved on the report editing page.
- Version in published mode: A version been saved and published.

The scenario of using this feature is as follows:

When editing a published report on the report editing page, if you are not satisfied with the editing effect, you want to roll back the configuration of the published report. Click **More** > **Revert to published version** and click **Confirm**. Then the published version will replace the editing version of the report, and you can continue editing the report.

## Exporting a Report to PDF

**Exporting as PDF**

Reports can be exported as PDF to your local workstation and saved in the download directory of the browser.

You have 3 options to export a report as PDF:

- On the report editing page, click **More** > **Export PDF**.
- On the report preview page, click the |report_download| icon in the upper right corner.
- On the report viewing page, click the |report_download| icon in the upper right corner.

.. |report_download| image:: media/report_download.png

**Show Paging Line**

The report content is automatically paginated in the exported PDF file. If the report content exceeds a page,  a chart might be split into two parts. To ensure the integrity and quality of the exported report, Data Report service provides a global setting for showing paging lines.

Click on the white area of the report display section, the global setting is displayed in the configuration section. Select the **Show Paging Line** checkbox, a dashed line is displayed in the report display section as the paging line. You can adjust the size of the chart for the paging line. When the report is export as PDF, the report will be divided into pages according to the location of the paging line. See the following screen capture.

.. image:: media/report_pageline.png


## Viewing a Published Report

Select **Data Report** > **Report** from the left navigation panel and click the name of a published report on the report list page. The published report is displayed on a new page.

Under the **All** tab, you can view reports created by other users in the organization and published as public within the organization. Click the report name to view the report content.

## Renaming a Report

Select **Data Report** > **Report** from the left navigation panel to open the report list.

You have 2 options to rename a report:

- On the report list page, click the **Rename** icon for a target report and enter the new name in the pop-up dialog.
- On the report editing page, enter the new name for the report on the tool bar.

A report name can be used repeatedly and it supports English and Chinese characters, with a limit of 50 characters.

## Copying a Report

Select **Data Report** > **Report** from the left navigation panel to open the report list.

On the report list page, expand the menu |dataset_menu_extend| and select **Copy**. The system will generate a copy of the report and add suffix "copy" to the name of the report.

## Deleting a Report

Select **Data Report** > **Report** from the left navigation panel to open the report list.

On the report list page, expand the menu |dataset_menu_extend| and select **Delete**. Click **OK** when prompted to delete the report.

.. |dataset_menu_extend| image:: media/dataset_menu_extend.png

## Related Information

- [Creating Reports](creating_report)
