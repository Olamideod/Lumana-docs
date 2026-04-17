# Tracking people

# Introduction 

Lumana is a modern, cloud-based VMS+ platform built around our powerful AI-Engine, enabling users to search 1000’s of hours of video in seconds, get real-time alerts, and trigger automatic responses. By unlocking the power of visual intelligence, Lumana transforms video surveillance into a proactive, action-based video management system that enables safer spaces and smarter operations.

Lumana is easy to install and can achieve novel analytics without human intervention. Our patented video AI algorithms are designed to optimize your cameras and continuously train on the video stream captured by each camera, delivering unprecedented object detection results that get smarter over time.

Powered by our novel AI engine, Lumana people analytics allow you to search, track and analyze occupancy trends based on facial recognition, person attributes and long range detection of persons.

## People analytics features

### Person detection

Lumana's AI engine excels in long-range person detection, capable of tracking individuals and storing their images in high resolution. This functionality allows for comprehensive viewing of all detected persons within your organization. You can select either a single person or groups appearing together, setting alerts based on their specific activities. This powerful tool enhances security, surveillance, and operational efficiency, providing a sophisticated layer of monitoring and response to movements within your premises

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-person-detection-results.png" alt="Person detection results showing tracked people across multiple camera views and time ranges." width="480"></div>

### Person attributes

Leverage the power of person attribute recognition to set proactive alerts and conduct searches across your organization based on specific characteristics such as clothing color, type, accessories, and gender. This advanced feature enhances security measures, streamlines search operations, and personalizes user experiences, allowing for a highly customized approach to monitoring and interaction within any organizational setting.

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-person-attributes-filters.png" alt="Person attributes search showing filters for appearance, clothing, and accessories." width="480"></div>

### Cross camera tracking
Cross camera tracking technology extends beyond facial recognition, utilizing body structure, clothing, and unique physical characteristics to track individuals across an organization. This approach ensures robust monitoring in situations where facial recognition may not be viable, enhancing security and operational efficiency. It serves as a critical tool for managing attendance, preventing unauthorized access, and ensuring safety, all with a keen eye on privacy and ethics.

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-cross-camera-tracking-results.png" alt="Cross-camera tracking results showing the same person matched across multiple camera views." width="480"></div>

### Face recognition

Lumana's face recognition technology enables swift search and alert setting based on facial recognition, enhancing both security and user experience. By using advanced algorithms, it can accurately identify individuals in various conditions, streamlining processes from personalized interactions to security monitoring. Lumana prioritizes user privacy and data protection, ensuring the ethical use of this powerful tool.

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-recognition-database-view.png" alt="Face recognition database view showing saved people profiles and unsaved people seen on cameras." width="480"></div>


<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-recognition-example.png" alt="Face recognition example showing a detected face highlighted within a meeting room camera view." width="480"></div>
 

### Head angle impact
For optimal performance of face recognition cameras should capture faces head–on, facing the camera and within face recognition distance.

The angle of captured faces must be within the following range of values:

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-face-angle-guidelines.png" alt="Face angle guidelines showing acceptable pitch, yaw, and roll ranges for face recognition." width="480"></div>

## Optimizing Your Camera Setup 
Ensure your cameras are positioned according to the [following guidelines](https://support.lumana.ai/knowledge/editor/01HEN6TW1P90ZT21YXAJT7FV3X/en-us?brand_id=10899747518610) to get the
optimized results with People Analytics.

### Determining Optimal Distance for Person analysis
When integrating person detection and facial recognition capabilities into a security system, it's crucial to understand that each camera's effective operational distance is determined by its specific resolution. The concept of pixels per foot (PPF) is central to this understanding, as it directly correlates the camera's resolution to the level of detail required for accurate detection and recognition. High PPF values indicate a higher resolution, which is crucial for identifying specific features or actions of individuals in surveillance footage.

### The Necessity of PPF in People Analytics

In people analytics, clarity is non-negotiable. Whether it's for identifying individuals or analyzing person details. The detail captured can be the difference between useful insight and ambiguity. Calculating the optimal PPF is thus a foundational step in setting up an effective surveillance system.

### Step-by-Step Calculation of PPF

1. **Determine the Horizontal Field of View of the Camera (HFoV)**: Begin by assessing the camera's field of view, which is the observable area the camera can capture. This is often provided in the camera's specifications.

2. **Understand the Camera's Resolution**: Know the resolution of the camera, typically denoted in pixels (e.g., 2560x1440 in 4MP camera).

3. **Identify the Distance**: Identify the distance from the camera to the area of interest where individuals will be monitored.
With these elements, you can calculate the PPF.

First, we would like to find what is the horizontal length the camera covers

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-horizontal-length-formula.png" alt="Formula for calculating the horizontal length covered by the camera using distance and horizontal field of view." width="480"></div>

where:


�W is the horizontal length the camera can see

�D is the distance from the camera to the subject

����HFOV is the horizontal field of view of the camera
Example based on Lumana 8MP camera (HFOV=112.9)

On 20 feet distance the horizontal length of the image plane is approximately 60.3 feet width.

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-horizontal-length-example.png" alt="Worked example of the horizontal length calculation using a Lumana 8MP camera field of view at 20 feet." width="480"></div>

The next step is to calculate the PPF at this distance

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-ppf-formula.png" alt="Formula for calculating pixels per foot using camera resolution and horizontal field of view." width="480"></div>


Using the numbers from above with camera horizontal resolution of 8MP camera

Horizontal Resolution of the Camera = 3840 pixels
Horizontal Field of View (Width) = 60.3 feet

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-ppf-worked-example.png" alt="Worked example of the pixels-per-foot calculation using 3840 pixels over a 60.3 foot horizontal field of view." width="480"></div>

PPF is approximately 63.6 pixels per foot 

 You can also find what is the distance for a required PPF. 

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-distance-formula.png" alt="Formula for calculating camera distance based on resolution, pixels per foot, and horizontal field of view." width="480"></div>

For example if we want to know what is the distance for 128 PPF. The distance for having 128 PPF is approximately 9.95 feets

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-ppf-over-distance-chart.png" alt="Chart comparing pixels per foot over distance for 8MP and 5MP cameras." width="480"></div>

### Practical Considerations

1. **Minimum PPF for Identification**: For effective people analytics, a minimum of 18 PPF is recommended for identifying individuals. Higher values are necessary for more detailed analytics, such as facial recognition.
2. **Environmental Factors**: Lighting, obstructions, and the angle of the camera can all affect the effective PPF. It's crucial to account for these factors in both the calculation and physical setup.
3. **Continuous Assessment**: As conditions and technologies evolve, regularly reassess your PPF calculations to ensure your surveillance system remains effective for people analytics.

To apply this knowledge practically, consider setting up a reference table that lists the PPF values against varying distances for each camera model in your inventory. This table will act as a quick guide to determining the maximum effective distance for person detection and facial recognition for each camera.

<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/tracking-people-distance-to-person-capabilities-diagram.png" alt="Top-down diagram showing how people analytics capabilities change with distance from the camera, from person detection to face recognition." width="480"></div>
 

Requirement table per feature: 

|  | Requirement |
| --- | --- |
| Person detection | 7.5 PPF |
| Person attributes | 15 PPF |
| Person tracking | 18 PPF |
| Face recognition | 137 PPF |
 

People analytic performance over Lumana cameras: 

Assembly with 9 feet height, 25 degree tilt, 5'10" person height

| Camera resolution | Person detection | Person attributes | Person tracking | Face recognition |
| --- | --- | --- | --- | --- |
| 5MP | 120 feets | 63 feet | 53 feet | 7 feet |
| 8MP | 160 feets | 84 feet | 70 feet | 9.3 feet |
 