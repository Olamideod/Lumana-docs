# Gun detection

Gun detection alerts you when a firearm is visible in the camera view, regardless of whether it's being actively held or brandished. It's distinct from the [gun drawn alert](gun-drawn.md), which looks specifically for a weapon raised in a threatening posture.

## How it works

Lumana's AI model scans the video feed for firearms within the frame. When one is identified, the alert triggers and footage of the event is saved for review.

## When to use it

This alert is suited for locations where unauthorized weapons are a defined security risk.

- Monitoring access points, lobbies, or public spaces for unauthorized weapons.
- Providing an early warning layer alongside the gun drawn alert for higher-risk environments.
- Supporting compliance in locations where weapons are prohibited.

What these locations share is a clear policy against unauthorized weapons, and the need for an automated layer of enforcement. [Speed control](speed-control.md) applies the same logic to vehicle behavior, using movement as the indicator rather than what someone is carrying.
