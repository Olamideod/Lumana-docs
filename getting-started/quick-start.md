# Quick start

This page provides the fastest method of connecting your Lumana Core to your network and cameras. 

It assumes the following: 
* Our partners or installers have already created your organization in the Lumana system and defined the location of your first Lumana Core.
* You will not be giving additional users access to the Lumana system at this time.
* Your cameras and your Internet connection are on the same local network.
* That network has a DHCP server.
* Your network firewall has been configured with the [open ports required by Lumana](https://support.lumana.ai/hc/en-us/articles/23402039526034-Lumana-Firewall-Requirements).

If any of these are not true, you should [follow the detailed procedure instead](define-your-organization.md).

## What you'll need

Make sure you have the following before starting:

* A Lumana box, containing:
  * A Lumana Core
  * Power adapter
  * C13 power cord
  * 10-pin terminal block connector (x2) (not needed for this procedure)
* At least one IP camera, connected to your network and powered on
* A computer with a supported web browser
* An active Lumana account

## What to do

1. Plug your Lumana Core into a power outlet using the provided cable and power adapter. Make sure to use the coaxial (circular) DC IN port that is next to the Ethernet ports. 
   
   {% hint style="warning" %}
   Do not use the square, four-pin Molex-style DC IN port.
   {% endhint %}

   The Lumana Core powers on immediately, and a green light appears around the Power button.

2. From the home screen of the Lumana web application, select **Devices** in the upper right.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-core-device-button.png" alt="" width="563"></div>

3. Select the **1 core** tile to view the list of Cores.

4. Hover over the Core to reveal the <img src="../.gitbook/assets/icons/edit icon.png" width="20" height="20" style="vertical-align:middle"> (**Edit**) icon, and select it.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-edit-core-button.png" alt="" width="563"></div>

5. If your Core does not have the most recent software update, an **Update to latest version** button appears. Select it.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-core-needs-updating.png" alt="" width="563"></div>
   
   Wait for the update to complete. It may take a few minutes.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-core-update-in-progress.png" alt="" width="563"></div>

6. In the upper left corner, select **Devices**.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-return-to-devices.png" alt="" width="563"></div>
   
7. Select the <img src="../.gitbook/assets/icons/add-icon.png" width="20" height="20" style="vertical-align:middle"> (**Add device**) icon in the upper right part of the appropriate location tile. (If this is your first Core, you will have only one location tile.)
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-camera-button.png" alt="" width="563"></div>
   
8. Select **Camera**.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-add-camera.png" alt="" width="563"></div>
   
9. From the list, choose which Core will handle the streaming video from the camera(s), then select **Next**.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-choose-core.png" alt="" width="563"></div>
   
10. Select **Express**, then select **Next**.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-choose-method.png" alt="" width="563"></div>

11. The system begins scanning the network for camera feeds based on the method you chose, and lists every camera it finds. Use the checkboxes on the left to select the camera feeds you want to monitor, then select **Next**.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-results.png" alt="" width="563"></div>

12. Enter the camera's username and password, enter a port number, and enter the path to the camera's RTSP video stream. For most cameras, the port number is `554` and the datastreams are located at `/media/video1` (primary stream) and `/media/video2` (substream).
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-authenticate.png" alt="" width="563"></div>
   
   If you have multiple cameras with different settings, select **+ Add Credentials** to add a line to the table. There you can provide different connection settings, including different credentials if necessary.
   
   {% hint style="info" %}
     There is no need to identify which connection settings are used for which camera. Lumana will match them automatically.
   {% endhint %}
   
   Select **Connect**.

13. Your Lumana Core attempts to connect to each camera using your credentials. After it does, select **Next**.

14. Select **Finish setup**.
    
    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-add-cameras-configuration.png" alt="" width="563"></div>