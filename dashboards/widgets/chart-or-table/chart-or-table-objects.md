# Objects

The Objects datasource counts camera detections of people, vehicles, and animals. Every time the camera's AI detects an object in the frame, that's recorded as a detection event. Use this datasource to track physical activity: how many times objects appeared in an area, how long they stayed, and how activity breaks down across time, location, or camera.

## Add the widget

1. Follow **Add a widget** in [Create and manage dashboards](../../create-and-manage-dashboards.md#add-a-widget) to open the widget list, then select **Chart or table**. The configuration dialog opens.
2.  Enter a name in the **Title** field.

    The title appears on the widget on the dashboard canvas. Use a name that identifies what the widget is tracking, for example "Main entrance detections today" or "Vehicle dwell time by hour."
3. Select **Objects** as the **Datasource**.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-datasource.png" alt="" width="313"></div>

4.  Select a **Visualization** type from the icon row. The preview panel updates immediately when you switch types.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-visualization-icons.png" alt="" width="263"></div>

    The preview tables below show each visualization type for both Appearance and Dwell Time. Use them to choose a chart format before continuing. You'll select between Appearance and Dwell Time in step 6 when you set the Y-Axis metric.

    If you selected **Number**, then skip to [Number visualization](chart-or-table-objects.md#number-visualization). If you selected **Table**, then skip to [Table visualization](chart-or-table-objects.md#table-visualization). For all other types, continue with step 5 below.

### Appearance

Appearance counts how many times objects were detected in the frame. The Y-axis label reads "Appearance total."

<table>
<thead>
<tr>
<th>Visualization type</th>
<th>Preview</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td><p><strong>Vertical bar chart</strong></p><p>Bars grouped by time period or category, vertical layout. Use this to compare detection counts across time intervals. For example, a bar peaking at 6:00 AM with 91 detections tells you that hour had the most activity. Click the bar to open the Object records view and see the actual camera frames from that hour.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-vertical-bar.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Horizontal bar chart</strong></p><p>Bars grouped by time period or category, horizontal layout. Use this when comparing many time periods or when hour labels are long. Click a bar to open the Object records for that period.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-horizontal.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Line chart</strong></p><p>A line connecting data points over time. Use this to track trends across a longer period, for example spotting a weekly pattern where activity spikes on weekday mornings. Click a data point to open the Object records for that time.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-line.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Vertical stacked bar chart</strong></p><p>Vertical bars split by object type, showing composition. Use this to see how people, vehicles, and animals each contribute to the total at each time interval. Click a segment to open the Object records for that object type and time.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-stacked-vertical.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Horizontal stacked bar chart</strong></p><p>Horizontal bars split by object type, showing composition. Use this for the same purpose as the vertical stacked chart when a horizontal layout suits your dashboard better.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-stacked-horizontal.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Number</strong></p><p>A single large count. Use this for a quick at-a-glance total, for example the total number of people detected today.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-number.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Table</strong></p><p>Data in rows and columns. Use this when you need precise values rather than a visual trend, or when you want to review exact counts per hour, location, or camera.</p></td>
<td align="center"><img src="../../../.gitbook/assets/widget-chart-viz-table.png" alt="" width="280"></td>
</tr>
</tbody>
</table>

The Appearance table shows detection counts. If you want to measure how long objects stayed in view instead, the Dwell Time table below shows the same visualization types using seconds as the unit.

### Dwell Time

Dwell Time measures how long objects remained in the camera's view, in seconds. The Y-axis label reads "Dwell Time average (seconds)."

<table>
<thead>
<tr>
<th>Visualization type</th>
<th>Preview</th>
</tr>
</thead>
<tbody>
<tr valign="top">
<td><p><strong>Vertical bar chart</strong></p><p>Bars grouped by time period or category, vertical layout. Use this to compare how long objects stayed in view across time intervals.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-vertical-bar.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Horizontal bar chart</strong></p><p>Bars grouped by time period or category, horizontal layout.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-horizontal-bar.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Line chart</strong></p><p>A line connecting data points over time. Use this to track how dwell time changes across a period.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-line.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Vertical stacked bar chart</strong></p><p>Vertical bars split by object type, showing how dwell time is distributed across people, vehicles, and animals.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-stacked-vertical.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Horizontal stacked bar chart</strong></p><p>Horizontal bars split by object type, showing dwell time composition.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-stacked-horizontal.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Number</strong></p><p>A single large dwell time value in seconds.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-number.png" alt="" width="280"></td>
</tr>
<tr valign="top">
<td><p><strong>Table</strong></p><p>Data in rows and columns with dwell time values per group or time interval.</p></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-dwell-table.png" alt="" width="280"></td>
</tr>
</tbody>
</table>

5. Set the **X-Axis**. The first dropdown controls how data is grouped.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-xaxis-dropdown.png" alt="" width="563"></div>

* **Time**: Groups data by time interval. A second dropdown appears where you set the interval.
* **Locations**: Groups data by location.
* **Cameras**: Groups data by camera name.

If you selected **Time**, then set the interval in the second dropdown.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-xaxis-interval.png" alt="" width="563"></div>

* `---`: No interval set. The widget determines the interval automatically.
* **Hour**: Groups data by hour.
* **Day**: Groups data by day.
* **Week**: Groups data by week.
* **Month**: Groups data by month.

6.  Set the **Y-Axis**. Three dropdowns control what is measured.

    First dropdown, aggregation:

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-aggregation.png" alt="" width="563"></div>

* **Total**: The sum of all detections across the period. For example, 1,817 total appearances recorded today.
* **Average**: The mean detection count per time unit. For example, an average of 3 appearances per hour.
* **Max**: The highest detection count recorded in any single time unit. For example, the busiest hour had 11 appearances.

Second dropdown, metric:

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-metric.png" alt="" width="563"></div>

* **Appearance**: Counts how many times objects were detected appearing in the frame.
* **Dwell Time**: Measures how long objects remained in the camera's view, in seconds.

Third dropdown, object filter:

* **All objects**: Includes every detected object type.
* **Group**: Filters by broad category. Select **Person**, **Vehicle**, **Animal**, **Shopping cart**, **Container**, or use **Select all** for all.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-group.png" alt="" width="563"></div>

* **Individual**: Filters by specific detected subjects, such as Unknown person, Adult male, or Bus. The options shown depend on what your cameras have detected.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-individual.png" alt="" width="563"></div>

7. Select the **Cameras** field to choose which cameras contribute data.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-camera-field.png" alt="" width="375"></div>

* Search by camera name or location using the search field.
* Select **All cameras** to include every camera in your account.
* Select individual cameras to filter to specific ones.
* Select **Select** to apply. The field shows how many cameras are selected, for example "1 cameras selected."

8. Optionally, set a widget-level **Time** range. If you leave this as `---`, then the widget follows the dashboard time filter.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-time-dropdown.png" alt="" width="375"></div>

> **Note:** Setting a widget-level time disconnects the widget from the dashboard time filter. To reconnect it, then clear the widget's time setting back to `---`.

9. Select **Add**. The widget appears on the dashboard canvas.

When you click on a data point in the chart, Lumana opens the Object records view for that time period, showing the actual camera frames that contributed to that count.

<table>
<thead>
<tr>
<th>Object records</th>
<th>Record detail</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><p>Results for the period you clicked in the chart.</p><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-records-view.png" alt="" width="400"></td>
<td align="center"><p>Frame and detections for a selected time.</p><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-records-live.png" alt="" width="400"></td>
</tr>
</tbody>
</table>

## Number visualization

If you selected Number in step 4, three unlabelled dropdowns replace the X-Axis and Y-Axis fields. The number on the canvas changes based on what you select in each dropdown.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-number-aggregation.png" alt="" width="563"></div>

The first dropdown controls the metric:

* **Appearance**: Counts how many times objects were detected in the frame.
* **Dwell Time**: Measures how long objects remained in view, in seconds. If no dwell time data has been recorded for the selected cameras and time range, the widget displays 0.

The second dropdown controls aggregation: how the number is calculated across the selected time range and cameras.

* **Total**: The sum of all detections. For example, 1,817 total appearances recorded today.
* **Average**: The mean detection count per time unit. For example, an average of 3 appearances per hour.
* **Max**: The highest count in any single time unit. For example, the busiest hour had 11 appearances.

<table>
<thead>
<tr>
<th>Total</th>
<th>Average</th>
<th>Max</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-number-total.png" alt="" width="280"></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-number-average.png" alt="" width="280"></td>
<td align="center"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-number-max.png" alt="" width="280"></td>
</tr>
</tbody>
</table>

The third dropdown controls the object filter:

* **All objects**: Counts every detected object type.
* **Group**: Counts by broad category. Select **Person**, **Vehicle**, or **Animal**, or use **Select all** for all three.
* **Individual**: Counts specific detected subjects such as Unknown person, Adult male, or Bus.

When Dwell Time is selected and no data has been recorded, the widget displays 0:

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-viz-number-dwell-config.png" alt="" width="563"></div>

Once you've set the three dropdowns, continue with step 7 to select cameras.

## Table visualization

If you selected Table in step 4, the X-Axis becomes **Group** and the Y-Axis becomes **Column**.

**Group** controls how rows are organized. The first dropdown sets the grouping type: **Time**, **Locations**, or **Cameras**.

* **Time**: A second dropdown appears where you set the interval: Hour, Day, Week, or Month. Each row in the preview is a time bucket, for example the first column is labelled **Hour** when that interval is selected.
* **Locations**: No second dropdown. Each row is a location that has data in the selected range.
* **Cameras**: No second dropdown. Each row is a camera that contributes data.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-table-group-interval.png" alt="" width="563"></div>

**Column** controls what is measured in the table. Three dropdowns set the aggregation (**Total**, **Average**, or **Max**), the metric (**Appearance** or **Dwell Time**), and the object filter (**All objects**, **Group**, or **Individual**). The preview updates as you change these settings. Together they define the column headers and values. Changing any of the three dropdowns updates the preview so you can confirm the table matches what you want before you save.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-table-config.png" alt="" width="563"></div>

<table>
<thead>
<tr>
<th>Locations</th>
<th>Cameras</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><p>Preview lists each location as a row.</p><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-table-group-locations.png" alt="" width="400"></td>
<td align="center"><p>Preview lists each camera as a row.</p><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-table-group-cameras.png" alt="" width="400"></td>
</tr>
</tbody>
</table>

Once you've set Group and Column, continue with step 7 to select cameras.

## Edit or delete the widget

To edit or delete the widget, follow the steps in [Change widget settings](../../create-and-manage-dashboards.md#change-widget-settings) and [Delete a widget](../../create-and-manage-dashboards.md#delete-a-widget) in Create and manage dashboards.
