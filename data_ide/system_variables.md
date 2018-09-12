# Supported system variables

You can use variables in path and parameter settings, you can also use variables directly in your SHELL script.


## Business-related variables

Before you start to use the service-related variables, note the following key concepts:

**Triggering time**： The time when a workflow is triggered. It can be the time when you manually trigger the workflow, or when the workflow is automatically triggered according to scheduling settings.

**Business date**: The date from which the data starts to be  processed by the workflow. Service date is generated based on the triggering time by deducting one day from the triggering time (because the batch job is performed against the data of yesterday by default). For example, when the triggering time is `2017-05-27 13:50:00`, and the scheduled cycle is one day. Then the business date is `2017-05-26`, meaning the data on `2017-05-26` will be processed at the triggering time of `2017-05-27 13:50:00`. With that said, if you want to process the data of the date 2018-03-01, you must set the triggering time to some time on 2018-03-02.

The following table explains the system variables by using `2017-05-27 13:50:00` as the example triggering time.

<table>
<thead>
<tr>
<th>Variable</th>
<th>Description</th>
<th>Format</th>
<th>Business Date</th>
<th>Variable Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>${last_week8}</td>
<td>- Using triggering time as the basis, indicates <strong>Last week</strong>。<br />- Using business date as the basis, indicates business date minus 6 days.</td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170520</td>
</tr>
<tr>
<td>${last_week10}</td>
<td>- Using triggering time as the basis, indicates <strong>Last week</strong>。<br />- Using business date as the basis, indicates business date minus 6 days.<br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-20</td>
</tr>
<tr>
<td>${cal_dt}</td>
<td>- Using triggering time as the basis, indicates <strong>yesterday</strong>。<br />- Using business date as the basis, indicates today.<br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-26</td>
</tr>
<tr>
<td>${cal_dt8}</td>
<td>- Using triggering time as the basis, indicates  <strong>yesterday</strong>。<br />- Using business date as the basis, indicates today.<br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170526</td>
</tr>
<tr>
<td>${ncal_dt}</td>
<td>Using triggering time as the basis, indicates <strong>today</strong>。<br />Using business date as the basis, indicates today+1.<br />Format: YYYY-MM-DD</td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-27</td>
</tr>
<tr>
<td>${ncal_dt8}</td>
<td>Using triggering time as the basis, indicates  <strong>today</strong>.<br />Using business date as the basis, indicates today+1.<br />Format: YYYYMMDD</td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170527</td>
</tr>
<tr>
<td>${end_day_this_month8}</td>
<td>Using business date as the basis, indicates <strong>last day of this month.</strong><br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170531</td>
</tr>
<tr>
<td>${end_day_this_month10}</td>
<td>Using business date as the basis, indicates <strong>last day of this month.</strong><br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-31</td>
</tr>
<tr>
<td>${first_day_this_month8}</td>
<td>Using business date as the basis, indicates <strong>first day of this month</strong>。<br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170501</td>
</tr>
<tr>
<td>${first_day_this_month10}</td>
<td>Using business date as the basis, indicates <strong>first day of this month</strong>。<br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-01</td>
</tr>
<tr>
<td>${first_day_last_month8}</td>
<td>Using business date as the basis, indicates <strong>first day of last month</strong>。<br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170401</td>
</tr>
<tr>
<td>${first_day_last_month10}</td>
<td>Using business date as the basis, indicates <strong>first day of last month</strong>。<br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-04-01</td>
</tr>
<tr>
<td>${last_day_last_month8}</td>
<td>Using business date as the basis, indicates <strong>last day of last month</strong>。<br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>2017-04-30</td>
</tr>
<tr>
<td>${last_day_last_month10}</td>
<td>Using business date as the basis, indicates <strong>last day of last month</strong>。<br /></td>
<td>YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>201704-30</td>
</tr>
<tr>
<td>${monday_next_week8}</td>
<td>Using business date as the basis, indicates <strong>next Monday</strong>。<br /></td>
<td>YYYYMMDD</td>
<td>2017-05-26<br /></td>
<td>20170529</td>
</tr>
<tr>
<td>${monday_next_week10}</td>
<td>Using business date as the basis, indicates <strong>next Monday</strong>。<br /></td>
<td>Format: YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-05-29</td>
</tr>
<tr>
<td>${30days_cal_dt}</td>
<td>Using business date as the basis, indicates <strong>30 days ago</strong>。<br /></td>
<td>Format: YYYY-MM-DD</td>
<td>2017-05-26<br /></td>
<td>2017-04-26</td>
</tr>
</tbody>
</table>

## Time related variables

The following table explains the time-related variables by using `2017-05-27 13:50:00` as the example triggering time.

<table>
<thead>
<tr>
<th>Variable</th>
<th>Description</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>${this_hour}</td>
<td>The hour when the workflow is triggered</td>
<td>2017-05-27 13:00:00</td>
</tr>
<tr>
<td>${unix_timestamp}</td>
<td>Unix time corresponding to the triggering time</td>
<td>1495864241</td>
</tr>
</tbody>
</table>

## Non-time related variables

<table>
<thead>
<tr>
<th>Variable</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td>${task_id}</td>
<td>Task ID of the current instance</td>
<td>2017-05-27 13:00:00</td>
</tr>
<tr>
<td>${instance_id}</td>
<td>Current instance ID</td>
<td>1495864241</td>
</tr>
<tr>
<td>${env.APP_CUSTOMER}</td>
<td>The group account who generated the instance</td>
<td>CLP</td>
</tr>
<tr>
<td>${env.APP_ID}</td>
<td>The App ID that the instance belongs to</td>
<td>a22b94f9-3b9d-40f6-9bd8-4d66b304d930</td>
</tr>
</tbody>
</table>
