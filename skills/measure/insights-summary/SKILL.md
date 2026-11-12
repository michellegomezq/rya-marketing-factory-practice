---
name: insights-summary
description: "Factory station 11 (measure line). Reads the approved performance report, client feedback and review notes, then turns them into evidence-based learnings and exact, human-approved proposals for the context pack and station SKILL.md files. Use when asked what we learned, how to improve the factory, or to update context after a campaign."
---

# Station: Insights summary

**Line:** Measure · **Needs:** performance-report · **Feeds:** next-cycle-brief and the `/context` pack

**Job:** Close the loop. Turn results into changes that make the next cycle better, without overclaiming what the evidence shows.

**This station proposes. It never edits context files or station files.** Every change waits for human approval and is then applied by the file owner through the team's existing GitHub editing and commit workflow.

---

## 1. Inputs

**Required (stop and ask if any is missing):**

| Input | Where to find it | Condition |
|---|---|---|
| Approved performance report | `outputs/<client-slug>/YYYY-MM-DD-performance-report-<period>.md` | Status must be `APPROVED`. If it is `DRAFT`, stop and say so. |
| Marketing plan | `context/marketing-plan.md` | Source of objectives, KPIs, targets and reporting period. This is the yardstick for "worked" and "did not work." |
| Guardrails | `context/guardrails.md` | Always read before analysing. |

**Optional evidence (record "Not provided" and continue if unavailable):**

| Input | Where to find it | Notes |
|---|---|---|
| Client feedback | Pasted into chat or uploaded (emails, call notes, comments, testimonials, complaints) | Record the source and date of each item. |
| Review notes | The human reviewer's notes from earlier review gates, pasted or uploaded | Include approvals, rejections and edits made at review gates. |

If either optional input is not provided, write "Not provided" in the report header and in the data gaps section, then continue with the available evidence. Do not infer what feedback or review notes might have said.

**Other context files, read only when needed:**

`context/brand-book.md`, `context/personas.md`, `context/positioning.md`, `context/voice-and-tone.md` and `context/offer.md` are used when a specific finding or proposed edit relates to them. Station `SKILL.md` files are used only when proposing a station change.

- If a file is needed for a specific finding or edit and is missing or unreadable, name the file, say which finding or edit needs it, and request it. Do not reconstruct its contents from memory or from other files.
- If a file is not needed for any finding, do not request it.
- Optional extras: the previous insights summary, the previous next-cycle brief, the content calendar.
- Set `<client-slug>` and `<period>` from the performance report. If they are unclear, ask one question.
- Client facts (names, prices, services, audiences, claims) come only from the context files, the report or the feedback. This station holds none.

---

## 2. Steps

1. **Check inputs.** Confirm the report is approved, the period matches, and `marketing-plan.md` and `guardrails.md` are readable. Record "Not provided" for any missing optional input. List anything missing before going further.
2. **Build the KPI scorecard.** From `marketing-plan.md`, list each objective and KPI with target, actual (from the report) and status: Met / Partly met / Not met / No target set / No data. If a target is missing, mark `[NEEDS CLIENT INPUT: target for <KPI>]`. Do not make one up.
3. **Log data gaps and limits.** Note missing channels or metrics, small samples, short windows, tracking or attribution problems, one-off events (holidays, outages, a single viral post), optional inputs marked "Not provided," and anything the report flags as unreliable. Do this before interpreting, so the limits shape the analysis.
4. **Write observations.** State only what the data or feedback shows: the figure or statement, source, period and sample size. No explanations at this stage. A single result may be reported here as an observation, labelled as single-instance, without generalising it. Give each an ID (O1, O2...).
5. **Write interpretations.** For each important observation, say what it may mean. Give a confidence level (High / Medium / Low) and at least one alternative explanation. Give each an ID (I1, I2...) and cite the observations behind it. Interpretations are not causal claims.
6. **Write hypotheses.** For anything plausible but unproven, state a testable hypothesis (H1, H2...) with: what to change, the metric to watch, what result would support or reject it, and a proposed threshold and sample size or duration. Apply the threshold rule below. Hypotheses are not learnings.
7. **Map evidence to audiences, pillars and channels.** Use the persona, content pillar and channel names defined in the context pack. For each, record what the evidence shows, how strong it is (Strong / Moderate / Weak / None), and whether it supports or contradicts the current context. Write "No evidence this cycle" where that is the case. If the persona or pillar definitions are needed and unavailable, request the file.
8. **Sort what worked and what did not.** Judge against the KPIs and targets, not against feelings or vanity metrics. Report client or reviewer reactions separately, labelled as feedback, not performance.
9. **Write key learnings.** Apply the evidence rules below. Promote a finding to a learning (L1, L2...) only when it meets them. Label each learning's type: *Performance learning* (supported by the report), *Confirmed client preference* (explicit client statement) or *Process learning* (patterns in review notes).
10. **Propose context changes.** For each learning that justifies one:
    - Open the current file. If it is unavailable, stop and request it for this edit.
    - Copy the exact current text. Write the exact proposed text.
    - Give the evidence (observation, interpretation, feedback IDs) and the reason.
    - Identify the file owner (see step 12).
    - Mark risk: Low (wording, examples), Medium (messaging, audience, offer framing), High (prices, services, credentials, claims, guardrails).
    - If the evidence supports only a test, propose a test, not an edit.
    - Never propose loosening `guardrails.md` without noting that it needs the owner's and the client's explicit sign-off.
    - Never write a new client fact (price, credential, statistic, testimonial). If one is needed, use `[NEEDS CLIENT INPUT: ...]`.
11. **Propose station changes.** Use the same format against the relevant station `SKILL.md`: file, current text, proposed text, evidence, reason. Base these on patterns in review notes (repeated edits, rejections, missing inputs) and on report findings. If review notes are "Not provided," propose station changes only where the report itself supports them. If the station file is unavailable, request it.
12. **Check file ownership.** Look in the team repo for an ownership record (e.g. `CODEOWNERS`, a `README` or an ownership table in `playbook/`). Name the owner of each file you propose to change. If ownership is not recorded, write `[OWNER UNCONFIRMED]` and ask. Do not assume. Changes to files the reviewer does not own are proposals for that owner to review.
13. **Write the hand-off.** Give `next-cycle-brief` the learnings, the approved, pending or rejected status of each change, hypotheses to test, gaps to close and open questions. Mark anything that depends on unapproved changes.
14. **Run the guardrail check** (section 4), save the report, and show the review checklist. Stop and wait for approval.
15. **After approval only:** list the approved changes with their IDs so the file owner can apply them using the team's existing GitHub editing and commit workflow. Branches and pull requests are optional unless the team requires them. Do not apply any change yourself. Record each decision in the approval log. Update the report status to `APPROVED` only when the human reviewer says so. Rejected or deferred changes stay in the report with the reason.

### Evidence rules

| Evidence type | What it can support | What it cannot support |
|---|---|---|
| **Single result** (one post, email, ad, week) | Reported as an observation, labelled single-instance. | A learning, a generalisation, or a context change on its own. |
| **Repeated pattern** across posts, channels or periods in the report | An interpretation, and a learning if confidence is at least Medium and alternatives are noted. | A causal claim. |
| **Explicit client statement** (a stated preference, constraint or correction) | A *confirmed client preference*, which can justify a context edit. Record the source and date. | Campaign effectiveness. What a client says they like is not evidence that it performed. |
| **Review-note pattern** (repeated edits or rejections) | A process learning and station-change proposals. | Claims about audience response. |
| **Before-and-after comparison** | An observation and an interpretation, with confounders listed. | Causation, because other things changed too. |
| **Appropriately designed controlled test** (for example an A/B test with a defined comparison, one changed variable, adequate sample and a pre-set success measure, or another method that justifies the comparison) | A causal claim, limited to the conditions tested. State the design and its limits. | Claims beyond the audience, channel and period tested. |

**Language for claims:**

- Use "coincided with," "is consistent with," "may suggest," "one possible explanation is" for anything that is not a controlled test.
- Use "caused," "drove," "led to," "because of" only for results from a controlled test that meets the design test above.
- Do not generalise from a single result. Do not treat a lack of data as a lack of effect. Do not claim results the report does not contain.

**Threshold and sample-size rule:**

- Any threshold, sample size, duration or significance level you suggest for a test is labelled **"Proposed, requires review"** unless it comes from the approved marketing plan, the approved performance report's method or another approved plan, or a stated, justified method (name the method and show the inputs).
- Do not present proposed thresholds as standards or as facts.
- If no basis exists for a number, write `[NEEDS REVIEW: threshold or sample size]` instead of guessing.

---

## 3. Output template

**Save path:** `outputs/<client-slug>/YYYY-MM-DD-insights-<period>.md`

```markdown
# Insights summary: <Client name> · <period>

**Station:** Insights summary (station 11)
**Date:** YYYY-MM-DD
**Context files used:** <list each file actually read, with date or version if known>
**Inputs used:** <approved performance report path and status · client feedback: items and dates, or "Not provided" · review notes: summary, or "Not provided">
**Tool:** <from playbook/tool-register.md, or: register unavailable, entry needs confirmation; model used: <actual model>>
**Status:** DRAFT – awaiting review

## 1. Summary
<3–5 sentences: how the period went against the objectives, the most important learnings, the most important gaps.>

## 2. KPI scorecard
| Objective / KPI | Target | Actual | Status | Source |
|---|---|---|---|---|

## 3. Data gaps and limits
- <gap or limit · why it matters · what would fix it>
- <include "Not provided" optional inputs>

## 4. Observations (what the data shows)
| ID | Observation | Source | Period / sample | Single-instance? |
|---|---|---|---|---|

## 5. Interpretations (what it may mean)
| ID | Interpretation | Based on | Confidence | Alternative explanation |
|---|---|---|---|---|

## 6. Hypotheses (to test, not yet true)
| ID | Hypothesis | Test | Metric | Proposed threshold and sample size (Proposed, requires review) |
|---|---|---|---|---|

## 7. Audiences, pillars and channels
| Audience / pillar / channel | Evidence | Strength | Supports or contradicts current context |
|---|---|---|---|

## 8. What worked / what did not
**Worked:** <items with IDs>
**Did not work:** <items with IDs>
**Client and reviewer feedback:** <items, labelled as feedback, with source and date, or "Not provided">

## 9. Key learnings
| ID | Type (Performance / Confirmed client preference / Process) | Learning | Evidence IDs | Confidence |
|---|---|---|---|---|

## 10. Proposed context changes
### C1 · <short title>
- **File:** `context/<file>.md`
- **Owner:** <name or [OWNER UNCONFIRMED]>
- **Risk:** Low / Medium / High
- **Current text:** "<exact quote>" *(or: file not available; requested)*
- **Proposed text:** "<exact replacement>"
- **Evidence:** <IDs>
- **Reason:** <why this change makes the next cycle better>
- **Decision:** Pending

## 11. Proposed station changes
### S1 · <short title>
- **File:** `<path>/SKILL.md`
- **Owner:** <name or [OWNER UNCONFIRMED]>
- **Current text:** "<exact quote>" *(or: file not available; requested)*
- **Proposed text:** "<exact replacement>"
- **Evidence:** <IDs>
- **Reason:** <...>
- **Decision:** Pending

## 12. Hand-off to next-cycle-brief
- **Learnings to carry forward:** <IDs and types>
- **Context and station changes:** <approved / pending / rejected, by ID>
- **Hypotheses to test next cycle:** <IDs with suggested test; thresholds marked "Proposed, requires review">
- **Data to collect or fix:** <list>
- **Open questions for the client:** <list, using [NEEDS CLIENT INPUT: ...] where relevant>
- **Do not assume:** <anything that depends on a pending change>

## 13. Guardrail check
<results from section 4 of the SKILL>

## 14. Review checklist
<the six questions from section 5 of the SKILL, unanswered>

## 15. Approval log
| Item | Decision (Approved / Rejected / Deferred) | By | Date | Note |
|---|---|---|---|---|
```

---

## 4. Guardrail check

Run this before presenting the report. Report each line as Pass / Fail / N/A with a note.

- Follows `context/guardrails.md` (claims, privacy, AI disclosure, audience sensitivity). Quote the relevant rule if a finding touches one.
- Every learning has cited evidence and meets the evidence rules. No learning rests on a single result alone.
- Observations, interpretations and hypotheses are separate. Causal language appears only for controlled tests that meet the design test.
- Client statements are recorded as confirmed preferences, not as proof of effectiveness.
- Missing data, "Not provided" inputs and unreliable metrics are listed, and no conclusion depends on data that is not in the report.
- Proposed thresholds and sample sizes are labelled "Proposed, requires review" unless sourced from an approved plan or justified method.
- No invented client facts: prices, services, credentials, testimonials, statistics or results. Gaps are marked `[NEEDS CLIENT INPUT: ...]`.
- Every proposed edit quotes the actual current text. No edit was written from a file that was not provided.
- No private or personal data from clients, customers or their families appears in the report beyond what the guardrails allow. Feedback is summarised or anonymised as the guardrails require.
- No proposed change weakens a guardrail. If one does, it is flagged High risk and needs owner and client sign-off.
- Proposed copy changes match `voice-and-tone.md` where that file was needed and read.
- Every proposed file has a named owner or is marked `[OWNER UNCONFIRMED]`.
- All changes are marked Pending. Nothing has been applied.

---

## 5. Review checklist (human)

Answer yes or no. Any "no" means revise before approval.

1. Is every learning backed by evidence from the approved report, direct client feedback or review notes, and typed correctly (performance, confirmed client preference or process)?
2. Are observations, interpretations and hypotheses clearly separated, with causal claims limited to controlled tests and data gaps stated?
3. Does each proposed context and station change show the exact current text, proposed text, evidence and reason?
4. Are file owners correct, are test thresholds labelled as proposals, and are any changes to prices, services, credentials, claims or guardrails flagged for owner and client confirmation?
5. Does the report pass the guardrail check and match the client's voice and tone?
6. Does the hand-off give `next-cycle-brief` what it needs, and do you approve the changes marked for approval?

**Nothing is applied until the human reviewer says "approved."** Approved changes are applied by the file owner using the team's existing GitHub editing and commit workflow.

---

## 6. Tool slot

**Job:** synthesis.

**Current tool:** Claude, used to build and test this station. This is the working entry until the tool register is confirmed.

Check `playbook/tool-register.md` for the synthesis entry and record it in the report header.

- If the register is unavailable, or has no synthesis entry, flag at the top of the response that the entry needs confirmation, and record the actual model used (for example, the model name shown in the interface). Do not guess the model or what the register says.
- If the register lists a different tool from the one in use, flag the mismatch and ask the human reviewer which to use.
