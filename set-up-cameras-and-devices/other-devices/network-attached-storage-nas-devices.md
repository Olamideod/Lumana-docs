# Network attached storage (NAS) devices

Connect a network attached storage (NAS) device to Lumana to expand recording storage and keep a backup of recorded video.

Adding a NAS does not replace Lumana Core. The NAS works alongside the Core as both an additional storage location for longer retention and a backup target for recorded data. Lumana's standard capabilities remain available.

{% hint style="info" %}
If you record to NAS for more than 30 days and want to keep **Smart Search** functionality, then you need an additional NAS license. You do not need a license for the first 30 days.
{% endhint %}

## Prerequisites

* The storage device must support NFS or S3-compatible object storage.
* Your Lumana Core unit must reach the storage device on the network.

## Add an external storage server

1. Save the IP of your network storage server and the path where Lumana should save videos.

   For example:

   * **NAS IP**: `192.168.100.200`
   * **NAS Path**: `/share/LumanaVideos`

2. In the Lumana console, open the **Devices** page. Find the location that holds the NAS, then select **Edit location** (pencil icon) for that site.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/nas-home-devices-edit-location.png" alt="" width="563"></div>

3. In the left menu, select **External Storage**, then select **Add external storage**.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/nas-edit-location-add-external-storage.png" alt="" width="563"></div>

4. Choose **NFS** or **Object Storage** as the storage type. See the NFS example below.

   * **Storage type**: `NFS`
   * **Name**: a label you will recognize when assigning cameras (for example `NFS-Server-1`)
   * **Path**: combine the NAS IP and export path, for example `192.168.100.200/share/LumanaVideos/` (format can vary; match what your NAS expects)

5. Select **Test** to verify connectivity to the server, then select **Save external storage**.

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/nas-edit-location-external-storage-form.png" alt="" width="563"></div>

## Configure cameras to use the external storage server

1. Open the camera’s live view (or the camera page). In the top bar, select **Edit camera** (pencil icon).

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/nas-live-view-edit-camera.png" alt="" width="563"></div>

2. In the edit camera menu, select **Storage**, then scroll to **Additional storage**.

3. Set **Additional storage** to **On**, then set the target type to **External**. Choose the NFS or object storage entry you created for this location, for example `NFS-Server-1`.

4. Set **External retention period** and what to copy to the NAS:

   * Choose the retention period for videos on external storage: 30 / 60 / 90 / 180 / 365 days (or the options your UI shows).
   * Turn on **Storage (SQ)** for standard-quality continuous footage backups.
   * Turn on **Alerts (HQ)** for high-quality clips tied to alerts.
   * Use **Event types** only if you want that subset of footage uploaded.

5. Optional: under **When the upload should occur**, leave **All time** for continuous backup or limit uploads to specific schedules.

6. Select **Save** on the edit camera page to apply your storage settings.

Example: **Storage** with **Additional storage** on **External**, a named NAS target, retention, **Storage (SQ)** / **Alerts (HQ)**, and upload timing:

<div align="center" data-with-frame="true"><img src="../../.gitbook/assets/set-up-cameras-and-devices/nas-edit-camera-storage-additional.png" alt="" width="563"></div>

## Storage capacity calculation

* `RAID 5` - minimum 3 disks
* `RAID 6` - minimum 4 disks
* For `5MP` camera SQ (`700Kbps`), plan `0.3TB` for 30 days of storage
* For `8MP` camera SQ (`1000Kbps`), plan `0.45TB` for 30 days of storage

## Examples of NAS servers

* QNAP TS-1673AU-RP-16G,16 Bay NAS
* QNAP TS-464U-RP-8G 4Bay NAS 2.5Gbe

## Examples of HDDs

* MG09ACA18 Toshiba Enterprise 3.5HDD 512E 18TB
* MG09ACA16 Toshiba Enterprise 3.5HDD 512E 16TB
* MG09ACA14 Toshiba Enterprise 3.5HDD 512E 14TB

## Next steps

After you connect a NAS, you can continue with related setup and storage tasks.

- Use [Configure Lumana Core as a DHCP server](../network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md) when the NAS sits on a network managed by the Core.
- Read [Firewall requirements](../network-and-infrastructure-configuration/firewall-requirements.md) to confirm outbound rules for backups and cloud sync.
- Use [Camera networking options](../camera-networking-options.md) to plan how cameras reach Lumana Core and the NAS.
