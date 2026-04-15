# Heatmap

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Main_entrance_heatmap.png" alt=""><figcaption></figcaption></figure></div>

A heatmap widget shows where activity is concentrated in a camera's field of view. It overlays a color-coded map on the camera feed, with more intense colors indicating higher detection activity.

Use this widget to understand movement patterns: which entrance gets the most traffic, where people tend to congregate, or which areas see the most activity over a given period.

## Prerequisites

A heatmap widget requires that your system contain at least one camera that is configured and online.

## Add a Heatmap widget

Adding a Heatmap widget opens a configuration dialog where you select a camera, set the display mode, and choose a time range.

1. While [creating your dashboard](../create-and-manage-dashboards.md#create-a-dashboard), or while it is in [edit mode](../create-and-manage-dashboards.md#edit-a-dashboard), select **Add widget** in the top right corner. Select **Heatmap** from the list that appears. The configuration dialog opens.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/widget-heatmap-dialog.png" alt="" width="563"></div>

2. Enter a name in the **Title** field.
3. Choose a camera from the **Camera** field.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/widget-camera-field.png" alt="" width="375"></div>

The Heatmap widget displays activity from a single camera at a time. To compare activity across multiple cameras, add a separate Heatmap widget for each one.

4. Select **Select.** The preview panel on the right updates to show the view from the selected camera.
5. Use the **Display** field to select which objects to track in the camera's view.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/widget-heatmap-display-individual.png" alt="" width="563"></div>

Your options are as follows:

* **All objects**: All detectable objects are included.
* **Group**: Only objects in the selected category or categories are included. Some examples of categories: **Person**, **Vehicle**, **Animal**, **Shopping cart**, and **Container**.
* **Individual**: Filter by specific detected subjects. The options available depend on what your cameras have detected.

6. Adjust the **Opacity** slider. This controls how much the heatmap overlay covers the underlying camera image. Drag it left for a more transparent overlay, or right for a more opaque one. The default is 50%.
7. Select a **Visualization** scale. Your options are:

* **Linear**: The color of a pixel reflects the raw number of objects detected in that area, and additional detections change the color value at a constant rate. For example, if it currently takes 5 more detections to change the color of a pixel, the color will change whether the number of detections increases from 0 to 5 or from 1,000 to 1,005.\
  This is useful for quickly identifying high-traffic zones, chokepoints, and entry points, but is less useful for noticing isolated cases of activity in forbidden areas.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/widget-heatmap-viz-linear.png" alt="" width="563"></div>

* **Logarithmic**: The color of a pixel reflects the _relative_ number of objects detected in an area. For example, if it currently takes twice as many detections to change the color of a pixel, the color will change by the same amount whether the number of detections increases from 10 to 20 or from 3,000 to 6,000.\
  This is useful for making sure small changes at the lower end of the scale become highly noticeable. It highlights isolated instances of activity in places where there shouldn't be any, but makes it harder to differentiate between high-traffic and very-high-traffic areas.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/widget-heatmap-viz-logarithmic.png" alt="" width="563"></div>

8. Optionally, set a **Time** range that the heatmap will cover.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

If you set this to `---`, then this widget will use [the time range that is set for the dashboard as a whole](../filter-a-dashboard.md#time-range).

9. Select **Add** in the lower right. The heatmap apperas on the dashboard canvas using the settings you configured.
