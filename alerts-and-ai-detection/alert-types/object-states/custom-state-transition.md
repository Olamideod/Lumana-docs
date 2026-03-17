# Custom state transition

The custom state transition alert triggers when an object moves from one defined state to another in a specific sequence. Unlike the state change alert, it only triggers when the exact from-state to to-state order is detected.

## How it works

You define two states and the object category to monitor. Lumana watches for the object moving from the first state into the second. When that sequence is detected, the alert triggers and captures a clip of the transition.

## When to use it

This alert is a good fit when direction matters. You need to catch a specific progression, not just any state change.

- Detecting when a vehicle moves from parked to active in a restricted area.
- Monitoring equipment that transitions from idle to in-use during off-hours.
- Tracking objects that move through a defined sequence of positions or zones.

These are the most common starting points, but the alert applies to any transition sequence that has operational meaning in your environment. [Custom state duration](custom-state-duration.md) adds a time element to that picture, triggering when an object remains in a particular state for longer than expected.
