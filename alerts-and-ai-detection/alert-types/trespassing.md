# Trespassing detection

Trespassing detection flags any object that enters a defined area, with no minimum time requirement. Unlike zone protection, which waits for a dwell threshold before triggering, this alert fires the moment an object appears.

## How it works

Lumana detects when a person, vehicle, or other object enters the configured camera view or zone. The alert fires immediately and records a clip for review.

**Trespassing zones** work the same way but apply to a specific drawn zone within the camera frame rather than the full view.

## When to use it

This alert works best in spaces that should remain completely off-limits, with no exceptions for brief or incidental entry.

- Monitoring restricted areas such as server rooms, storage facilities, or private property
- Detecting after-hours access to spaces that are only authorized during specific times
- Flagging any entry into a defined perimeter, regardless of how briefly an object appears

## Next steps

The configuration guide below has the full setup steps for trespassing and trespassing zone alerts.

- [Configure alerts](../configure-alerts.md) covers scheduling, zone setup, and notification options for this alert.
