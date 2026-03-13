# Fall detection

The fall detection alert triggers when a person falls in the camera view. It's used in healthcare facilities, care homes, workplaces, and any environment where a fall is a safety event that needs an immediate response.

## How it works

Lumana uses AI to analyze body posture and movement in the video feed. The model is trained to distinguish between normal movements, such as walking, sitting, or bending, and an actual fall. When a fall is detected, the alert captures a clip and notifies the designated contacts.

## Camera placement

Camera placement directly affects detection accuracy. For reliable fall detection:

- Position cameras at a corner or overhead angle that captures the person's full body.
- Ensure there are no obstructions between the person and the camera. Furniture, walls, or other people blocking the view can trigger false alerts.
- Maintain adequate lighting to ensure clear visibility.
- Keep individuals within a reasonable distance from the camera. Subjects too far from the lens may not be detected reliably.

Not every environment is suitable for this alert type. Review the limitations below before deploying.

## Limitations

Fall detection works best in controlled, low-traffic environments. It may not perform reliably in the following conditions:

- **Object size**: The detected person must cover at least 5% of the camera frame and be positioned within the central 80% of the frame.
- **Analysis limit**: Only three individuals are analyzed per frame. If more than three people are present, the three largest are prioritized.
- **Crowded areas**: High-traffic locations such as malls or busy streets can produce false detections.
- **Dynamic environments**: Gyms, sports facilities, or workplaces with frequent rapid movement can confuse the AI model.
- **Distance**: Subjects far from the camera significantly reduce detection accuracy.

If your environment meets the requirements, here's how to set up the alert.

## Configure the alert

1. Select **Alerts** in the left navigation bar, then select **Configurations**.
2. Select **Add alert**.
3. Under the **Security** category, select **Fall detection**.
4. Give the alert a name.
5. Select the camera or cameras positioned to monitor the relevant area.
6. Set the time frame for when the alert should be active, or leave it set to all day.
7. Select **Then do this** to configure notifications. You can notify emergency services, medical personnel, or security staff by SMS, email, or the Lumana app.
8. Select **Create alert**.

## Next steps

Fall detection is also a supported alert type for professional monitoring. Trained agents can verify the alert and dispatch first responders when needed.

- [Configure alerts](../configure-alerts.md) covers scheduling, notification options, and advanced configuration settings.
- [Professional monitoring with Lumana](../../monitoring-services/professional-monitoring-with-lumana.md) explains how professional monitoring works for supported alert types.
