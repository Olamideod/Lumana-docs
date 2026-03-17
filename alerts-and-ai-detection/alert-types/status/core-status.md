# Core status

Core status alerts fire when a Lumana Core device loses its connection or comes back online. Because a single Core manages multiple cameras, a Core going offline can affect coverage across an entire site.

## How it works

Lumana monitors the connection status of all registered Core devices. When a Core loses connectivity or reconnects, the alert triggers and sends a notification with the device name, location, and timestamp.

## When to use it

Core status alerting is especially important in deployments where each Core serves a large number of cameras or where sites are remote and unmanned.

- Detecting when a Core device goes offline, which may indicate a network outage, power failure, or hardware issue.
- Catching infrastructure problems before they are reported by end users.
- Monitoring Core connectivity across multiple locations from a single dashboard.

Because a single Core manages multiple cameras, catching a Core going offline quickly is critical to maintaining full-site coverage. That coverage is what makes AI-based alerts reliable. [Protective gear detection](../safety-and-compliance/protective-gear.md) is one of those alerts, using it to enforce PPE compliance across your facility.
