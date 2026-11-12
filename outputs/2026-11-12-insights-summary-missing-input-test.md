# Missing-input test, not a campaign analysis

**Station:** Insights summary (station 11), run against the revised draft · **Date:** 2026-11-12 · **Context files used:** `guardrails.md` (read for the input check only) · **Status:** `DRAFT – awaiting review`

## Result: stopped at step 1

The station requires an approved performance report, `marketing-plan.md` and `guardrails.md`, and says to stop and ask if any is missing. Two of the three are missing, so I stopped before building a scorecard, observations, learnings or change proposals. No report file was saved.

## Input check

| Input | Status | Notes |
|---|---|---|
| Approved performance report | **Missing (blocking)** | Nothing in the Project. Without it I can't set `<client-slug>` or `<period>`, or confirm `APPROVED` status. |
| `context/marketing-plan.md` | **Missing (blocking)** | Not in the Project, so there are no objectives, KPIs, targets or reporting period to judge results against. |
| `context/guardrails.md` | Available | Read as `guardrails.md`. The file itself says it is a draft policy until the team approves it. |
| Client feedback | Not provided | Optional. Recorded as "Not provided." |
| Review notes | Not provided | Optional. Recorded as "Not provided." |

## Other context files

These are present but not needed, since there are no findings or proposed edits to relate them to: `brand-book`, `voice-and-tone`, `personas`, `positioning` and `offer`. No file was requested beyond the two blocking items.

## Tool slot

I can't see `playbook/tool-register.md` in the Project. **The synthesis entry needs confirmation.** The actual model used for this test is Claude Sonnet 5.5.

## What I need to proceed

1. The approved performance report (with its period), and
2. `marketing-plan.md`. Rya's `guardrails.md` cites a "Team Marketing Plan (October 22, 2026)" as a source, so a version may already exist.

I didn't infer, estimate or reconstruct either document.

## Guardrail check (limited to what applies)

- Follows `guardrails.md`: **Pass**
- No invented client facts, results or campaign data: **Pass**
- No edits proposed, nothing applied: **Pass**
- Missing data and "Not provided" inputs listed: **Pass**
- All other lines (evidence rules, thresholds, current-text quotes, owners): **N/A**, because no analysis ran

## Review checklist for this test

1. Did the station stop on the two missing required inputs rather than analysing around them?
2. Did it record client feedback and review notes as "Not provided" and treat them as non-blocking?
3. Did it avoid inventing a plan, report, KPIs or results?
4. Did it request only the files it actually needed?
5. Did it flag the missing tool register and name the actual model used?
6. Is the stop message clear about what to supply next?

## Things I noticed while running it

- The Project files use names like `brand-book__1_.md` and live under `/mnt/project/`, not `context/`. The station's `context/...` paths won't match until the repo layout is confirmed.
- The `SKILL (1).md` uploaded in the Project is still the original stub. I ran the revised version from our conversation. Replace the uploaded file before further testing.
- `positioning.md` has a `[PLACEHOLDER – sync from team repo]` version line, so its currency is unverified.

**What to check:** whether you want the station to also save a short "stopped" note to `outputs/<client-slug>/`. The current draft doesn't, and it couldn't set the slug or period here anyway.

Waiting for your approval or edits.
