# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A stranded-customer support agent connected to a test flow covering five contact shapes.
Does: Responds to cancellations, delays, missed connections, out-of-scope requests, and abusive messages.
Number: Before: 0 of 5 shapes resolved per test run. After: 5 of 5 shapes resolved per test run.
Guardrail: Out-of-scope handling, proved with an out-of-scope trace that did not invent a resolution.
Next: Add an inbound tone gate and measure token cost and cost per resolved contact against $6.90.
Still broken: There is no tone gate on the way in, so an abusive message still receives a calm, helpful answer.
Lever: cost and speed

## Priya asked

Costs: $0.10–$0.15 range per contact at 8 turns per contact. $6.90 per resolved contact at 46 turns per contact. 8 turns per contact is a reasonable target for a human agent.
Wrong: No tone gate on the way in. An abusive message still gets a calm, helpful answer.
Runs it: Not yet defined. Operational ownership and handoff are still to be agreed before deployment.
Left out: Accuracy measurement, dollars per contact, and production-volume validation. We focused on proving the 5 contact shapes first: cancellation, delay, missed connection, out of scope, and abusive message. The given cost is an estimate based on the number of turns and the cost per turn. We have not yet measured accuracy or validated the system at production volume. 
