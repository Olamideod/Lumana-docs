# Traffic control

Traffic control detection monitors whether objects move through a sequence of checkpoints in the expected order and within an expected time window. It triggers when movement deviates from the configured path.

## How it works

Configure a path by setting up a sequence of zones or checkpoints across one or more cameras. Lumana tracks objects as they move through the path and fires the alert when one completes it outside the expected time window, or when it skips or reverses the expected sequence.

## When to use it

Traffic control detection is suited for environments where the order and timing of movement through defined checkpoints matters.

- Monitoring controlled entry or exit flows in secure facilities where the order of checkpoints is required
- Detecting vehicles completing a circuit too quickly, which may indicate unsafe driving on a premises
- Ensuring people follow a required screening or check-in path before reaching a restricted area

## Next steps

- [Occupancy](occupancy.md) — Monitor how many people or vehicles are in a zone.
- [Configure alerts](../../configure-alerts.md) — Scheduling, notification options, and advanced settings.
