# Verkada

Verkada cameras connect to Lumana Core over RTSP. You first enable RTSP on the camera in Verkada, then map the URL into **Main stream** and **Sub stream** fields in Lumana Core.

## Connect your Verkada camera to Lumana Core

### Enable RTSP on the camera

1. Enable RTSP using Verkada's instructions: [Low latency RTSP streaming](https://help.verkada.com/en/articles/6422089-low-latency-rtsp-streaming).

### Map the RTSP URL into Lumana

After RTSP is enabled, Verkada provides an RTSP URL. Use its host, port, credentials, and path segments in Lumana. A typical URL looks like this:

```
rtsp://username:PASSWORD@0bees456678444559515e35.37.camera.verkada-lan.com:8554/high
```

Replace `username`, `PASSWORD`, and the hostname with the values from your camera. The **Main stream** usually uses the `/high` path; the **Sub stream** uses `/low`.

### Configure the main stream

1. Open **Main stream** in the camera connection form.
2. Enter the following from your RTSP URL:
   * **IP address**: `0bees456678444559515e35.37.camera.verkada-lan.com` (example only; use your camera hostname).
   * **RTSP Port**: `8554`
   * **Username** and **Password**: Same as in the RTSP URL.
   * **Connection string**: `/high`

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/verkada-main-stream-rtsp-settings.png" alt="" width="563"></div>

3. Select **Test**, then wait until the camera preview appears.
4. Select **Save**.

### Configure the sub stream

1. Open **Sub stream** in the same form. If the UI shows a **Sub stream** toggle, turn it on.
2. Enter the same **IP address**, **RTSP Port**, **Username**, and **Password** as for **Main stream**.
3. Set **Connection string** to `/low`.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/verkada-sub-stream-rtsp-settings.png" alt="" width="563"></div>

4. Select **Test**, then wait until the camera preview appears.
5. Select **Save**.

{% hint style="info" %}
Verkada allows only one RTSP client per stream URL. If another system uses the same RTSP URL as Lumana Core, then the stream may conflict. Make sure Lumana Core is the only client on that URL, or use separate stream endpoints if Verkada provides them.
{% endhint %}
