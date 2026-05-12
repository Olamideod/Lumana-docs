# Enable PTZ control

Use Lumana's Remote PTZ (Pan-Tilt-Zoom) control to adjust camera direction and zoom in real time. You can monitor precisely without physical access to the device. After you save these settings, operators can use PTZ from **Live view** when their role permits.

## Prerequisites

- Confirm your camera supports PTZ functionality.
- Add the camera to your Lumana organization and confirm it is online.
- Verify that PTZ is accessible via `ONVIF` or your camera's supported protocol.

## Configure PTZ on the camera

1. Open the camera from the **Devices** list.
2. Select the **Edit camera** icon <img src="../.gitbook/assets/edit-camera-icon-inline.png" alt="Edit camera pencil icon." data-size="line"> on the camera live view.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/set-up-cameras-and-devices/enable-ptz-control/live-view-edit-camera-button.png" alt="" width="563"></div>

3. Navigate to the **PTZ** section.
4. Enable **PTZ support**.
5. Select the **Driver**. Most cameras use **ONVIF** by default.
6. Enter the **PTZ control path**. A common format is `{camera_IP}:80/onvif/device_service`.
7. Specify the **port** when it differs from the default `80`.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/set-up-cameras-and-devices/enable-ptz-control/ptz-settings-onvif-address-port.png" alt="" width="563"></div>

8. Select **Save** to apply changes.

   Lumana stores the PTZ profile on the camera record and shows PTZ controls where your role allows them.

## Next steps

To try PTZ in the web player after you save (pan, tilt, zoom), see [PTZ control](../live-video-monitoring-and-operations/ptz-control.md).
