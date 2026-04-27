# Chart or table

The chart or table widget turns camera data into visual reports. Choose a datasource, choose a visualization format, and configure your axes and filters to track the data that matters.

## Add the widget

1. Follow **Add a widget** in [Create and manage dashboards](../../create-and-manage-dashboards.md#add-a-widget) to open the widget list, then select **Chart or table**. The configuration dialog opens.
2. Enter a name in the **Title** field. Use a name that identifies what the widget is tracking, for example "Main entrance detections today" or "Gun detection alerts this week."
3. Under **Datasource**, choose from:

   * **Objects**: Counts camera detections of people, vehicles, and animals. Use this to track physical activity. For example, how many people passed through the main entrance between 6 and 9 AM, or which hour of the day sees the most foot traffic.
   * **Alerts**: Counts alert events triggered by your configured alert rules. Use this to monitor rule-triggered incidents. For example, how many safety helmet alerts occurred this week or which camera triggers the most trespassing alerts.
   * **Event tags**: Counts how often event tags were applied to video clips. Use this when your team tags clips and you want to measure how often. For example, how many clips were flagged for review this month, or whether tagging is consistent across shifts. Before using this datasource, you need at least one event tag configured and one successful POST to the Lumana API. See [Enhance your video data with Lumana Event Tags](../../../databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md).

4. In **Visualization**, select a format from the icon row. The preview panel updates immediately when you switch types. For a description of each format, see [Visualization types](#visualization-types) below.

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-visualization-icons.png" alt="" width="263"></div>

   For all chart types, continue with step 5.

   If you selected **Counter**, then steps 5 and 6 don't apply. Lumana replaces the X-axis and Y-axis with unlabelled dropdowns: aggregation (**Total**, **Average**, or **Max**; only **Total** is available for Alerts), metric (**Appearance** or **Dwell Time**, Objects datasource only), and filter (**All objects / All alerts / All event tags**, **Group**, **Individual**, or **Additional fields**). Set these, then skip to step 7.

   If you selected **Table**, then the X-axis becomes **Group** (how rows are organized: Time, Locations, Cameras, or Alert types) and the Y-axis becomes **Column** (the same aggregation, metric, and filter dropdowns as step 6). Set both, then continue with step 7.

5. Set the **X-axis**. The first dropdown controls how data is grouped.

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-xaxis-dropdown.png" alt="" width="563"></div>

   * **Time**: Groups data by time interval. When you select this, a second dropdown appears where you set the interval.
   * **Locations**: Groups data by location.
   * **Cameras**: Groups data by camera name.
   * **Alert types**: Groups data by alert type. Only available when **Datasource** is set to **Alerts**. When you use this option, set the Y-axis filter to **Group** or **Individual** for reliable results. Setting the filter to **All alerts** may not display correctly.

   If you selected **Time**, use the second dropdown to set the interval.

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-xaxis-interval.png" alt="" width="563"></div>

   * `---`: Lumana sets the interval automatically based on the active time range of the widget, set in step 8.
   * **Hour**: Groups data by hour.
   * **Day**: Groups data by day.
   * **Week**: Groups data by week.
   * **Month**: Groups data by month.

6. Set the **Y-axis**. Aggregation controls how Lumana combines multiple data points into a single value for each group on the chart.

   First dropdown, aggregation:

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-aggregation.png" alt="" width="563"></div>

   * **Total**: The sum of all events across the selected period.
   * **Average**: The average number of events per time unit across your selected range. Use this to compare activity rates rather than totals. Not available when **Datasource** is set to **Alerts**.
   * **Max**: The highest count in any single time unit. Not available when **Datasource** is set to **Alerts**.

   Second dropdown, metric:

   {% hint style="info" %}
   This dropdown only appears when **Datasource** is set to **Objects**.
   {% endhint %}

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-metric.png" alt="" width="563"></div>

   * **Appearance**: Counts how many times the selected objects were detected in the frame.
   * **Dwell Time**: Measures how long the selected objects remained in the camera's view, in seconds.

   Third dropdown, filter:

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/dashboards/widgets/objects/widget-chart-objects-yaxis-group.png" alt="" width="563"></div>

   * **All objects / All alerts / All event tags**: Includes every item in the count.
   * **Group**: Includes every item that fits in one or more categories that you select. For example, if the widget is counting objects, you can choose categories such as Person, Shopping cart, and Container. If the widget is counting alerts, you can choose categories such as Gun brandished, Traffic control, or License plate. Not available when **Datasource** is set to **Event tags**.
   * **Individual**: Includes only a specific item. For Objects: a specific detected subject, such as a specific person or vehicle. For Alerts: a named alert rule. For Event tags: a specific event tag.
   * **Additional fields**: Filters by field-level values from your API POST requests. Only available when **Datasource** is set to **Event tags**.

   {% hint style="info" %}
   When **Datasource** is set to **Event tags**, the Y-axis label in the preview shows the last metric you set for **Objects**. The data is correct, but only the label is affected. To update the label, switch to **Objects**, change the metric, then switch back to **Event tags**.
   {% endhint %}

7. Select the **Cameras** field to choose which cameras contribute data.

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-camera-field.png" alt="" width="375"></div>

   * Search by camera name or location using the search field.
   * Select **All cameras** to include every camera in your account.
   * Select individual cameras to filter to specific ones.
   * Select **Select** to apply. The field shows how many cameras are selected, for example "1 cameras selected."

   {% hint style="info" %}
   If **Datasource** is set to **Event tags**, then select every camera you included as `cameraId` in your API POST requests. The widget only shows events for cameras selected here. If a camera isn't selected, then its events won't appear in the chart.
   {% endhint %}

8. Optionally, set a widget-level **Time** range. If you leave this as `---`, then the widget uses the dashboard's time filter.

   <div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-time-dropdown.png" alt="" width="375"></div>

   {% hint style="info" %}
   Setting a widget-level time disconnects the widget from the dashboard time filter. To reconnect it, clear the **Time** field back to `---`.
   {% endhint %}

9. Select **Add**. The widget appears on the dashboard canvas.

When you select a data point in the chart, Lumana opens the records view for that period. For **Objects**, it shows the camera frames that contributed to the count. For **Alerts**, it shows alert cards with video clips and timestamps. For **Event tags**, it shows clip thumbnails with the field values from your POST request.

{% hint style="warning" %}
If **Datasource** is set to **Event tags** and the chart shows no data, verify the following: your API POST returned a 2xx response, the `cameraId` in your POST matches a selected camera, the `timestamp` falls within the widget's time range, and the tag filter matches the `eventTypeId` in your POST. For further troubleshooting, see [Enhance your video data with Lumana Event Tags](../../../databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md).
{% endhint %}

## Visualization types

The Chart or table widget supports many different visualization formats. When you select a format in step 4, the preview panel updates immediately so you can see what your data looks like before saving.

### Vertical bar chart

Bars grouped by your X-axis selection, vertical layout. Use this to compare counts across time periods, locations, or cameras at a glance. For example, a bar peaking at 6:00 AM with 91 detections tells you that hour had the most activity.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-vertical-bar.png" alt="" width="563"></div>

### Horizontal bar chart

The same as the vertical bar chart, but rotated. Use this when group labels are long or when you are comparing many time periods.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-horizontal.png" alt="" width="563"></div>

### Line chart

A line connecting data points over your selected grouping. Use this to track trends across a longer period and spot patterns, for example whether activity is rising week over week.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-line.png" alt="" width="563"></div>

### Vertical stacked bar chart

Vertical bars split into segments by object type, alert type, or event tag. Use this when composition matters, for example seeing not just how many detections occurred each hour, but how many were people versus vehicles.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-stacked-vertical.png" alt="" width="563"></div>

### Horizontal stacked bar chart

The same as the vertical stacked bar chart, but rotated. Use this when a horizontal layout suits your dashboard better or when labels are long.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-stacked-horizontal.png" alt="" width="563"></div>

### Counter

A single large count displayed on the canvas. Use this when you want one clear number at a glance, for example the total people detected today or the total gun detection alerts triggered this week.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-number.png" alt="" width="563"></div>

### Table

Data in rows and columns. Use this when you need precise values rather than a visual trend, or when you want to export data for a report.

<div align="center" data-with-frame="true"><img src="../../../.gitbook/assets/widget-chart-viz-table.png" alt="" width="563"></div>

## Edit or delete the widget

To edit or delete the widget, follow the steps in [Change widget settings](../../create-and-manage-dashboards.md#change-widget-settings) and [Delete a widget](../../create-and-manage-dashboards.md#delete-a-widget) in Create and manage dashboards.
