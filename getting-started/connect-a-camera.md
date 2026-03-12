# Connect a camera

Lumana works with any IP camera that supports ONVIF or RTSP protocol. This guide walks you through connecting a camera to your Core using four available methods.

## Before you begin

To get the best performance from your system, configure your camera streams before connecting. See Lumana optimal camera configuration for the recommended settings.

If your camera APIs are supported, enabling the Lumana configuration button automatically configures the camera streams for you.

Stream configuration ensures Lumana gets the best input from your camera. Head to your Core device to start the connection.

## Step 1: Select your Core device

Hover over the relevant Core device and click **Add camera**.

Your Core has been selected and is ready to receive a camera. How Lumana finds that camera depends on your network setup.

## Step 2: Choose a connection method

Lumana offers four methods for adding a camera:

- **Camera search** finds cameras on your network without requiring an IP address.
- **IP search** scans a specific IP range you provide.
- **ONVIF search** detects all ONVIF-enabled devices on your network.
- **Add manually** lets you configure the camera connection directly.

Lumana offers four methods for adding a camera. Choose the one that matches your setup.

Each method requires different information, so have your network details ready. Follow the steps for the method that matches your setup.

## Method 1: Camera search

Use this method if you don't know the camera's IP address. Lumana Core scans your network and automatically locates cameras. You'll only need the camera username and password.

1. Select the camera you want to add and click **Activate stream**.
2. Enter the **Camera name**, **Username**, **Password**, **RTSP port**, and **RTSP path**.
3. Click **Activate camera stream**. Once the connection is established, a static image from the camera appears for verification.
4. Click **Next**.
5. Enter the substream RTSP port and RTSP path.

> **Note:** Configuring a substream extends video recording storage, enabling you to keep footage for more days, but at a reduced quality.

6. Click **Activate Substream**, then click **Next**.

> **Note:** You can skip the substream configuration by clicking **Skip**.

7. Configure the following storage settings:
   - Storage stream
   - Local storage retention period
   - Maximum local storage
   - Storage schedule
   - Retention days

8. Click **Add camera**.

Most networks support camera search without any extra configuration. If you need to scan a specific IP range, Method 2 gives you that control.

## Method 2: IP search

Use this method if you know the IP range of the cameras on your network.

You'll need:
- IP range
- Port

Once you have these details, follow the steps below.

1. Enter the IP range and port, then click **Continue**.
2. Select the camera you want to add and click **Activate stream**.
3. Follow steps 2 to 5 from Method 1 to complete the connection.

Scanning by IP range works well when you know your network topology. For ONVIF-enabled cameras, Method 3 handles detection without requiring an IP range.

## Method 3: ONVIF search

Use this method if your cameras are ONVIF-enabled. Lumana automatically scans the network and detects all ONVIF devices.

You'll need:
- Username and password
- URL path

Gather these details before proceeding. Once you're ready, follow the steps below.

1. Select the detected camera you want to add and click **Add**.
2. Enter the camera credentials and URL path to complete the connection.

ONVIF detection covers most modern IP cameras. If your camera didn't appear in the search results, Method 4 lets you enter the connection details directly.

## Method 4: Add a camera manually

Use this method if automatic detection doesn't find your camera or if you prefer to configure the connection directly.

You'll need:
- Camera name
- IP address
- RTSP port, typically 554
- Username and password
- RTSP path, which is model-dependent and can be found in your camera user manual or [LINK: placeholder]

Gather these details before proceeding. Once you're ready, follow the steps below.

1. Enter all required camera details.
2. Click **Activate Camera**. Once the connection is established, a static image from the camera appears for verification.
3. Click **Continue**.

All four methods yield the same result: a verified camera connection. Download the reference files below if you need them during future configuration.

## Downloads

Use the following files for reference during camera configuration.

- Camera Configuration.csv
- cameras.json

## Next steps

Your cameras are now connected to your Core. The following guides cover manufacturer-specific setup steps.

- **Connect an AXIS camera** walks you through connecting an AXIS camera to your Core.
- **Connect a Hikvision camera** walks you through connecting a Hikvision camera to your Core.
