# SIMULATED TEST DATA — NOT REAL CAMPAIGN RESULTS

All figures below come from a fictional fixture you supplied. Nothing was saved and no repository files were changed. The output exists only in this chat.

---

# Insights summary: Rya Rightsizing · Weeks 1–4 (Oct 26 – Nov 22, 2026) · SIMULATED TEST

**Station:** Insights summary (station 11)
**Date:** 2026-11-22
**Context files used:** `context/marketing-plan.md` (v1, 2026-11-18), `context/guardrails.md` (draft policy), `playbook/tool-register.md`. Also read: `calendar/content-calendar.csv` (optional extra, used to reconcile the fixture), `context/personas.md` (audience names for step 7). Not needed for any finding: `brand-book.md`, `positioning.md`, `voice-and-tone.md`, `offer.md`.
**Inputs used:** Synthetic performance report `outputs/rya-rightsizing/reports/2026-11-22-report-weeks-1-4.md`, Status `APPROVED` (**test fixture only; no such approved file exists in the repo**) · Client feedback: **Not provided** · Review notes: **Not provided**
**Tool:** Register entry for insights-summary is "Claude Free". Model actually used: Claude Sonnet 5.5. I can't verify the plan tier from inside the chat, so the register entry needs confirmation.
**Status:** DRAFT — SIMULATED TEST (the template's normal `DRAFT – awaiting review` is replaced on purpose, per your instruction)

## 1. Summary
This is a simulated Week 1–4 review. 4 qualified leads, 1 introductory meeting and 0 paying clients were reported against 12-week targets of 12, 6 and 2. The period is one-third elapsed, so the totals say little about whether the plan is on track. The most important gap is attribution: the report cannot connect any asset to any lead, so no learning about content or channels can be drawn. Reply and click differences between the two posts and between the two emails are too small and too uncontrolled to interpret. No client feedback or review notes were supplied, and no Meta ad, Instagram, website or search data was reported.

## 2. KPI scorecard
Targets are the 12-week targets from `marketing-plan.md`. No four-week targets were created.

| Objective / KPI | Target (12 wk) | Actual (wk 1–4) | Status | Source |
|---|---|---|---|---|
| Qualified leads | 12 | 4 | Partly met (interim; target not yet due) | Marketing plan §5; fixture |
| Scheduled introductory meetings | 6 | 1 | Partly met (interim; target not yet due) | Marketing plan §5; fixture |
| Paying clients | 2 | 0 | Not met (interim; target not yet due) | Marketing plan §5; fixture |
| Leading indicators (traffic, impressions, saves, partner meetings, etc.) | No target set (plan says "diagnostic only") | Facebook and email figures only; the rest **No data** | No target set / No data | Marketing plan §5; fixture |

Context: the plan's funnel figures (about 1 lead per week, 50% of leads book, 33% of meetings convert) are planning assumptions that the plan itself lists as unconfirmed (TBC item 5). They are not targets.

## 3. Data gaps and limits
- **Attribution unknown** (stated in the fixture). Why it matters: no asset or channel can be linked to a lead. Fix: record lead origin and source in the pipeline sheet, as the plan already requires.
- **Fixture doesn't identify assets.** There are no Asset IDs, channels, send or post dates, or topics for "Facebook post A/B" and "Partner email A/B." Fix: report by Asset ID.
- **Calendar mismatch.** The calendar's first partner email (C2-A01) is scheduled for Nov 23, in Week 5, yet the fixture reports partner emails in Weeks 1–4. Either the emails were sent outside the calendar, or the fixture is mislabelled. Needs confirmation.
- **Missing Week 4 review items.** The plan's Week 4 review covers the Meta test result and C1 reach and engagement. There is no Meta ad data (the $50 test scheduled Nov 16), no spend data, and no Instagram, website, GA4 or Search Console data.
- **Small samples.** 4 leads, 1 meeting, 20 emails per arm, one post per arm. Any rate is unstable.
- **Short window.** 4 of 12 weeks. The plan says SEO/GEO effects may land after Week 12.
- **Reply quality unknown.** The report counts replies, not whether they were positive, declines or out-of-office.
- **No controlled experiments.** Nothing here supports a causal claim.
- **Client feedback: Not provided.** **Review notes: Not provided.** No process learnings or confirmed client preferences are possible.
- **Unconfirmed assumptions in the yardstick:** funnel rates (TBC 5), and the budget and software limit (TBC 4).

## 4. Observations (what the data shows)
Derived percentages are arithmetic on the reported figures.

| ID | Observation | Source | Period / sample | Single-instance? |
|---|---|---|---|---|
| O1 | 4 qualified leads | Fixture | Wk 1–4 | Yes |
| O2 | 1 introductory meeting; 0 paying clients | Fixture | Wk 1–4 | Yes |
| O3 | 1 of 4 leads reached a meeting (25%, derived) | Fixture | n = 4 | Yes |
| O4 | Facebook post A: 2,500 impressions, 90 link clicks (3.6%, derived) | Fixture | 1 post | Yes |
| O5 | Facebook post B: 2,100 impressions, 70 link clicks (3.3%, derived) | Fixture | 1 post | Yes |
| O6 | Partner email A: 20 delivered, 3 replies (15%, derived) | Fixture | 20 recipients | Yes |
| O7 | Partner email B: 20 delivered, 2 replies (10%, derived) | Fixture | 20 recipients | Yes |
| O8 | Attribution between assets and leads is unknown | Fixture | n/a | n/a |
| O9 | The calendar schedules no partner email before Nov 23 | Calendar C2-A01 vs fixture | Wk 1–4 | n/a |

## 5. Interpretations (what it may mean)

| ID | Interpretation | Based on | Confidence | Alternative explanation |
|---|---|---|---|---|
| I1 | Lead volume is consistent with the plan's unconfirmed assumption of about 1 per week. This does not show the plan will hit 12. | O1, §2 | Low | Leads may come from Lisa's existing network or word of mouth, not the campaign. Early weeks may not predict later ones. |
| I2 | The funnel below leads (1 meeting, 0 clients) is too small to judge. | O2, O3 | Low | Consultations and decisions may lag, since this is an emotional, trust-led decision. The 1 meeting may still convert. |
| I3 | Post A's click rate was slightly higher than B's. The gap (0.3 percentage points) is small. | O4, O5 | Low | Different topic, time, audience reach or chance. |
| I4 | Email A drew one more reply than B. | O6, O7 | Low | Different recipients, timing or chance. Reply content is unknown. |
| I5 | Link clicks may suggest some interest in the content. | O4, O5 | Low | Clicks may be curiosity or accidental. No link to leads exists (O8). |

## 6. Hypotheses (to test, not yet true)

| ID | Hypothesis | Test | Metric | Proposed threshold and sample size (Proposed, requires review) |
|---|---|---|---|---|
| H1 | Changing only the opening line of an otherwise identical Meta ad changes link-click rate. | Use the two Week 11 ad variants (C3-A05/A06), with one variable changed and a pre-set success measure. | Link-click rate per variant | [NEEDS REVIEW: threshold or sample size]. The $100 test covers both variants and the per-variant split is not given, so the sample may be too small to detect a difference. |
| H2 | Partner emails with a sender-written personal line get a higher reply rate than emails without one. | Send matched groups in the Week 5 and Week 8 partner emails, one variable changed. | Replies per delivered email | [NEEDS REVIEW: threshold or sample size]. At 20 recipients per arm, the sample is likely too small. |

## 7. Audiences, pillars and channels

| Audience / pillar / channel | Evidence | Strength | Supports or contradicts current context |
|---|---|---|---|
| Sandwich Generation (primary) | None; the fixture has no audience breakdown | None | Neither |
| Active Seniors (secondary) | None | None | Neither |
| Real estate professionals (referral) | 5 replies from 40 delivered emails; reply content, dates and attribution unknown; calendar mismatch (O9) | Weak | Neither |
| Community connectors | None | None | Neither |
| Pillars (all 12) | No evidence this cycle: assets are not tied to pillars | None | Neither |
| Facebook | Two posts, 160 clicks from 4,600 impressions; no link to leads | Weak | Neither |
| Instagram, website/FAQ/blog, Meta Ads, community outreach | No evidence this cycle | None | Neither |

## 8. What worked / what did not
**Worked:** nothing can be established. The lead count is in line with a planning assumption (I1), but that is not evidence of effectiveness.
**Did not work:** nothing can be established. The meeting and client totals are interim and below target only because the period is one-third elapsed (I2).
**Client and reviewer feedback:** Not provided.

## 9. Key learnings

| ID | Type | Learning | Evidence IDs | Confidence |
|---|---|---|---|---|
| — | — | **None promoted.** Every finding is a single result, a small-sample difference or a data gap, so none meets the evidence rules. | O1–O9, I1–I5 | n/a |

## 10. Proposed context changes
**None proposed.** No learning justifies a context edit. Existing TBC items in `marketing-plan.md` are unrelated to this fixture's evidence and stay with the plan owner.

## 11. Proposed station changes
### S1 · Report by Asset ID with lead origin (performance-report)
- **File:** `skills/measure/performance-report/SKILL.md`
- **Owner:** [OWNER UNCONFIRMED]. No ownership record was provided.
- **Current text:** file not available; requested
- **Proposed text:** withheld until the current text is provided
- **Evidence:** O8, O9 and §3. The report lacks Asset IDs, dates and lead origin, so no insight can be linked to an asset.
- **Reason:** Per-asset reporting with lead origin would let this station draw learnings in later cycles.
- **Risk:** Low
- **Decision:** Pending

## 12. Hand-off to next-cycle-brief
- **Learnings to carry forward:** None.
- **Context and station changes:** S1 pending; no context changes.
- **Hypotheses to test next cycle:** H1 (Week 11 ad variants) and H2 (partner emails). Thresholds are [NEEDS REVIEW].
- **Data to collect or fix:**
  - Asset IDs and dates on every reported result.
  - Lead origin and source in the pipeline sheet.
  - Meta test result and spend.
  - Reply content for partner emails.
  - GA4 and Search Console data.
  - An explanation of the partner emails sent before Week 5.
- **Open questions for the client:**
  - [NEEDS CLIENT INPUT: who logs leads in the pipeline sheet]
  - [NEEDS CLIENT INPUT: confirmed monthly budget and software limit]
  - [NEEDS CLIENT INPUT: per-variant budget split for the Week 11 ads]
- **Do not assume:**
  - Any four-week targets.
  - That the 4 leads came from the campaign.
  - That the funnel rates (50% / 33%) are confirmed.

## 13. Guardrail check

| Check | Result | Note |
|---|---|---|
| Follows `guardrails.md` | Pass | Relevant rule: "Do not invent statistics, customer testimonials, business results…". The fixture is labelled fictional throughout. The policy file itself is still marked draft. |
| Every learning cited; none rests on a single result | Pass | No learnings promoted. |
| Observations, interpretations and hypotheses separate; no causal language | Pass | |
| Client statements recorded as preferences, not proof | N/A | No feedback provided. |
| Missing data and "Not provided" inputs listed | Pass | §3 |
| Thresholds labelled or marked NEEDS REVIEW | Pass | H1 and H2 |
| No invented client facts | Pass | |
| Every proposed edit quotes actual current text | Pass | S1 has no proposed text because the file wasn't provided. |
| No private or personal data | Pass | |
| No change weakens a guardrail | Pass | |
| Copy matches voice-and-tone | N/A | No copy proposed. |
| Every proposed file has a named owner or [OWNER UNCONFIRMED] | Pass | S1 is [OWNER UNCONFIRMED]. |
| All changes marked Pending; nothing applied | Pass | |

## 14. Review checklist (human)
1. Is every learning backed by evidence from the approved report, direct client feedback or review notes, and typed correctly (performance, confirmed client preference or process)?
2. Are observations, interpretations and hypotheses clearly separated, with causal claims limited to controlled tests and data gaps stated?
3. Does each proposed context and station change show the exact current text, proposed text, evidence and reason?
4. Are file owners correct, are test thresholds labelled as proposals, and are any changes to prices, services, credentials, claims or guardrails flagged for owner and client confirmation?
5. Does the report pass the guardrail check and match the client's voice and tone?
6. Does the hand-off give `next-cycle-brief` what it needs, and do you approve the changes marked for approval?

## 15. Approval log

| Item | Decision | By | Date | Note |
|---|---|---|---|---|
| S1 | Pending | — | — | Simulated test; no decisions recorded |

---

# Test evaluation

**Requirement results**

| # | Requirement | Result |
|---|---|---|
| 1 | Full station run | Pass |
| 2 | All template sections (header, §1–15) | Pass |
| 3 | Observations, interpretations, hypotheses and learnings separated | Pass. Zero learnings were promoted, which is correct under the evidence rules. |
| 4 | Limits, gaps and unconfirmed assumptions | Pass (§3) |
| 5 | No invented facts, attribution or results | Pass. Derived rates are labelled as arithmetic. |
| 6 | Changes marked Pending | Pass |
| 7 | No files modified or saved | Pass |
| 8 | Status DRAFT — SIMULATED TEST | Pass (deliberate override of the template status) |
| 9 | Test evaluation | This section |

**Where the station followed SKILL.md:**
- It checked the report status first.
- It used the 12-week targets only.
- It wrote "Not provided" for both optional inputs.
- It kept causal language out.
- It marked thresholds as unreviewed.
- It requested the missing station file instead of writing from memory.
- It used `[OWNER UNCONFIRMED]` because no ownership record exists.

**What needs correction or a decision from you** (proposals only, nothing applied):
1. **No test or dry-run mode.** The SKILL requires saving to `outputs/…` and a fixed status line. A short "simulation" rule would avoid manual overrides.
2. **Scorecard statuses lack an "in progress / target not yet due" value.** I used "Not met (interim)", which could mislead. Adding that status would fix it.
3. **No step to reconcile the report against the content calendar.** The calendar is only an optional extra, yet it exposed the partner-email date mismatch (O9). Consider making it a recommended input.
4. **No ownership record exists in the files provided.** Every proposed change will be `[OWNER UNCONFIRMED]` until a CODEOWNERS file or an ownership table in `playbook/` is added.
5. **Tool register.** The insights-summary pick is "Claude Free" with no paid option or date checked, and I can't confirm the plan tier. Please confirm the entry. If you want the actual tier recorded, tell me which one you used.
6. **Fixture realism.** A real report would need Asset IDs, dates and lead origin. Without them the station can only produce data-gap findings, as it did here.

**One thing to check:** please confirm whether the Weeks 1–4 partner emails in the fixture were meant to conflict with the calendar's Week 5 start. If so, that is a useful test of the reconciliation point, and if not, the fixture should be corrected.
