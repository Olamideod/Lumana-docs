# Event validation

Event validation triggers when camera footage doesn't match the expected conditions of an Event Tag trigger. Use it to catch discrepancies between what an external system recorded and what the camera actually shows.

## How it works

You define an Event Tag and a set of conditions that the camera scene should meet when that event occurs. When Lumana receives the event, it checks the footage against those conditions. If the scene doesn't match, for example no customer was present when a cash register was opened, the alert triggers.

## When to use it

Event validation is most useful in environments where fraud, policy violations, or operational exceptions need to be caught in real time.

* Detecting when an employee opens a cash register without serving a customer, indicating a potential cash handling violation.
* Flagging transactions that occur outside of expected camera conditions, such as no person visible at a POS terminal during a refund.
* Verifying that physical activity at a location matches what an external system logged at that time.

These scenarios all rely on the same logic: if the camera doesn't show what the external system says happened, it's worth investigating.
