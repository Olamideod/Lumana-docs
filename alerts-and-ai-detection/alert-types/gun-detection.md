# Gun detection

Gun detection alerts you when a firearm is visible in the camera view, regardless of whether it's being actively held or brandished. It's distinct from the [gun drawn alert](gun-drawn.md), which looks specifically for a weapon raised in a threatening posture.

## How it works

Lumana's AI model scans the video feed for firearms within the frame. When one is identified, the alert fires and footage of the event is saved for review.

## When to use it

This alert is suited for locations where unauthorized weapons are a defined security risk.

- Monitoring access points, lobbies, or public spaces for unauthorized weapons
- Providing an early warning layer alongside the gun drawn alert for higher-risk environments
- Supporting compliance in locations where weapons are prohibited

## Next steps

For organizations where weapons are strictly prohibited, pairing this alert with the gun drawn alert gives you layered detection. The configuration guide covers the setup for both.

- [Configure alerts](../configure-alerts.md) covers scheduling, notification options, and advanced configuration settings.
- [Gun drawn](gun-drawn.md) covers the companion alert for actively brandished weapons.
