# Tracking people

Lumana combines video management with an AI engine so you can search large archives of footage quickly, receive real-time alerts, and automate responses. People analytics builds on that stack: you can search, track, and review occupancy-related activity using person detection, attributes, cross-camera association, and—where enabled—face recognition.

The platform is designed to install with standard cameras. Detection and analytics improve as the system processes each stream; positioning and resolution still matter, especially for face recognition and attribute detail at distance.

## Before you begin

- Cameras are added in Lumana and streaming reliably.
- You know which sites or cameras should run people-related analytics (and any org policies that apply to face recognition or cross-camera identity).
- For mounting and aiming, see [camera guidelines for people analytics](https://support.lumana.ai/knowledge/editor/01HEN6TW1P90ZT21YXAJT7FV3X/en-us?brand_id=10899747518610) on the support site.

## People analytics features

These capabilities apply when people analytics is enabled on your cameras.

### Person detection

The engine supports long-range person detection: individuals can be tracked and their crops stored at useful resolution. You can review everyone detected across your organization, select one person or groups that appear together, and base alerts on their activity. This supports security, investigations, and operations that depend on knowing who moved where and when.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-person-detection-results.png" alt="Person detection results showing tracked people across multiple camera views and time ranges." width="480"></div>

### Person attributes

You can filter and alert on person attributes such as clothing color and type, accessories, and gender (where the model provides them). That narrows search and review without manually scanning every clip.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-person-attributes-filters.png" alt="Person attributes search showing filters for appearance, clothing, and accessories." width="480"></div>

### Cross camera tracking

Cross-camera tracking uses body shape, clothing, and other visible cues—not only the face—to associate the same person across cameras. That helps when the face is not visible or not suitable for recognition. Typical uses include attendance, access and investigations across large sites, and safety monitoring where you need continuity beyond a single camera view. Configure and use this capability according to your organization’s policies and applicable privacy requirements.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-cross-camera-tracking-results.png" alt="Cross-camera tracking results showing the same person matched across multiple camera views." width="480"></div>

### Face recognition

Face recognition supports search and alerts based on enrolled or observed faces. Performance depends on lighting, angle, and resolution (see [Head angle impact](#head-angle-impact) and [Pixels per foot (PPF) for camera placement](pixels-per-foot-for-camera-placement.md)). Use face data in line with your policies and regulatory obligations.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-recognition-database-view.png" alt="Face recognition database view showing saved people profiles and unsaved people seen on cameras." width="480"></div>

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-recognition-example.png" alt="Face recognition example showing a detected face highlighted within a meeting room camera view." width="480"></div>

### Head angle impact

For best face recognition results, faces should be roughly head-on—looking toward the camera—and within the distance your setup can support for the required pixels per foot (PPF).

Acceptable head orientation falls in the ranges illustrated below (pitch, yaw, roll).

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-angle-guidelines.png" alt="Face angle guidelines showing acceptable pitch, yaw, and roll ranges for face recognition." width="480"></div>

## Optimize your camera setup

Position and aim cameras using the [camera guidelines for people analytics](https://support.lumana.ai/knowledge/editor/01HEN6TW1P90ZT21YXAJT7FV3X/en-us?brand_id=10899747518610) so people analytics gets consistent coverage.

To derive PPF from resolution, HFOV, and distance, use [Pixels per foot (PPF) for camera placement](pixels-per-foot-for-camera-placement.md). That reference includes worked examples and a **5MP** and **8MP** PPF-over-distance chart.

## People analytics PPF targets

Use the **minimum PPF** values below when you plan each camera or zone. **Person tracking** needs **18 PPF** in this table; **face recognition** needs the highest value. Add margin when lighting is poor, the angle is steep, or the scene is crowded.

Keep a small PPF-versus-distance sheet per camera model so installers can check range quickly.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-distance-to-person-capabilities-diagram.png" alt="" width="563"></div>

Use the following **PPF targets** when planning which capability you need at a given distance:

| Capability | Requirement (PPF) |
| --- | --- |
| Person detection | 7.5 PPF |
| Person attributes | 15 PPF |
| Person tracking | 18 PPF |
| Face recognition | 137 PPF |

**Approximate maximum distances** on Lumana cameras (assembly height **9 feet**, tilt **25°**, reference person height **5′10″**). Treat these as **typical** planning values; your mounting, scene, and lighting will change results.

| Camera resolution | Person detection | Person attributes | Person tracking | Face recognition |
| --- | --- | --- | --- | --- |
| 5MP | 120 feet | 63 feet | 53 feet | 7 feet |
| 8MP | 160 feet | 84 feet | 70 feet | 9.3 feet |

## Next steps

- [Pixels per foot (PPF) for camera placement](pixels-per-foot-for-camera-placement.md) — shared formulas and charts for PPF planning.
- [Build a database of people and vehicles](build-a-database-of-people-and-vehicles.md) — enroll faces and organize profiles for search and alerts.
- [Search video footage for people or vehicles](search-video-footage-for-people-or-vehicles.md) — query by person, attributes, and time.
- [Tracking vehicles](tracking-vehicles.md) — parallel guidance for vehicle analytics and placement.
