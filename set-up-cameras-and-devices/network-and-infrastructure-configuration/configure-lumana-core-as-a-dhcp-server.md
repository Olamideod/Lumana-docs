# Configure Lumana Core as a DHCP server

Lumana Core can run a DHCP server on **Ethernet 2**. It assigns IP addresses to devices on that interface so you skip manual addressing for each device.

{% hint style="info" %}
Use this feature when you want Lumana Core to assign IP addresses to devices connected on Ethernet 2.
{% endhint %}

## Key DHCP server capabilities

When you enable DHCP on Lumana Core, the server assigns addresses and manages client connectivity basics, including:

- Automatic assignment of IP addresses
- Management of network connectivity for connected devices
- Centralized configuration of network settings such as DNS servers and gateways

## Before you start

- Confirm you can edit the relevant Core in Lumana.
- Connect the devices you want Lumana Core to manage to **Ethernet 2**.
- If another DHCP server is already active on that segment, then review the impact before you enable this feature. Turning on Lumana’s DHCP server can change IP assignments for devices on the network.

## Configure DHCP server on Lumana Core

1. In the left sidebar, select the <img src="../../.gitbook/assets/dhcp-sidebar-cameras-icon.png" alt="Cameras icon in the sidebar." data-size="line"> **Cameras** icon.

2. Select **Devices**. Under **Devices by types**, select **Cores** (for example the **1 core** tile). On the **Devices list**, apply the **Cores** filter if it is not already active. Then select **Edit location** <img src="../../.gitbook/assets/dhcp-edit-pencil-icon.png" alt="Edit pencil icon." data-size="line"> on the row for the location that contains the Core where you want DHCP.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/dhcp-devices-by-types-core-tile.png" alt="Devices overview with Devices by types and Core tile selected." width="563"></div>

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/dhcp-devices-list-edit-location.png" alt="Devices list filtered to Cores with Edit location on the location row." width="563"></div>

3. Select **DHCP Server** in the sidebar, enter the required parameters, then select **Enable**.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/dhcp-server-configuration-form.png" alt="Edit Core with DHCP Server selected: pool fields, DNS, gateway, lease time, and Enable." width="563"></div>

## Configuration parameters

Configure the following parameters when you set up the DHCP server on Lumana Core:

- **Starting IP Address**: The first IP address in the DHCP pool that Lumana Core assigns to devices.
- **Ending IP Address**: The last IP address in the DHCP pool, defining the range of available IPs.
- **DNS Servers**: A list of DNS servers that clients should use for domain name resolution. Separate multiple servers with commas.
- **Gateway**: The default gateway IP address that clients will use to communicate with external networks.
- **Lease Time**: How long, in seconds, a device keeps an IP address before it must renew the lease.

## Example configuration

The example below shows a completed DHCP server configuration.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/dhcp-example-configuration-filled.png" alt="Example DHCP Server configuration with sample values." width="563"></div>

When you enable DHCP, the page shows an option to reserve IP addresses.

## Address reservation

Lumana Core supports DHCP address reservation, allowing specific devices to always receive the same IP address based on their MAC address. This feature is useful for devices that require static IPs but benefit from centralized DHCP management.

### Configure address reservation

1. Identify the MAC address of the device that requires a reserved IP.
2. Assign a specific IP address within the DHCP range to the device.
3. Ensure that the reserved IP does not overlap with dynamically assigned addresses.
4. Save the configuration so that the device always receives the assigned IP when connecting to the network.

### Address reservation use cases

- Ensuring stable IP addresses for critical infrastructure such as servers and other network devices
- Preventing IP conflicts by pre-assigning known addresses

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/dhcp-address-reservation-ui.png" alt="" width="563"></div>

## Next steps

After you configure DHCP on Lumana Core, you can continue with related setup tasks.

- Use [Firewall requirements](firewall-requirements.md) to align outbound rules with the new pool.
- Use [Local time and NTP configuration](local-time-and-ntp-configuration.md) to keep Core timestamps accurate.
- Use [Set up a static IP address](../set-up-a-static-ip-address.md) when you need fixed addresses outside the DHCP pool.
