# Firewall requirements

Lumana requires an outbound internet connection to communicate with Lumana Cloud. The system does not require inbound connections. If your firewall monitors outbound traffic, you'll need to allow the endpoints and ports below to ensure the platform and web application function correctly.

This page is organized by function: start with the outbound requirements for Lumana Core and the platform, then review the shared live view and media requirements that also support the web application, and use the final section for web application-specific endpoints.

## Lumana Core and platform requirements

### Infrastructure URLs

Lumana provides two methods to configure your firewall:

- **Lumana URLs**: A list of domains with their corresponding access requirements
- **Lumana IPs**: An API endpoint that returns all Lumana infrastructure IPs

Allow outbound TCP `443` to the following:

- `*.lumix.ai` - 443 TCP outbound
- `*.lumana.ai` - 443 TCP outbound
- `.us-west.compute.amazonaws.com` - 443 TCP outbound
- `eu-central.compute.amazonaws.com` - 443 TCP outbound
- `.us-east.compute.amazonaws.com` - 443 TCP outbound
- `*cloudfront.net` - 443 TCP outbound
- `auth.docker.io` - 443 TCP outbound
- `*.docker.io` - 443 TCP outbound
- `production.cloudflare.docker.com` - 443 TCP outbound
- `storage.googleapis.com` - 443 TCP outbound
- `www.googleapis.com` - 443 TCP outbound
- `*bc.googleusercontent.com` - 443 TCP outbound
- `*nac.nodebalancer.linode.com` - 443 TCP outbound
- `prometheus-prod-56-prod-us-east-2.grafana.net` - 443 TCP outbound
- `prometheus-us-central1.grafana.net` - 443 TCP outbound
- `www.speedtest.net` - 443 TCP outbound
- `api.speedtest.net` - 443 TCP outbound
- `c.speedtest.net` - 443 TCP outbound

### Infrastructure IPs

Instead of managing URL-based firewall rules, you may whitelist IPs directly.

1. Generate an API key.

   Navigate to:

   **Organization settings** -> **API keys** -> **Generate Key**

2. Get the list of IPs.

   Call:

   `https://access.lumana.ai/v1/network/get-ip-addresses`

   API reference:

   `https://apidocs.lumana.ai/reference/networkcontroller_getipaddresses-1`

3. Put the IPs on the firewall allowlist.

   Add the returned IPs to your firewall’s allowlist.

#### Reference IP allowlist (snapshot)

Prefer the [API response](#infrastructure-ips) above when your tools can consume it. The table below is a **static reference** grouped by **category** and **region**, useful for ticketing, change control, or firewalls that need explicit rows. Entries can change; reconcile with the API and review at least annually.

| IP | Protocol | Port | Category | Region |
| --- | --- | --- | --- | --- |
| 34.133.223.153 | tcp | 443 | MQTT | All |
| 34.54.76.179 | tcp | 443 | HTTPS | All |
| 35.231.124.3 | tcp | 443 | Playback | All |
| 34.68.222.66 | tcp | 443 | Remote Camera Management | All |
| 34.36.94.198 | tcp | 443 | API Server | All |
| 34.102.140.197 | tcp | 443 | Grafana | All |
| 34.36.15.174 | tcp | 443 | Grafana | All |
| 34.30.23.184 | tcp | 443 | SW update | All |
| 34.36.94.198 | tcp | 443 | Storage | All |
| 34.165.189.157 | tcp | 443 | Playback | ME-West |
| 34.165.107.42 | tcp | 443 | Playback | ME-West |
| 34.165.113.111 | tcp | 443 | Playback | ME-West |
| 34.165.67.45 | tcp | 443 | Playback | ME-West |
| 34.165.124.67 | tcp | 443 | Playback | ME-West |
| 34.165.184.208 | tcp | 443 | Playback | ME-West |
| 34.165.220.253 | tcp | 443 | Playback | ME-West |
| 34.165.148.21 | tcp | 443 | Playback | ME-West |
| 34.165.11.252 | tcp | 443 | Playback | ME-West |
| 34.105.92.245 | tcp | 443 | Playback | US-West |
| 34.82.111.200 | tcp | 443 | Playback | US-West |
| 34.58.73.221 | tcp | 443 | Playback | US-Center |
| 34.123.183.49 | tcp | 443 | Playback | US-Center |
| 34.59.105.110 | tcp | 443 | Playback | US-Center |
| 34.58.114.37 | tcp | 443 | Playback | US-Center |
| 34.172.162.34 | tcp | 443 | Playback | US-Center |
| 34.31.30.74 | tcp | 443 | Playback | US-Center |
| 34.135.104.177 | tcp | 443 | Playback | US-Center |
| 34.171.227.109 | tcp | 443 | Playback | US-Center |
| 34.31.15.238 | tcp | 443 | Playback | US-Center |
| 35.184.148.35 | tcp | 443 | Playback | US-Center |
| 34.46.140.117 | tcp | 443 | Playback | US-Center |
| 34.173.210.144 | tcp | 443 | Playback | US-Center |
| 34.66.245.180 | tcp | 443 | Playback | US-Center |
| 35.237.79.158 | tcp | 443 | Playback | US-East |
| 104.196.47.65 | tcp | 443 | Playback | US-East |
| 35.231.124.3 | tcp | 443 | Playback | US-East |
| 35.185.42.155 | tcp | 443 | Playback | US-East |
| 34.23.128.144 | tcp | 443 | Playback | US-East |
| 34.165.255.223 | tcp | 443 | Camera API | ME West |
| 34.68.222.66 | tcp | 443 | Camera API | US |
| 34.27.47.112 | tcp | 443 | Camera API | US |

{% hint style="info" %}
Lumana infrastructure IPs may change periodically. Annual review and update is recommended. When in doubt, use the IP list from `get-ip-addresses` rather than this table alone.
{% endhint %}

### NTP (time synchronization)

Allow at least two of the following NTP servers.

- `time.cloudflare.com` - 123 UDP outbound
- `ntp.ubuntu.com` - 123 UDP outbound
- `pool.ntp.org` - 123 UDP outbound
- `time.google.com` - 123 UDP outbound
- `0.pool.ntp.org` - 123 UDP outbound
- `1.pool.ntp.org` - 123 UDP outbound
- `0.fr.pool.ntp.org` - 123 UDP outbound

### OS Updates

- `archive.ubuntu.com` - ports: 80, 443 TCP outbound
- `security.ubuntu.com` - ports: 80, 443 TCP outbound
- `*canonical.com` - ports: 80, 443 TCP outbound
- `ports.ubuntu.com` - 443 TCP outbound
- `repo.download.nvidia.com` - 443 TCP outbound
- `nvidia.github.io` - 443 TCP outbound

## Shared live view and media requirements

These requirements apply to Lumana Live View and the Lumana Web application.

Lumana Live View uses WebRTC and WebSocket.

All traffic is encrypted with TLS and DTLS.

If UDP is blocked, TURN/TLS over TCP 443 is used.

### STUN servers

- `global.stun.twilio.com` - 3478 UDP outbound
- `stun1.l.google.com` - 19302 UDP outbound
- `stun.l.google.com` - 19302 UDP outbound

### Ports

- `TURN` - 3478 UDP outbound
- `WebRTC media` - 50000-60000 UDP outbound
- `ICE` - 7881 TCP/UDP outbound

For best audio/video performance:

- Allow the UDP ports above
- Enable UDP hole-punching or disable symmetric NAT

### Regional media server details

#### US Central

- `stream-us-central1.lumana.ai` - 443 TCP outbound - Signal connection over secure WebSocket
- `turn-us-central1.lumana.ai` - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
- Load balancer: `34.27.216.77` (`livekit-external-lb`)
- Media server hostname: `stream-us-central1-*.lumana.ai`

Media server IPs:

- `34.27.11.6`
- `35.225.131.69`
- `34.57.39.16`
- `35.202.149.180`
- `34.46.106.42`
- `34.41.133.0`
- `34.29.153.34`
- `35.202.93.234`
- `34.45.55.192`
- `34.60.41.218`

#### US East

- `stream-us-east1.lumana.ai` - 443 TCP outbound - Signal connection over secure WebSocket
- `turn-us-east1.lumana.ai` - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
- Load balancer: `35.196.117.219` (`livekit-external-lb`)
- Media server hostname: `stream-us-east1-*.lumana.ai`

Media server IPs:

- `34.75.254.27`
- `104.196.29.253`
- `34.73.113.91`
- `35.243.236.207`
- `34.139.235.43`
- `34.148.161.83`
- `34.75.232.205`
- `35.237.127.235`
- `35.196.67.179`
- `34.23.19.135`

#### US West

- `stream-us-west1.lumana.ai` - 443 TCP outbound - Signal connection over secure WebSocket
- `turn-us-west1.lumana.ai` - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)
- Load balancer: `35.199.186.174` (`livekit-external-lb`)
- Media server hostname: `stream-us-west1-*.lumana.ai`

Media server IPs:

- `35.247.26.49`
- `35.203.141.127`
- `34.19.8.114`
- `34.169.52.181`
- `35.227.169.160`
- `34.168.155.221`
- `34.169.112.111`
- `34.83.57.138`
- `34.19.100.187`
- `34.105.37.179`

#### Israel

- `stream-me-west1.lumana.ai` - 443 TCP outbound - Signal connection over secure WebSocket
- `turn-me-west1.lumana.ai` - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic
- Load balancer: `34.165.216.47` (`livekit-external-lb`)
- Media server hostname: `stream-me-west1-*.lumana.ai`

Media server IPs:

- `34.165.44.152`
- `34.165.88.175`
- `34.165.75.89`
- `34.165.47.176`
- `34.165.22.239`
- `34.165.201.74`
- `34.165.187.232`
- `34.165.25.182`
- `34.165.19.119`
- `34.165.34.86`

## Lumana Web application requirements

The Lumana Web application also requires an outbound internet connection to communicate with Lumana Cloud. If your network firewall monitors outbound traffic, allow the following endpoints for the application itself.

### Web application infrastructure

- `*.lumix.ai` - 443 TCP outbound
- `*.lumana.ai` - 443 TCP outbound

### Shared live view requirements

For corporate firewalls, the web application also uses the shared live view and media requirements above, including:

- WebSocket and WebRTC traffic
- TURN/TLS over TCP 443 when UDP is not viable
- STUN servers
- Regional media server endpoints and IPs
