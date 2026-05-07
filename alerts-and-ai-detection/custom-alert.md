# Configure a custom alert

A custom alert lets you create an alert using any existing alert type's condition. You select the condition type from a central dropdown, configure the parameters, set a schedule, and define what happens when the alert triggers.

{% hint style="info" %}
Admin access is required to configure alerts.
{% endhint %}

## Create a custom alert

1. In the left navigation, select **Alerts**. The Alerts page opens.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/alerts-monitoring-view1.png" alt="" width="563"></div>

2. Select **Add alert** in the top right corner. The Configure alerts page opens, showing all available alert types grouped by category.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/alerts-configure-page.png" alt="" width="563"></div>

3. From the left sidebar, select **Custom alert**. The Custom alert creation page opens.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-creation-page.png" alt="" width="563"></div>

4. Enter a name for the alert in the **Alert name** field. Use a name that describes the condition and location, for example "Warehouse motion" or "Main entrance trespassing."

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-name-field.png" alt="" width="563"></div>

5. Select **When this happens**. A dropdown opens showing all available alert types grouped by category.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-when-dropdown.png" alt="" width="563"></div>

6. Search for or scroll to the alert type you want to use, then select it. The condition sentence appears with the configurable parameters highlighted.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-condition-sentence1.png" alt="" width="563"></div>

{% hint style="info" %}
Depending on the alert type, the sentence may show one parameter or several. For some alert types, the next parameter appears only after you set the one before it.
{% endhint %}

7. Select each highlighted parameter in the sentence and set its value. The last parameter in every sentence is **camera**. Selecting it completes the condition. After you select a camera, the scheduling, configuration, and action options appear.

The example below shows a completed sentence with all parameters set.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-completed-sentence.png" alt="" width="563"></div>

For the exact parameters your alert type uses, see [Custom alert parameters](custom-alert-parameters.md).

8. The **at all times** field controls when the alert is active. The default keeps the alert active around the clock. To restrict the alert to specific hours or days, select **at all times** to open the scheduling options. For all scheduling options, see [Configure alerts](create-and-manage-alerts.md#schedule).

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-schedule.png" alt="" width="563"></div>

9. Select **default configuration** to open the advanced settings panel. This lets you set confidence level, priority, blocking period, and alert message. Select **Done** to close the panel. The link updates to **custom configuration** to confirm your changes were applied. For details on each setting, see [Configure alerts](create-and-manage-alerts.md#default-configuration).

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/custom-alert-advanced-config.png" alt="" width="563"></div>

10. Select **Then** to choose what Lumana does when the alert triggers. Select an action from the list. For a description of each action and how to configure it, see [Alert actions](alert-actions.md).

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/alert-then.png" alt="" width="563"></div>

11. When all settings are complete, select **Create alert** in the top right. The alert is saved.
