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

- [Speed control](speed-control.md) — Detect when vehicles or people exceed a speed threshold.
- [Gun drawn](gun-drawn.md) — The companion alert for actively brandished weapons.
- [Configure alerts](../../configure-alerts.md) — Scheduling, notification options, and advanced settings.
