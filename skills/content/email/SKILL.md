---
name: email
description: Factory station 6 (content line). Turns one content-calendar row whose Station is email into ready-to-send email copy - a one-to-one or partner outreach email, a follow-up, a newsletter, or a short welcome or nurture sequence - plus any companion piece the row sends by email (one-pager, referral card). For each email it writes the goal, send timing, three subject lines, preview text, body, one CTA, sign-off, a footer that meets CASL, merge fields and tracked links, and it records the consent basis for every recipient group. Also writes a sources file tracing every claim to the context pack. Flags unapproved pricing, unclear consent and missing contact details instead of guessing. Use when asked for an email, partner or referral email, introduction email, follow-up, newsletter, welcome or nurture sequence, subject lines or preview text.
---

# Station: Email

**Line:** Content · **Needs:** content-calendar, positioning-messaging · **Feeds:** performance-report

**Job:** Keep warm leads moving toward a conversation with the client.

---

## 1. Inputs

**Required context files** (read all of them before writing anything)
- `context/positioning.md`: pillars, proof points, persona and partner messages, positioning statement
- `context/personas.md`: the recipient's goals, fears, questions and preferred materials
- `context/offer.md`: confirmed services, service area, consultation, pricing status
- `context/voice-and-tone.md`: voice, tone by situation, say / never-say lists, CTAs, sign-off and geography rules
- `context/brand-book.md`: business name, sender name, contact details, mailing address, imagery and photo-permission rules
- `context/guardrails.md`: claims, privacy, AI disclosure, audience sensitivity

**Also required**
- `calendar/content-calendar.csv`: the row for this Asset ID (Topic, Format, Channel, Target audience, Specs, CTA, Notes, Notes for the client)
- `context/marketing-plan.md`: the hand-off block (campaign, phase, key message, KPIs, spending controls)

**Optional**
- Approved assets this email links to or attaches, from `outputs/<client-slug>/` (article, landing page, PDF)
- Earlier emails in the same sequence or to the same recipients, so nothing repeats
- Results from earlier sends (replies, clicks, unsubscribes) from performance-report

If the body of a required file is still a placeholder, stop and tell the user which file is incomplete. If only a version line says `[PLACEHOLDER`, flag it in the output and continue.

**Required from the user for each asset** (if any item is missing, ask for all missing items in one message)
1. **Asset ID:** exactly as it appears in the calendar
2. **Email type:** one-to-one outreach, follow-up, newsletter, or sequence (welcome or nurture), and how many emails
3. **Recipients and how they joined:** who they are, and how the client got their address (sign-up form, inquiry, past client, referral from a named person, business address published on their website, personal contact). This decides the consent basis in step 3
4. **Sender and sending tool:** who the email comes from, and whether it is sent by hand from the client's inbox or through the email tool in `playbook/tool-register.md`
5. **Links and attachments:** URLs or Asset IDs the email points to, and any file attached. Never invent a URL

---

## 2. Steps

1. **Read the row and confirm the brief.** Restate in five lines or fewer: Asset ID, email type, recipients, campaign and phase, CTA, send week. Flag any conflict between the calendar Notes and the context files, and do not resolve it.
2. **Set one goal per email.** One sentence each: what the recipient should do after reading (reply, book, click, refer). In a sequence, each email gets a different goal that moves one step closer to a conversation. If the row asks one email to do two things, split it or drop one, and say so.
3. **Record the consent basis** for each recipient group, using the answer to input 3: express consent (they opted in), implied consent (for example, a recent inquiry or purchase, or a business address published openly where the email relates to their work), a named referral, or a personal or existing relationship. If the basis is unclear, write `[NEEDS CLIENT INPUT: consent basis]` and do not mark the email ready to send. Do not decide legal questions; note what needs checking against current CASL guidance.
4. **Choose the format and length.** Use Specs if given, otherwise these defaults:

   | Type | Default length and shape | Default timing |
   |---|---|---|
   | One-to-one or partner outreach | 90–150 words, plain text, no images | Weekday morning, recipient's time zone |
   | Follow-up | 60–120 words, replies in the same thread | 5–7 days after the first email; at most 2 follow-ups, stop on any reply or unsubscribe |
   | Newsletter | 200–400 words, 1 main story + 1–2 short items | Same day and time each issue |
   | Welcome or nurture sequence | 3–5 emails, 120–250 words each | Day 0, Day 3, Day 7, Day 14 (adjust to the calendar) |

5. **Choose the tone** from the situation table in `voice-and-tone.md` that fits the recipient and phase. Professional partners get a peer-to-peer tone; families and older adults get the warm, reassuring tone. Open with the recipient's situation or interest, not with the client.
6. **Write three subject lines per email** that are true to the body: one plain and direct, one benefit-led, one question or curiosity line. Keep each under 45 characters so it fits on a phone. No all caps, no "RE:" or "FWD:" on a first email, no false urgency. Mark a recommended pick; for one-to-one sends there is no test, so pick one.
7. **Write the preview text** (40–90 characters): it continues the subject line and adds a reason to open. Never leave it to default to "View in browser" or the first line of a footer.
8. **Write the body.** Short paragraphs of one to three sentences. Describe services only as `offer.md` states them and the client's role only as `guardrails.md` allows. For one-to-one emails, leave a clearly marked `[PERSONAL LINE: sender writes one true sentence about this recipient]` slot. Never invent a shared connection, a past conversation or a referral.
9. **Write one CTA** from the calendar row, using the approved CTA wording in `voice-and-tone.md`. One link or one reply request, said once in the body and repeated at most in a P.S. Make it low-effort (reply, a short call, one link). No countdowns, scarcity or pressure.
10. **Write the sign-off and footer.** Sender name, business name and contact details exactly as in `brand-book.md`. For any commercial email, the footer must identify the sender, include a mailing address and one other contact method, and give a working unsubscribe method (a link for tool-sent emails, or "reply 'unsubscribe'" for hand-sent ones). If a detail is missing from the context files, write `[NEEDS CLIENT INPUT: ...]`.
11. **Add merge fields and tracked links.** List every merge field (for example `{{first_name}}`) with a fallback value. Add tracking to every link: `utm_source=email`, `utm_medium=<email type>`, `utm_campaign=<Campaign ID>`, `utm_content=<Asset ID>`. For one-to-one emails, track replies in the client's lead sheet instead.
12. **Write the companion piece** if the calendar row's Format is something sent by email (one-pager, referral card, checklist): its copy in order, section by section, and a short design brief for the design tool in `playbook/tool-register.md`, with colours, fonts and contrast rules from `brand-book.md`. Make sure the email and the attachment say the same thing.
13. **Plan the sequence logic** (sequences and follow-ups only): send order, gaps between emails, what stops the sequence (reply, booking, unsubscribe), and what happens to people who click but don't book.
14. **Write the sources file.** Map every claim, service description, place name, contact detail and CTA to its context file and section. Record the consent basis, link list and any `[NEEDS CLIENT INPUT]` items.
15. **Fill the calendar fields** to update: AI use, AI disclosure, Output link (the asset folder), Status `In review`.
16. **Run the guardrail check** (section 4), fix what fails, then present both files with the review checklist (section 5).

---

## 3. Output template

Save two files:
- `outputs/<client-slug>/<Asset ID>/<Asset ID>-copy-vN.md`
- `outputs/<client-slug>/<Asset ID>/<Asset ID>-sources.md`

Rules in `outputs/README.md` apply: never overwrite; a revision is a new `vN`. Use this exact structure, in this order. Repeat the **Email** block once per email, numbered in send order. If there is no companion piece or sequence logic, write `Not applicable` under that heading.

**Copy file**

```markdown
Station: email
Date: YYYY-MM-DD
Asset ID: 
Context used: [list files]
Status: DRAFT – awaiting review

# Email: [working title]

## Brief
- **Calendar row:** [week · format · channel · audience · campaign ID and phase]
- **Email type and count:** 
- **Recipients and how they joined:** 
- **Consent basis:** [express / implied (reason) / referral (by whom) / personal relationship / NEEDS CLIENT INPUT]
- **Sender and sending method:** [name · by hand or tool from playbook/tool-register.md]
- **Tone used:** [row from voice-and-tone.md]

## Email 1 of [n]
- **Send day:** [e.g. Week 5, Tue morning / Day 0]
- **Goal:** 
- **Subject options:**
  1. [plain] ([n] characters)
  2. [benefit] ([n] characters)
  3. [question] ([n] characters)
  - **Recommended:** [1/2/3] – [reason]
- **Preview text:** [text] ([n] characters)
- **Body:**

  [greeting with merge field]

  [body]

  [CTA]

  [sign-off]

  [P.S., optional]
- **CTA:** [wording · link or reply]
- **Footer:** [sender ID · mailing address · contact · unsubscribe method]
- **Word count:** 

## Merge fields
| Field | Fallback |
|---|---|

## Links
| Link text | URL or Asset ID | Tracking parameters |
|---|---|---|

## Sequence logic
- **Order and gaps:** 
- **Stop when:** 
- **If they click but don't book:** 

## Companion piece
- **Format:** 
- **Copy (section by section):** 
- **Design brief:** [tool · size · colours and fonts from brand-book.md · contrast check]

## Disclosure and open items
- **AI disclosure needed?** [Yes / No, and why] · [exact wording if yes]
- **Assumptions to validate with the client:** 
- **[NEEDS CLIENT INPUT] items:** 

## Calendar update
- **AI use:** 
- **AI disclosure:** 
- **Output link:** outputs/<client-slug>/<Asset ID>/
- **Status:** In review
```

**Sources file**

```markdown
Station: email (sources)
Date: YYYY-MM-DD
Asset ID: 
Status: DRAFT – awaiting review

## Claims
| Email # | Element | Exact wording or claim | Context file and section | Approved for public use? |
|---|---|---|---|---|

## Consent record
| Recipient group | How they joined | Consent basis | Checked by | Date |
|---|---|---|---|---|

## Tools and prompts used
- 

## Open items
- [NEEDS CLIENT INPUT] ...
- (assumption – validate with client) ...
```

---

## 4. Guardrail check

Before showing the output, confirm each item and fix anything that fails:

- [ ] **Consent is recorded.** Every recipient group has a consent basis in the sources file. Emails without one are not marked ready to send.
- [ ] **CASL footer.** Every commercial email identifies the sender, gives a mailing address and one other contact method, and has a working unsubscribe method that is easy to use. Unsubscribes are honoured promptly and the sequence stops for them.
- [ ] **Honest subject lines and preview text.** Each matches the body. No fake "RE:" or "FWD:", no implied prior conversation, no misleading sender name.
- [ ] **No false familiarity.** No invented shared contacts, referrals, past meetings or personal details. Personal lines are left for the sender to write.
- [ ] **No invented facts.** No made-up statistics, results, credentials, testimonials, prices or years in business. Every claim appears in the sources file. Gaps are marked `[NEEDS CLIENT INPUT: ...]`.
- [ ] **Claims match the offer.** Services, role and service area only as `offer.md` and `guardrails.md` confirm. No guaranteed outcomes. Partner emails don't present the client as replacing the partner's own professional services.
- [ ] **No unapproved pricing, discounts or guarantees**, in the email or the companion piece.
- [ ] **No fear, guilt, pressure or false urgency** in the subject, preview, body, P.S. or CTA.
- [ ] **Words and phrases** checked against the say / never-say lists, CTA rules and sign-off in `voice-and-tone.md`.
- [ ] **Privacy.** No real client names, stories, addresses or photos without written permission. Recipient lists and personal details are not pasted into AI tools without authorization.
- [ ] **Accessibility.** Plain language, descriptive link text, no meaning carried only by images, alt text on any image, readable on a phone.
- [ ] **AI disclosure.** Any AI-generated image or representation that could mislead is disclosed. No AI-written quotes presented as real customers.
- [ ] **Follows `context/guardrails.md`.** Client-facing content still needs the client's approval before sending.

---

## 5. Review checklist (human)

- [ ] Would the recipient know within the first two lines why this email is for them?
- [ ] Does each email ask for one thing that is easy to do?
- [ ] Is the subject line honest, and would we open it ourselves?
- [ ] Do we know how every recipient joined, and can they unsubscribe easily?
- [ ] Is every claim true, approved and listed in the sources file?
- [ ] Does it sound like the client writing personally, not like a marketing blast?

When approved: change both status lines to `APPROVED – <date>`, update the calendar row (Status `Done`, Output link), commit with a message like `Add [client] email [Asset ID] (approved)`, and give the send date, links and tracking parameters to whoever sends it. After sending, give replies, clicks, bookings and unsubscribes to performance-report.

---

## 6. Tool slot

**Job:** email writing and sending.
**Current tools:** see `playbook/tool-register.md` → email. Fill in two picks there:
- **Writing tool:** Claude (this skill)
- **Sending tool:** the client's own inbox for one-to-one and partner emails, or an email platform for newsletters and sequences (one with sign-up forms, unsubscribe handling and link tracking)

**Default:** Claude writes the copy, companion piece brief and sources file. A person sends. Open rates are unreliable because some mail apps open emails automatically, so judge results on replies, clicks and bookings. Swapping a sending tool means changing one register row, not this station.
