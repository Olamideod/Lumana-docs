# Set up a static IP address

Assign a static IP address so your camera keeps the **same** IP after reboots or when **DHCP** would otherwise supply a new address.

Lumana and other systems can keep using that one address for the camera.

{% hint style="warning" %}
Do not assign a static IP that falls inside the **Dynamic Host Configuration Protocol (DHCP)** pool unless you use a reservation for that address. Otherwise you can get IP conflicts.
{% endhint %}

**DHCP** expands to **Dynamic Host Configuration Protocol**. That service assigns each device an IP address automatically, usually from a range your router, firewall, or Lumana Core manages. Devices can then communicate without manual IP entry on each device.

### How do I know if I have a DHCP server?

**DHCP** is the service that hands out IP addresses automatically. Most sites have one.

You likely have DHCP if a **router, office firewall, or Lumana Core** on the network assigns addresses and your camera already shows an IP in Lumana without you setting a static address on the device. Check your router or Core admin UI for **DHCP** or **LAN** settings if you are unsure.

You likely **do not** have DHCP if every device uses manually entered IPs and nothing on the subnet offers leases. Use **Scenario 3** in that case.

## Choose your setup scenario

Follow the scenario below that matches your network.

- **Scenario 1: Your network includes a DHCP server and you want to assign a permanent IP address** — You keep the camera on **DHCP** and create a **reservation** on the router or Core so this camera always receives the same address.
- **Scenario 2: Your network includes a DHCP server and you want a permanent static IP on the camera outside the DHCP pool** — You set a fixed **IP address**, **subnet mask**, and **gateway** on the camera, **outside** the DHCP pool.
- **Scenario 3: Your network lacks a DHCP server** — No device hands out **DHCP** leases. You configure the camera’s IP in its local web interface (you may need a temporary static IP on your PC first).

### Scenario 1: Your network includes a DHCP server and you want to assign a permanent IP address

1. Connect the camera to your network.
2. In Lumana, collect the **IP address** and **MAC address** you will map on the DHCP server. If the camera is not listed under **Devices** yet, add it to your organization first.
   - From **Devices**, open the camera and note the **IP address**.

 <div align="center" data-with-frame="true"><img src="../.gitbook/assets/devices-list-ip-address.png" alt="Devices list showing the camera IP address."></div>

   - Open **Edit camera** → **Details** and copy the **MAC address**.

 <div align="center" data-with-frame="true"><img src="../.gitbook/assets/camera-details-mac-address.png" alt="Camera details page showing the MAC address field."></div>

3. Configure DHCP reservation on your router using the MAC address.
The camera keeps the same IP address after reboots or power interruptions when the server always offers that lease to this MAC address.
Refer to your router documentation for instructions.

Here's an example of [static mapping configuration](https://www.cisco.com/c/en/us/td/docs/ios/12_2sb/12_2sba/feature/guide/sbhcpsm.html) for Cisco routers.

### Scenario 2: Your network includes a DHCP server and you want a permanent static IP on the camera outside the DHCP pool

You still have **DHCP** on the network, but you set a fixed address on the camera that sits **outside** the DHCP pool instead of using a reservation.

**Before you begin**

- Identify your network’s DHCP range
- Choose an IP address outside that range

{% hint style="warning" %}
Assigning an IP address inside the DHCP pool without a reservation can cause duplicate IP conflicts.
{% endhint %}

On the camera, use the same workflow as [Scenario 3: Your network lacks a DHCP server](#scenario-3-your-network-lacks-a-dhcp-server):

- If you **can** open the camera’s local web UI, go to **Setup → Network**, switch to **Static IP**, enter **IP address**, **subnet mask**, and **gateway**, then save.
- If you **cannot** reach the camera yet, start at step 1 of that scenario and work through until the static values are saved.

### Scenario 3: Your network lacks a DHCP server

If your network does not have a DHCP server, connect to the camera’s local page and configure the IP address on the camera.

**Default camera settings (example)**

- Default IP address for the camera is: `192.168.1.13`
- Default Subnet Mask: `255.255.255.0`
- Default user: `admin`
- Default password: `123456`

1. If your device is not receiving an IP address automatically, assign a temporary static IP address on the same subnet as the camera (for example, `192.168.1.10` with subnet mask `255.255.255.0`).

{% hint style="info" %}
If needed, refer to your computer or operating system documentation for instructions on setting a temporary static IP address.
{% endhint %}

2. Open a web browser on a device connected to the same network.

3. Enter the camera’s IP address and log in.

    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-camera-web-login-lb800.png" alt="Camera local web interface login page."></div>

4. Change the default password when prompted.

5. Go to **Setup → Network**.
    <div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-dhcp-settings.png" alt="Camera network settings showing IPv4 DHCP mode."></div>

6. Change the network mode from DHCP to Static IP.

7. Enter your **IP address**, **subnet mask**, and **gateway**.

8. Save your changes.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/lumix-network-ipv4-static-settings.png" alt="Camera network settings showing static IP, subnet mask, and gateway."></div>
