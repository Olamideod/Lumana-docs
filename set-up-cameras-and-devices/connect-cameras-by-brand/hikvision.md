# Hikvision

Hikvision cameras are supported in Lumana when you use compatible series and recommended stream settings.

## Supported Hikvision models

Compatible Hikvision networked camera lines include:

* Hikvision Networked camera Value series with AcuSense
* Hikvision Networked camera Value series with ColorVu
* Hikvision Networked camera DeepinView Series
* Hikvision Networked camera Panoramic Series
* Hikvision Networked camera Performance Series
* Hikvision Networked camera Solar-powered Series
* Hikvision Networked camera Value Express Series

## Connect your Hikvision camera to Lumana Core

This guide explains how to connect your Hikvision camera to Lumana Core. If needed, you can connect using the admin credentials, an ONVIF profile, or a new profile.

Choose the connection method that fits your setup:

* **Admin credentials:** Best option when available. Gives Lumana the highest level of access and compatibility.
* **ONVIF:** Useful when you need a standards-based connection, including some PTZ use cases.
* **New profile:** Useful when you do not want to use the admin account directly and want to manage access separately.

> **Note:** Using reduced-permission accounts may limit some functionality in Lumana.

> **Note:** Use the camera's admin username and password when possible. This provides the highest level of compatibility and access.

### Prepare your Hikvision camera

Ensure your Hikvision camera is updated, correctly configured, and ready to connect, whether using admin credentials, an ONVIF profile, or a new profile.

### Activate your camera with the SADP tool

* **Download SADP Tool:** If your camera is new or hasn’t been initialized yet, start by downloading the SADP (Search Active Device Protocol) tool from the [Hikvision official website](https://www.hikvision.com/en/support/tools/hitools/clea8b3e4ea7da90a9/). This software is designed to help find and initialize Hikvision devices on your network. Note: Hikvision's SADP tool requires Windows OS
* **Install and Launch SADP:** After downloading, install and open the SADP tool on a computer connected to the same network as your Hikvision camera.
* **Detect and Initialize the Camera:** The SADP tool will scan your network and list all Hikvision devices that are not initialized. Select your camera from the list and set a password for it, effectively initializing the device. Note down the IP address assigned to your camera; you will need it for later steps.
* **Assign a static IP (Recommended):** To ensure your camera maintains a consistent connection to Lumana Core, assign it a static IP address through its web interface under the network settings.

### Continue after you log in

If you have successfully logged into your Hikvision camera's web interface using the IP address identified via the SADP tool, this indicates that your camera has been initialized properly. At this stage, your device is ready to be connected to Lumana Core using the recommended admin credentials method for optimal compatibility and feature access.

If you are using admin credentials, you can proceed directly to [Connect a camera](../../getting-started/connect-a-camera.md).

### Configure ONVIF on your Hikvision camera

1. Log into the Hikvision Web Portal.

* **Open a web browser:** Enter the IP address of your Hikvision camera into the browser’s address bar.
* **Administrator login:** Use your administrator credentials to log into the Hikvision web portal. These credentials are the admin username and password established during the initial setup of your camera.

2. Open **Configuration** -> **Network** -> **Advanced Settings**.

* Once logged in, locate and click on the **Configuration** tab found in the top menu of the web interface.
* In the **Configuration** menu, select **Network**, then click **Advanced Settings**.

3. Enable **Hikvision-CGI** and set authentication to **Digest**.

* In the **Advanced Settings** menu, look for the option to **Enable Hikvision-CGI**.
* Check this box to enable CGI, which is often required for third-party integrations and advanced functionality.

4. Enable ONVIF.

* Locate the **Enable ONVIF** field within the same section.
* Check this box to activate ONVIF support on your camera.

5. Add an ONVIF user.

* Add a user specifically for ONVIF access.
* Use the same login information as the camera at the admin level. This means creating an ONVIF user with administrative privileges.

6. Save your settings.

* After configuring the ONVIF settings and adding a user, click **Save** to apply and preserve your changes.
* A confirmation message or visual indicator should appear, signifying that the settings have been successfully saved.

After completing ONVIF setup, proceed to [Connect a camera](../../getting-started/connect-a-camera.md).

### Create a new user on your Hikvision camera

1. Access the Hikvision Web Portal.
2. Open **Configuration** -> **System** -> **User Management**.

* Once logged in, look for the **Configuration** tab on the top menu of the web portal's interface. Click on this tab to access the various configuration settings available for your camera.
* Inside the **Configuration** menu, look for the **System** section. Under this section, you will find an option labeled **User Management**. Click on **User Management** to proceed to the next step.

3. Add a new user.

* On the **User Management** page, click the **Add** button to start the process of creating a new profile.
* Fill in the details for the new user. You will need to specify a username and password for the new profile.
* Assign a role: It's recommended to assign the role of **Operator** to the new user.
* Permissions: Ensure you select **All** under permissions to grant the new user profile comprehensive access.

4. Save the new user profile.

* After filling in the details and assigning the appropriate role and permissions, click **Save** to finalize the creation of the new user profile.
* A confirmation message or indicator should appear, confirming that the new user has been added successfully.

Using an **Operator** user with **All** permissions allows Lumana Core to configure camera settings, including stream configurations, automatically.

You can now proceed to [Connect a camera](../../getting-started/connect-a-camera.md), which will guide you through the process of adding your camera to Lumana Core and ensuring everything is functioning as expected.
