# Gloves detection

Gloves detection flags people in the camera view who aren't wearing hand protection where it's required. It's designed for environments where gloves are a hygiene or safety requirement that can't be left to self-enforcement.

## How it works

Lumana's AI model scans the camera feed and checks whether detected individuals are wearing gloves. When someone is found without them in the monitored area, Lumana flags the person and records a clip.

## When to use it

This alert is most effective in environments where bare hands pose a hygiene or safety risk.

- Monitoring food preparation or packaging areas where gloves are required for hygiene compliance.
- Enforcing hand protection policies in labs, clean rooms, or medical environments.
- Providing an automated compliance check alongside manual inspections.

In each case, the alert replaces or supplements manual spot-checks with continuous automated monitoring. Gloves detection works entirely from the camera feed, with no external data required. [Event tag](../integrations/event-tag.md) inverts that model, pulling in events from external systems and anchoring them to the corresponding camera moment.
