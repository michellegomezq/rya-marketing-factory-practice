---
name: next-cycle-brief
description: "Use this station to plan the next campaign cycle. It turns approved insights, client priorities, dates and budget into a brief for the marketing-plan and content-calendar stations."
---

# Station: Next-cycle brief

**Line:** Measure  
**Needs:** Approved output from insights-summary  
**Feeds:** Marketing-plan and content-calendar

## 1. Inputs

- Read the approved insights summary for the previous cycle. Use its findings, evidence IDs, approval decisions and suggested tests.
- Gather the client's priorities for the next period, key dates, available budget and capacity. Record which details the client has confirmed.
- Read `context/marketing-plan.md` for the current objectives and KPI definitions, `context/personas.md` for audience names, `context/positioning.md` for messaging and `context/guardrails.md` for client rules. Check `context/offer.md` when the brief mentions a service or price.
- Use `templates/client-brief.md` for the brief's structure.

## 2. Steps

1. Check that the insights summary is approved and identify the period it covers. If it is missing or still a draft, ask for the approved summary before writing the brief.
2. Choose one main objective for the next cycle. Explain which approved finding and client priority support it. Flag any conflict for the reviewer.
3. Define how the team will measure the objective. For each KPI, give the target, data source and review date. Label a suggested target as proposed until the client confirms it.
4. Select the priority persona and content pillar. Use the names from the team’s context files and explain why each fits the objective.
5. List the assets needed, the station responsible for each, and the deadlines. Check the schedule and planned costs against confirmed dates, budget and capacity. Mark missing details `[TBC]`.
6. Select a test supported by the previous cycle’s findings. State what will change, what will be compared and which KPI will guide the decision. If the evidence does not yet support a test, record what the team needs to learn first.
7. Present the draft for human review. After approval, pass the objective, KPIs, asset list, dates and test instructions to the marketing-plan and content-calendar stations.

## 3. Output template

Follow `templates/client-brief.md`, keeping its headings and adding any missing planning fields below. If the template is unavailable, use these fields for the draft and flag the template check for review.

Save path: `outputs/<client-slug>/reports/YYYY-MM-DD-brief-<period>.md`

# Next-cycle brief — <client and planning period>

**Station:** Next-cycle brief  
**Date:** <date prepared>  
**Context files used:** <files actually reviewed>  
**Status:** DRAFT – awaiting review

### Objective and evidence
<One main objective, the client priority it addresses and the approved finding that supports it.>

### Audience and message
<Priority persona, content pillar, key message and call to action.>

### Measurement
| KPI | Target and confirmation status | Data source | Review date |
|---|---|---|---|

### Calendar hand-off
| Asset | Channel and format | Responsible station | Deadline | Budget or capacity constraint |
|---|---|---|---|---|

### Test for this cycle
<Approved finding or hypothesis ID, proposed change, comparison, KPI and decision rule.>

### Client confirmations
<List open decisions, who can confirm each one and which part of the brief depends on it.>

## 4. Guardrail check

- Follow `context/guardrails.md`. Check service details and public claims against the current client files.
- Trace each recommendation to an approved finding or a stated client priority. Keep hypotheses labelled as tests.
- Use KPIs the team can measure. Mark unknown targets, dates, costs or capacity `[TBC]`.
- Identify any work that exceeds the budget or available time. Ask the reviewer to adjust the scope before handing it to the calendar lead.

## 5. Review checklist (human)

- [ ] Does the brief have one clear objective supported by an approved insight and a client priority?
- [ ] Can the team measure each KPI using the named data source?
- [ ] Do the audience, pillar, message and call to action match the client context?
- [ ] Are the budget, capacity and deadlines confirmed or clearly marked for follow-up?
- [ ] Does the proposed test explain what result would guide the next decision?
- [ ] Does the calendar lead know which assets to schedule and which decisions are still pending?

## 6. Tool slot

**Job:** Planning.  
Check `playbook/tool-register.md` for the team's current planning tool. Record the tool and model actually used when running the station. If the register is unavailable, flag the entry for confirmation.
