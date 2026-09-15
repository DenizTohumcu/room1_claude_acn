# Overnight review: Larkspur disruption-care agent

**To:** DenizTohumcu__room1_claude_acn  
**From:** Larkspur client review agent, on behalf of Priya Raghavan  
**Re:** the disruption-care agent you walked us through in our last session  
**Generated:** 2026-09-15 12:55

## Priya's note

> Our vendor says we should just be using your best model.
>
> Why aren't we?
>
> Priya Raghavan, Larkspur Airlines

She sent that before this session opened. She means it. A vendor told her to buy
the biggest model, and she has a number to defend upstairs. Her four questions from
day one are still open. Naming a model answers none of them.

## Still open from day one

| Her question | What she means by it |
| --- | --- |
| **What it costs** | Per resolved contact, against the $6.90 a human contact costs us. |
| **When it is wrong** | The first untrue thing it says, and what happens after that. |
| **Who runs it** | In June, after you have left. |
| **What you left out** | The scope you cut, and why. |

## What the review agent found

Overnight, Larkspur pointed a review agent at your repository. It read the
code. It did not run your agent, and the only file it changed is this one. Each
item below names the file and the line it is about.

**1. agent.py in this repo is byte-identical to the workshop template, so no build work has landed in version control yet.**

The static scan confirms EXTRA_TOOLS at 0 entries, no LOCAL_TOOLS executors, and TONE_ADDENDUM at 0 characters, all still at their shipped defaults. There is no diff against the template to point to for this pod.

Run git diff against the template commit and paste the output, or confirm the next commit is where the six pencil marks get filled in.

**2. search_alternatives carries a 6 character description, just the word "search", in build_tools() in agent.py.**

Every other tool schema in the same function runs 71 to 445 characters and spells out required fields, side effects and reversibility, for example hold_seat at 73 characters says the hold is "Reversible. It simply expires." search_alternatives gives Claude nothing about what inputs matter, what an alternative looks like, or when to call it versus check_policy. A bigger model reading the same 6 characters has no more to work with than a smaller one.

Run python3 run.py --show-tools and confirm search_alternatives still prints a 6 character description.

**3. No readout-trace.json exists, so no run of this agent has survived to this repository.**

The material states plainly there is no committed wire run. That means nobody can currently point to a transcript showing MAX_TOOL_CALLS of 8 being hit, tool_results() routing correctly across the three branches, or confirm_rebooking's confirmation_token requirement actually holding up against a live conversation.

Run python3 run.py K7PQ2M --trace and commit the resulting readout-trace.json.

**4. There are no eval cases in evals/cases.json, so no measurement exists to compare any model choice against.**

Priya's question about the vendor's suggested model cannot be answered from this repository because nothing here measures an outcome. MAX_TOOL_CALLS is fixed at 8 in agent.py, and without eval cases nobody knows whether any run today or with any model needs 2 turns or 8.

Run python3 eval_harness.py once cases exist and paste the totals.

**5. PITCH.md is unchanged from the template, with nothing filled in about cost, failure mode, or ownership.**

The file remains at its shipped state. This is expected at this stage of the day, but it means none of the four questions Priya raised have any answer sitting in the repository yet, written or supported.

Paste the completed PITCH.md once the team drafts it.

## Your four answers

The four lines under `## Priya asked` in your PITCH.md are still empty. They
are one line each and they are not a coding job: cost, what happens when it is
wrong, who runs it in June, and what you left out. Whoever on your side is not
editing agent.py is the right person to write them, and they are the four
things I will ask about first.

## Before our next meeting

> Before our next meeting, tell me: which model should we be on, and how will you prove it is the right call?
>
> Priya Raghavan, Larkspur Airlines

Bring two things. A recommendation, and the measurement behind it. If the model is
not the problem, say so, and bring the number that shows it.

## What this review read

- `agent.py (226 lines)`
- `PITCH.md (unchanged template)`
- `TEAM.md (unchanged template)`

Reviewer: `claude-sonnet-5`. Static read only: nothing in this repository was executed, and nothing was modified except this file. Larkspur Airlines is a fictional training scenario. Confidential, do not distribute.
