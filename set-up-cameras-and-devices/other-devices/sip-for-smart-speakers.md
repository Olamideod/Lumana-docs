# Configure SIP for smart speakers

Use _Session Initiation Protocol_ (SIP) to enable communication between Lumana and external audio devices such as network speakers.

You typically need this setup for advanced deployments that use network-managed audio and a firewall such as Check Point.

## Configure SIP on a Check Point router

### Prerequisites

You need:

* Administrative access to the Check Point router
* Access to Check Point SmartConsole
* Network topology details

### Configure the router

Complete the following steps in order on the Check Point router.

1. Open VoIP settings.

   - Log in to Check Point.
   - Go to **Access Policy** > **VoIP**.

2. Enable VoIP. On the **Access Policy** > **VoIP** screen, enable VoIP.

   <div align="center" data-with-frame="true"><img src="../../.gitbook/assets/check-point-voip-toggle-on.png" alt="" width="563"></div>

3. Configure the SIP service provider.

   - Enable **Use SIP Service Provider**.
   - Set **Name** to **SIP-Provider**.
   - Add the networks and domains listed below.

   **Networks**:

   | Name                | Address        | Subnet Mask     |
   | ------------------- | -------------- | --------------- |
   | Oregon\_Gateways    | 54.244.51.0    | 255.255.255.252 |
   | Frankfurt\_Gateways | 35.156.191.128 | 255.255.255.252 |
   | Virginia\_Gateways  | 54.172.60.0    | 255.255.255.252 |
   | Media\_server\_1    | 34.203.254.0   | 255.255.255.0   |
   | Media\_server\_2    | 3.235.11.128   | 255.255.255.128 |

   **Domains**:

   * lumana1.sip.twilio.com
   * lumana1.sip.us1.twilio.com

   <div align="center" data-with-frame="true"><img src="../../.gitbook/assets/off-premise-sip-provider-service-list.png" alt="" width="563"></div>

4. Configure RTP services.

   - Disable SIP traffic inspection.
   - Add the services in the table below.
   - Enable bidirectional traffic.

   | Name           | Protocol | Port |
   | -------------- | -------- | ---- |
   | SIP\_TLS\_AUTH | TCP      | 5061 |
   | SIP\_TCP       | TCP      | 5060 |
   | SIP\_UDP       | UDP      | 5060 |
   | SIP\_UDP       | UDP      | 5061 |

   <div align="center" data-with-frame="true"><img src="../../.gitbook/assets/sip-traffic-inspection-rtp-services.png" alt="" width="563"></div>

5. Configure on-premise devices.

   - Use on-premise phones without a SIP server (PBX).
   - Add all relevant resources, for example:

   | Name             | Type      | Address        |
   | ---------------- | --------- | -------------- |
   | Uniview\_speaker | Single IP | 192.168.100.30 |

   <div align="center" data-with-frame="true"><img src="../../.gitbook/assets/on-premise-devices-ip-phones.png" alt="" width="563"></div>

6. Configure SIP services. Add the following services:

   | Name           | Type           | Protocol | Destination Ports |
   | -------------- | -------------- | -------- | ----------------- |
   | SIP\_TLS\_AUTH | SIP\_TLS\_AUTH | TCP      | 5061              |
   | SIP\_TCP       | SIP\_TCP       | TCP      | 5060              |
   | sip\_any-tcp   | sip\_any-tcp   | TCP      | 5060              |
   | SIP\_UDP       | SIP\_UDP       | UDP      | 5060              |
   | Any\_TCP       | Any\_TCP       | TCP      | 1-65535           |
   | SIP\_UDP       | SIP\_UDP       | UDP      | 5061              |
   | Any\_UDP       | Any\_UDP       | UDP      | 1-65535           |

   <div align="center" data-with-frame="true"><img src="../../.gitbook/assets/sip-service-ports-table.png" alt="" width="563"></div>

## Configure SIP on each speaker

After you finish the Check Point steps above, open each speaker's own admin interface and enter its SIP account so the device can register. The subsections below walk through Uniview and TOA speakers as examples.

{% hint style="info" %}
**Note**: SIP credentials (address, username, password) are supplied by your CSM.
{% endhint %}

### Uniview speaker

1. Log in to the Uniview speaker interface.
2. Go to the **SIP Account** section.
3. Enter the following:
   - Username
   - ID
   - Password
   - **Display Name**: used as the identifier on alerts.
   - Server Host
   - Port
4. Set **Expire Time > 600**.
5. Set **Auto Answer** to **Immediately**.
6. Save.
7. Verify the speaker's status shows **Registered**.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/sip-account-setup-example.png" alt="" width="563"></div>

### TOA speaker

1. Log in to the TOA speaker interface.
2. Go to the **SIP** section.
3. Update the following details:
   - SIP Server Address
   - SIP Server Port
   - Registration Expiry > 3600
   - User ID
   - Display Name
   - Password
4. **Audio codec**: enable all audio codecs.
5. Save.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/toa-speaker-sip-account-registered.png" alt="" width="563"></div>

## Next steps

* To add IP speakers you trigger with patterns over REST or TCP/UDP in VMS+, continue with [Smart speakers](smart-speakers.md).
* For remote access to a camera manufacturer's web UI, see [Camera networking options](../camera-networking-options.md).
