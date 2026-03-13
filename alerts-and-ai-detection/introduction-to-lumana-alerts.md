# Introduction to Lumana alerts

Lumana uses AI to detect activity across your cameras and trigger alerts when specific events occur. Alerts help you monitor your sites, review incidents, and respond to security events without manually watching every camera.

## How alerts work

When Lumana detects an event that matches a configured alert, it captures a video clip and notifies the relevant people. Each alert includes the camera that triggered it, the time it occurred, and the detected object or event.

You configure which alerts are active for your organization, which cameras they apply to, and who gets notified. Lumana groups alert types to make it easier to find and set up the right one.

## Alert types

Alert types are grouped by the kind of activity they detect. You'll see these groups when filtering alerts in the monitoring view or when setting up new alerts in configuration.

- **Security**: Detects threats and unauthorized activity, including motion, tampering, proximity, trespassing, trespassing zones, tailgating, zone protection, gun detection, gun brandished, speed control, doors, fire, fall detection, violence, and suspect.
- **Identification**: Detects and identifies specific people, vehicles, or containers, including face recognition, license plate, and container.
- **Tracking**: Monitors object movement and behavior within defined zones, including appearing, disappearing, traffic control, occupancy, loitering, line crossing, missing object, absence, and snapshot.
- **Status**: Monitors the health and connectivity of your devices, including camera status and Core status.
- **Safety & compliance**: Monitors workplace safety conditions, including protective gear, personal safety, free-text periodic, gloves, and hands.
- **Integrations**: Connects alert events to external systems and workflows, including event tag, event validation, door tailgating, event clearance, and developer.
- **Retail**: Tracks product availability and shelf conditions, including shelf occupancy threshold and shelf occupancy change.
- **Object states**: Tracks changes in the state of defined objects, including custom state change, custom state transition, and custom state duration.

Once you've set up your alerts, you can monitor and manage them from a single view.

## What you can do with alerts

Each alert includes a video clip, detected object data, and metadata such as the camera name, timestamp, and location. From the **Alerts** section you can:

- Monitor incoming alerts in real time using the **Monitoring** view.
- Filter alerts by camera, object type (Person, Vehicle, or Gun), alert type, tags, and acknowledgement status.
- Set a time range using relative intervals (minutes, hours, days, or weeks) or a specific calendar date.
- Switch between **Clips** and **Objects** views to see alerts as video clips or detected objects.
- Mute and unmute incoming alert sound notifications.
- Save your current filter and time range settings as a named view for quick access later.
- Review video clips, images, and detected objects for each triggered alert.
- Acknowledge alerts to mark them as reviewed.
- Share alerts with others directly from the alert detail.
- Set up and manage alert rules in **Configuration**.

For organizations that need around-the-clock coverage, Lumana also offers a professional monitoring service.

## Professional monitoring

Lumana offers optional [professional monitoring](../monitoring-services/professional-monitoring-with-lumana.md) for supported alert types. A separate license is required. Trained agents review verified alerts and dispatch first responders when needed.

Your alerts are only as useful as the rules behind them. The next guide walks you through setting up alert rules for your organization.

## Next steps

- [Configure alerts](configure-alerts.md) walks you through setting up alert rules for your cameras.
- [Alert view](alert-view.md) explains how to monitor and review alerts in real time.
