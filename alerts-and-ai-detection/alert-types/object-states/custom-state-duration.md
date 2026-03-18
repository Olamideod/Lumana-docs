# Custom state duration

The custom state duration alert triggers when an object stays in a defined state longer than a time threshold you set. It's similar to loitering detection, but applied to a custom state rather than simple presence in a zone.

## How it works

You define a state, an object category, and a minimum duration. Lumana monitors the camera feed and starts a timer when the object enters the defined state. If it remains in that state past the threshold, the alert triggers and a clip is captured.

## When to use it

Use this alert when the length of time in a state matters more than the state itself.

- Alerting when a door stays open beyond an acceptable time window.
- Detecting when a vehicle remains parked in a no-stop zone for too long.
- Monitoring equipment that stays in an idle or fault state longer than expected.

These are the most common starting points, but the alert applies to any state where time in that state is the key risk indicator.
