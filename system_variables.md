# Supported System Variables

You can use variables in path and parameter settings, you can also use variables directly in your SHELL script.

## Business-related Variables

Before you start to use the service-related variables, note the following key concepts:

### Triggering time

The time when a workflow is triggered. It can be the time when you manually trigger the workflow, or when the workflow is automatically triggered according to scheduling settings.

### Business date

The date from which the data starts to be processed by the workflow. Service date is generated based on the triggering time by deducting one day from the triggering time (because the batch job is performed against the data of yesterday by default). For example, when the triggering time is `2017-05-27 13:50:00`, and the scheduled cycle is one day. Then the business date is `2017-05-26`, meaning the data on `2017-05-26` will be processed at the triggering time of `2017-05-27 13:50:00`. With that said, if you want to process the data of the date 2018-03-01, you must set the triggering time to some time on 2018-03-02.

The following table explains the system variables by using `2017-05-27 13:50:00` as the example triggering time.

.. list-table::
   :widths: 15 40 20 15 10

   * - Variable
     - Description
     - Format
     - Business Date
     - Variable Value
   * - ${last_week8}
     - + Using triggering time as the basis, indicates Last week.
       + Using business date as the basis, indicates business date minus 6 days.
     - YYYYMMDD
     - 2017-05-26
     - 20170520
   * - ${last_week10}
     - + Using triggering time as the basis, indicates Last week.
       + Using business date as the basis, indicates business date minus 6 days.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-20
   * - ${cal_dt}
     - + Using triggering time as the basis, indicates yesterday.
       + Using business date as the basis, indicates today.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-26
   * - ${cal_dt8}
     - + Using triggering time as the basis, indicates yesterday.
       + Using business date as the basis, indicates today.
     - YYYYMMDD
     - 2017-05-26
     - 20170526
   * - ${cal_dt-n}
     - + Using triggering time as the basis, indicates n+1 days before today.
       + Using business date as the basis, indicates n days before today.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-25
   * - ${cal_dt8-n}
     - + Using triggering time as the basis, indicates n+1 days before today.
       + Using business date as the basis, indicates n days before today.
     - YYYYMMDD
     - 2017-05-26
     - 20170525
   * - ${ncal_dt}
     - + Using triggering time as the basis, indicates today。
       + Using business date as the basis, indicates today+1.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-27
   * - ${ncal_dt8}
     - + Using triggering time as the basis, indicates today.
       + Using business date as the basis, indicates today+1.
     - YYYYMMDD
     - 2017-05-26
     - 20170527
   * - ${end_day_this_month8}
     - Using business date as the basis, indicates last day of this month.
     - YYYYMMDD
     - 2017-05-26
     - 20170531
   * - ${end_day_this_month10}
     - Using business date as the basis, indicates last day of this month.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-31
   * - ${first_day_this_month8}
     - Using business date as the basis, indicates first day of this month.
     - YYYYMMDD
     - 2017-05-26
     - 20170501
   * - ${first_day_this_month10}
     - Using business date as the basis, indicates first day of this month.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-01
   * - ${first_day_last_month8}
     - Using business date as the basis, indicates first day of last month.
     - YYYYMMDD
     - 2017-05-26
     - 20170401
   * - ${first_day_last_month10}
     - Using business date as the basis, indicates first day of last month.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-04-01
   * - ${last_day_last_month8}
     - Using business date as the basis, indicates last day of last month.
     - YYYYMMDD
     - 2017-05-26
     - 20170430
   * - ${last_day_last_month10}
     - Using business date as the basis, indicates last day of last month.
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-04-30
   * - ${monday_next_week8}
     - Using business date as the basis, indicates next Monday。
     - YYYYMMDD
     - 2017-05-26
     - 20170529
   * - ${monday_next_week10}
     - Using business date as the basis, indicates next Monday。
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-05-29
   * - ${30days_cal_dt}
     - Using business date as the basis, indicates 30 days ago。
     - YYYY-MM-DD
     - 2017-05-26
     - 2017-04-26
   * - ${hcal_dt8}
     - Using business date and time as the basis, indicates 1 hour ago. Variable value is the current date.
     - YYYYMMDD
     - 2017-05-26 00:30:00
     - 20170525
   * - ${cal_hr}
     - Using business date and time as the basis, indicates 1 hour ago. Variable value is the current hour-level number.
     - HH
     - 2017-05-26 00:30:00
     - 23

## Time related variables

The following table explains the time-related variables by using `2017-05-27 13:50:00` as the example triggering time.

.. list-table::
   :widths: 25 35 40

   * - Variable
     - Description
     - Value
   * - ${this_hour}
     - The hour when the workflow is triggered
     - 2017-05-27 13:00:00
   * - ${unix_timestamp}
     - Unix time corresponding to the triggering time
     - 1495864241


## Non-time related variables

.. list-table::
   :widths: 25 40 35

   * - Variable
     - Description
     - Example
   * - ${task_id}
     - Task ID of the current instance
     - 2017-05-27 13:00:00
   * - ${instance_id}
     - Current instance ID
     - 1495864241
   * - ${env.APP_CUSTOMER}
     - The group account who generated the instance
     - CLP
   * - ${env.APP_ID}
     - The App ID that the instance belongs to
     - a22b94f9-3b9d-40f6-9bd8-4d66b304d930

<!--end-->
