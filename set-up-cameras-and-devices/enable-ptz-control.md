# Enable PTZ control

Use Lumana's Remote PTZ (Pan-Tilt-Zoom) control to adjust camera direction and zoom in real time. You can monitor precisely without physical access to the device.

## Prerequisites

* Ensure your camera supports PTZ functionality.
* Confirm the camera is added to your Lumana organization and is online.
* Verify that PTZ is accessible via `ONVIF` or your camera’s supported protocol.

## Key capabilities

- **Full coverage control**: Pan, tilt, and zoom to monitor every area.
- **Remote operations**: Control cameras from anywhere via Lumana.
- **Preset positions**: Configure and return to predefined camera angles.

## Enable PTZ control

1. Select the camera
   * Open the camera from the **Devices** list.
2. Open camera settings

    * Select the <img src="../.gitbook/assets/dhcp-edit-pencil-icon.png" alt="Edit camera pencil icon." data-size="line"> **Edit camera** control.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/live-view-edit-camera-button.png" alt="Camera live view with Settings wrench control highlighted in the top toolbar." width="563"></div>
3. Configure PTZ settings

    * Navigate to the **PTZ** section.
    * Enable **PTZ support**.
    * Select the **driver**
      * Most cameras use **ONVIF** by default.
    * Enter the **PTZ control path**
      * Common format:\
        `{camera_IP}:80/onvif/device_service`
    * Specify the **port** (if different from default `80`).

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/ptz-settings-onvif-address-port.png" alt="Edit camera PTZ tab: PTZ support on, Onvif driver, X address, and port number." width="563"></div>
4. Save configuration
   * Select **Save** to apply changes.

## Next steps

To try PTZ in the web player after you save (pan, tilt, zoom), see [PTZ control](../live-video-monitoring-and-operations/ptz-control.md).
