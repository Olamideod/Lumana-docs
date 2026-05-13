# Part 2: Set up your Lumana Core

On this page you will connect your Lumana Core to the network that you use for Internet access and make sure it is using the latest software.

1. If your network has a firewall, open the ports that are listed at https://support.lumana.ai/hc/en-us/articles/23402039526034-Lumana-Firewall-Requirements.

2. Plug your Lumana Core into a power outlet using the provided cable and power adapter. Make sure to use the coaxial (circular) DC IN port that is next to the Ethernet ports. 
   
   {% hint style="warning" %}
   Do not use the square, four-pin Molex-style DC IN port.
   {% endhint %}

   The Lumana Core powers on immediately, and a green light appears around the Power button.

3. If your network has a DHCP server, skip to step 4.
   
   <details>
   <summary> Advanced: If your network does not have a DHCP server, expand this section and follow the instructions.</summary> 

   a. Plug one end of an Ethernet cable into port 2 on the Core, and the other end into a laptop or desktop computer.
   
   b. On that computer, configure a temporary static IP address:
       
      * **IP address**: `192.168.1.235`
      * **Subnet mask**: `255.255.255.0`
      * **Gateway**: `192.168.1.1`
      
      <details>
      <summary>Expand for detailed Windows instructions with screenshots</summary> 

      * Open **Network & Internet** settings.
      * Select **Ethernet**.
        
        <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/windows-network-settings.png" alt="" width="563"></div>
      * Under **IP assignment**, select **Edit**.
        
        <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/windows-ethernet-settings.png" alt="" width="563"></div>
      * Change the IP assignment from **Automatic (DHCP)** to **Manual**.
        
        <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/windows-IP-settings.png" alt="An 'Edit IP settings' window with the first dropdown open, showing the options 'Automatic (DHCP)' and 'Manual'." width="563"></div>
      * Enable **IPv4** and fill in the following
        * **IP address**: `192.168.1.235`
        * **Subnet mask**: `255.255.255.0`
        * **Gateway**: `192.168.1.1`
        * **Preferred DNS**: `8.8.8.8`
        
        <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/windows-IPv4-settings.png" alt="An 'Edit IP settings' window with the first dropdown set to 'Manual'. IPv4 is set to On. The 'IP address' field reads 192.168.1.235. The 'Subnet mask' field reads 255.255.255.0. The 'Gateway' field reads 192.168.1.1. The 'Preferred DNS' field reads 8.8.8.8." width="563"></div>
      </details>
   c. Open a web browser and go to `192.168.1.158`. A login page opens.

   d. Enter `admin` for both username and password and select **Login**.
      <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/core-login.png" alt="A 'Welcome to Lumana' screen with a Username and Password field and a Login button." width="563"></div>
    
   e. You are prompted to select a new password. Choose one that is lengthy, memorable, and unique, then select **Save new password**.

   f. Deselect **DHCP**, then change the IPv4 settings to match the settings that the Core should expect to be assigned by your router. Ensure that these settings are reserved or valid within your network's IP plan.
      <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/core-network-config.png" alt="" width="563"></div>
   g. Select **Save changes**.
   </details>

4. Plug one end of an Ethernet cable into port 1 on the Core, and the other end into your router. Green and yellow LEDs on the Ethernet port turn on and begin to blink.

5. Log in to https://app.lumana.ai

6. From the home screen, select **Devices** in the upper right.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-core-device-button.png" alt="" width="563"></div>

{% hint style="info" %}
The next few steps involve defining a location and assigning your Core to that location. Our partners or installers may have already done this for you. If the **Devices** screen lists "1 Core", that means your Core has already been provisioned. Skip to step 13. Otherwise, continue with step 7.
{% endhint %}

7. Select the **0 locations** tile to create a new location.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-core-devices-screen.png" alt="" width="563"></div>

8. Give the location a name, then provide its address, time zone, and other identifying information. When you are done, select **Next** in the bottom right.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-location-screen-1.png" alt="" width="563"></div>

9. To ensure compliance with local law, some features may be unavailable in your area. Choose your jurisdiction from the dropdown; if it is not listed, select **Independent**. Enable or disable the features that you want, then select **Next** in the bottom right.
   
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-location-screen-2.png" alt="" width="563"></div>

10. Enter a name for the core in the **Name** field, and enter its unique ID in the **Core ID** field. This ID is a 24-character hexadecimal that has been printed on a sticker and attached to the side of the Core.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-location-screen-3.png" alt="" width="563"></div>
   
   {% hint style="info" %}
   You can also find the ID in the Core's **About** screen. Open the "advanced" instructions above and follow steps a-e to connect to the core, then go to **About**->**Edge ID**. This is the same as the Core ID.
   {% endhint %}

11. Select **Add Core**. The system thinks for a moment and then brings up a success message:
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/add-core-success.png" alt="" width="563"></div>

12. Select **Done** in the lower right. You are returned to the **Devices** screen, where you can see that you now have "1 device" and "1 core" listed.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-devices-screen-1-core.png" alt="" width="563"></div>

13. Select the **1 core** tile to view the list of Cores.

14. Hover over the Core to reveal the <img src="../.gitbook/assets/icons/edit icon.png" width="20" height="20" style="vertical-align:middle"> (**Edit**) icon, and select it.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-edit-core-button.png" alt="" width="563"></div>

15. If your Core does not have the most recent software update, an **Update to latest version** button appears. Select it.
   <div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-core-needs-updating.png" alt="" width="563"></div>
   
   {% hint style="info" %}
   Do not close this window just yet; you will need to continue to use it in part 3.
   {% endhint %}

The update may take a few minutes. 

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/getting-started/setup-core-update-in-progress.png" alt="" width="563"></div>

In the meantime, if you connected a computer to port 2 on the Core, disconnect it now.

When the update is complete, proceed to [part 3, where you will connect your cameras to the Core](connect-a-camera.md).