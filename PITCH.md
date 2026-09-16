# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A disruption-care chat agent for Larkspur Airlines built on the Claude Messages API with 9 tools.
Does: Handles flight cancellations and delays: looks up bookings, checks policy, searches alternatives, and issues vouchers without human intervention.
Number: $0.047 per resolved contact (5 shapes, ~12,300 tokens in avg), vs $6.90 human contact cost.
Guardrail: Never confirms a rebooking without a customer confirmation token, and never processes refunds — those go to a human.
Next: Add tone detection and escalation for abusive messages.
Still broken: Tone: the agent responds normally to abusive messages instead of escalating.
Lever: <cost | speed | intelligence>

## Priya asked

Costs:
Wrong:
Runs it:
Left out:
