# Custom alert

A custom alert lets you build an alert condition from scratch instead of starting from a predefined template. Use it when none of the standard alert types match what you need to detect, or when you want to combine conditions in a way that a template doesn't support.

## Create a custom alert

1. Select the **bell icon** in the navigation bar. The Alerts monitoring view opens.

2. Select **Add alert** in the top right corner. The Configure alerts page opens.

<!-- IMAGE: alerts/alerts-configure-page.png — Configure alerts page with the left sidebar showing categories including Custom alert at the bottom. -->

3. Select **Custom alert** from the left sidebar, or scroll to the bottom of the alert type list. The Custom alert card appears.

<!-- IMAGE: alerts/alerts-custom-alert-card.png — Custom alert card showing a description and a Use template button. -->

4. Select **Use template**. The alert creation page opens with a blank rule sentence.

5. Enter a name for the alert in the **Alert name** field.

6. Configure the alert rule by selecting the underlined fields in the sentence. Each field opens an input or dropdown. Build the condition that describes what you want to detect, for example a specific object type on a specific camera at a specific time.

7. Optionally, select **default configuration** to open the Advanced configuration panel. This lets you set confidence level, priority, blocking period, alert message, and display options. Select **Done** to close the panel.

8. Select **Then** to choose what Lumana does when the alert fires. Each action and how to configure it is covered in [Alert actions](../alert-actions.md).

9. Select **Create alert**. The alert is saved and appears in the configured alerts list.
