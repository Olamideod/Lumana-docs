# Event tag

Event tag connects Lumana to external systems such as point-of-sale, warehouse management, or access control, and triggers an alert when a defined event is received from that system. Use it when the condition you need to monitor lives in an external platform, not in the camera feed alone.

## How it works

You create an API key in Lumana and configure an event with the fields you want to track (text, integer, decimal, or boolean). Your external system sends a POST request to Lumana when the event occurs. Lumana indexes the event against the camera footage at that timestamp and triggers the alert. The footage tied to the event becomes searchable in Smart Search.

## When to use it

Event tag alerts are useful when you need to correlate video footage with data from another system.

- Alerting security when a high-value refund is processed at a POS terminal, so footage of the transaction can be reviewed immediately.
- Flagging shipment arrivals in a warehouse by pulling pallet IDs from a warehouse management system.
- Triggering an alert when a specific access control event occurs and linking it to the corresponding camera view.

In each case, the value is in connecting an external system event to the moment it happened on camera. [Event validation](event-validation.md) builds on that connection, flagging cases where what the external system logged doesn't match what the camera actually shows.
