# Loitering

Loitering detection fires when something stays in a monitored zone past a time limit you set. Brief visits don't trigger it, and the alert only fires once the dwell threshold is crossed.

## How it works

Set up a detection zone in the camera frame and configure a minimum dwell time in seconds. Lumana tracks objects inside the zone and flags the event once one has stayed past the threshold. A clip is saved when the alert fires.

Compare this with the [appearing alert](appearing.md), which triggers the moment an object enters with no time requirement.

## When to use it

Loitering detection is a good fit when you need to separate incidental contact with an area from deliberate, extended presence.

- Detecting someone lingering near a cash register, ATM, or point of sale terminal
- Monitoring parking areas for vehicles that stay far beyond normal visit durations
- Identifying unauthorized extended presence in restricted or sensitive spaces

## Next steps

- [Line crossing](line-crossing.md) — Detect when objects cross a directional line.
- [Configure alerts](../../configure-alerts.md) — Scheduling, notification options, and advanced settings.
