# Disruptive sensors

Connecting a Disruptive sensor to Lumana lets you link sensor events, such as temperature changes, to camera views and automated actions. For example, you can automatically send a snapshot when the temperature crosses a set threshold.

## Connect Disruptive sensors to Lumana

1. Generate a Lumana API key.

   Log in to the Lumana portal, then navigate to **Organization settings** → **API Keys**. Generate a key and save it. You will use it in the next step.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/other-devices/disruptive-sensors/disruptive-create-api-key.png" alt="" width="563"></div>

2. In the Disruptive portal, open **Data Connector**. Create a new connector.

3. Name the connector (for example `Lumana Production`).

4. In **Endpoint URL**, enter `https://access.lumana.ai/v1/sensors/disruptive/heartbeat`.

5. In **Custom HTTP Request Header**, add the Lumana API key from step 1.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/other-devices/disruptive-sensors/disruptive-data-connectors.png" alt="" width="563"></div>

6. Create a Disruptive service account.

   Create a new service account in the Disruptive portal. Generate a key and save the `Key ID` and `Secret`, then go to **Project Settings** and note the `Project ID`.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/other-devices/disruptive-sensors/disruptive-service-accounts.png" alt="" width="563"></div>

7. In Lumana, open **Organization Settings** → **Integration** → **Disruptive**.

8. Enter the `Project ID`, `Key ID`, and `Secret`, then select **Install**.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/other-devices/disruptive-sensors/disruptive-install-integration.png" alt="" width="563"></div>

9. In Lumana, go to **Devices** → **Location** → **Edit Location**.

10. Add sensors from the available list. Assign each sensor to the relevant camera.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/other-devices/disruptive-sensors/disruptive-location-sensors.png" alt="" width="563"></div>

## Next steps

After you connect Disruptive sensors, you can continue with related setup tasks.

- Use [GPIO devices](gpio-devices.md) when you also need wired triggers from the Lumana Core.
- Use [Smart speakers](smart-speakers.md) to add audio responses to Disruptive-driven alerts.
- Read [Camera networking options](../camera-networking-options.md) to plan remote access to camera and sensor admin pages.
