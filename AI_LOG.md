# AI Log: Handover pretotype

Running record of what AI generated for the pretotype, what we accepted or changed, and why.
Feeds the report's "how we checked and revised AI outputs" section (rubric criterion 2).

**Tool:** Claude (Anthropic), model Claude Opus 5.5, used through Claude Code.
**Pretotype:** `site/index.html`, a single static landing page with a scripted demo (no live AI, no data collected).

---

## v1 (24 Nov 2026): first draft of the website

### What we asked for
A mobile-first landing page for the move-out marketplace that (a) lets departing and arriving
students understand the offer and decide whether they're interested, and (b) matches our digital
trace evidence. That means leading with collection/handover, not just AI listings.

### Human decisions made before generation
| Decision | Choice | Why |
|---|---|---|
| Name | **Handover** | AI suggested 5 names. We chose Handover because it names the pain our data surfaced (collection, 4/10 posts; "where do I go", 9/10). We first picked "Trinity Handover" but **dropped the university name** to avoid implying an affiliation or using TCD's brand without permission. |
| Format | Landing page + scripted demo | Rubric: a pretotype is enough and technical complexity earns nothing. A demo *shows* the AI value rather than just describing it. |
| Call-to-action | Shows a "this is a prototype" message, **collects nothing** | The brief stops before the demand test. Collecting real sign-ups would need ethics approval. |
| Hosting | GitHub Pages (free, personal account) | Shareable link for WhatsApp, Instagram and QR posters, matching our channels. |

### How the evidence shaped the AI-drafted page
| Evidence (midterm Appendix B) | Where it appears on the page |
|---|---|
| No obvious outlet: 9/10 asked where or how | Hero promise ("We'll handle the handover"); "How it works" says "you don't need to know where to sell" |
| Wants collection, storage or drop-off: 4/10 | Step 3 "Hand it over" is highlighted as **"The bit that matters"**; there's a whole Collection days section plus a €5 pickup option |
| Time pressure, fixed departure: 5/10 | "One evening, not three weeks"; FAQ "I'm leaving in three days"; collection dates tied to December flights |
| Price secondary to speed: 5/10 | Pitch leads with speed and ease. Prices are modest and suggested for you, with no haggling |
| Waste avoidance: 2/10 | "Nothing in the skip" panel; unsold items are donated |
| Scam or trust concern: only 1/10 | Trust kept to a light strip and one panel (students-only college email), **not** the headline |
| Arrival demand side: post 7 | "I'm arriving" toggle and starter bundles |
| Meta already has AI listing tools | The AI demo is one section, not the hero. Our differentiator is handover and timing |

### Assumptions the AI introduced (the group must review: these are invented, not evidenced)
- **Seller payout: 80% of the sale price.** This is a revenue-model assumption. It could be tested later.
- **Room pickup fee: €5.**
- **Bundle prices:** Kitchen €25, Bedroom €35, Study €15, plus "about € new" comparisons. The comparison prices are rough estimates, not checked.
- **Collection days:** 12, 15 and 19 Dec at generic Dublin areas, labelled "Example dates".
- **Example listing prices** in the demo and the hero phone mock-up (kettle €8, lamp €10, duvet €15, bike €60).
- **Operations promises:** washed bedding, safety-checked electricals, payouts to Revolut or bank after leaving Ireland, no mattresses or opened food, unsold items to charity shops. None are tested.
- **"4 items listed in 6 minutes"** in the hero mock-up. This is illustrative, not measured.

### Things we checked and changed in v1
- Removed any college name or logo. The footer and top banner say it's a prototype and not affiliated with any college or accommodation provider.
- Residences are generic areas (city centre, Rathmines & Ranelagh, Docklands), not real named buildings.
- Prices and dates are labelled "Example" on the page so viewers aren't misled.
- Checked the layout at phone width (390px) and desktop width (1280px).

---

## v2 (24 Nov 2026): added single-item browsing, demoted bundles

### What we noticed reviewing v1
The AI's v1 leaned too hard on **starter bundles**. On the arriving side, bundles were the only
way to buy. Single items got one passing mention.
- **Inconsistent with our own page:** the seller side showed single listings (kettle €8, lamp €10),
  but buyers couldn't see or buy them. So who buys Helena's kettle?
- **Not what the evidence says:** our only buyer-side post (post 7) asked for "bedroom furniture and
  kitchen items… second-hand sources… a good price". That's browsing for items, not asking for a pack.
  Bundles are marked **(A) assumption** in our Lean Canvas.
- **Undersold the core idea:** the concept is a *move-out marketplace*. Making bundles the only option
  put our least-evidenced feature up front.

### What we changed
- **New "Browse items" section** ("Just need a kettle? Buy one thing") with 8 example single listings.
  Each shows price, condition and collection point/date, and there are working category filters
  (Kitchen, Bedroom, Study, Bikes).
- **Bundles kept but repositioned** as the shortcut: "Or skip the browsing: grab a starter bundle".
  We kept them because they're part of our differentiation (Facebook Marketplace can't do "ready
  at your residence on move-in day") and they carry our main revenue assumption (bundle commission).
- **Arriving hero and step 1** now say "pick single items or grab a ready-made bundle".
- **Seller step 4** now links the two sides: "Your things sell one by one, and anything left over can
  go into a starter bundle". This also explains where bundle stock comes from.

### Why it matters for the demand test (next steps)
With both options on the page, a future test can compare whether arriving students click single items or
bundles. That directly tests the bundle assumption instead of building the offer around it.

### New AI-invented assumptions to review
- Example single-item prices: saucepan set €10, desk chair €20, mirror €12, drying rack €6
  (plus kettle, lamp, duvet and bike as before).

---

## v3 (27 Nov 2026): AI-simulated student walkthrough (prediction, not data)

- **What:** 10 Claude agents (5 Opus 5.5, 5 Sonnet 5.5) role-played students with different
  demographics. Each browsed a local tracking copy of the site (`sim/site-b.html`, never published) at phone
  size, then gave interview-style feedback. Prompt and personas: `sim/PROMPT.md`. Results: `sim/RESULTS.md`.
- **Limiting agreeable bias:** agents were told they're not assistants, most visitors leave without signing up, and
  to leave whenever they'd really leave. They saw only screenshots, not the code, and weren't told we built it.
  Personas included low-need, sceptical and ineligible people.
- **Headline prediction:** 4 of 10 signed up. Both leaver sign-ups were the **€5 pickup** (nobody published a
  listing), which supports collection-first. The biggest blocker (6/10) was "is this for me?": the page reads as
  residences-only and December-only, which our own mission (Dec–Jan **and** May–Sep) doesn't intend.
- **Compared with our evidence:** agrees on collection and on the problem being wider than students; more
  optimistic than our evidence on buyers; raised a platform-trust question ("who runs this?") our trace posts
  couldn't show.
- **Limitations:** not real customers; model and persona confounded; the same AI built and judged the site; a
  setup artifact ("pay on collection" wording only in the test variant) may have driven both buyer reserves.

---

## v4 (27 Nov 2026): revisions from the simulated walkthrough

Four changes, each tied to a finding in `sim/RESULTS.md`. Kept to four so a rerun can show whether they helped.

| Change | Why (simulation finding) |
|---|---|
| **Who it's for, up front:** "Halls, house shares or apartments · December or May" in the hero; May collection days added; residence-only wording replaced throughout; new FAQ "I live in a house share" | 6/10 personas thought it wasn't for them (house shares, May leavers). Our own mission covers May–Sep, the page didn't |
| **Pickup booking made concrete:** asks for address, room, day, time and rough items, with "list everything for me (no photos needed)" ticked by default; confirmation repeats the booking back | Both leaver sign-ups were pickups, and both felt "Done… done what?". Jake would have left if listing came first |
| **Pay on collection everywhere:** reserve form asks where you're staying and when you arrive; "free to reserve, pay by card or Revolut when you collect"; new arrivals FAQ (damaged item or late arrival) | Both buyers asked how items would be matched to them. Removes the pass-1 mismatch (test form said pay on collection, page said deposit) |
| **Trust and hygiene:** "Who we are" section (student team; publish resold/donated/binned numbers each term). Duvets "washed at 60°C and sealed", pillows always new, used pillows not accepted | "Who runs this?" stopped Wei and Aoife. Jonas skipped the Bedroom Starter over "washed" |

**New assumptions introduced (unvalidated):** pay on collection (risk: no-shows), staff photograph and list items at
pickup (a cost not in our model), May collection dates and areas, 60°C washing, new pillows in the €35 bundle,
holding reservations for a week, and publishing reuse numbers.
**Deliberately not changed yet:** students-only (Tomasz, the non-student), a donate-first option (Aoife), moving single
items higher (Siobhán). These are strategy questions for the group.
**Public site:** after the final step, every form shows "prototype, nothing was booked or saved" plus a preview of the
confirmation. No data is sent anywhere.

### Open for the group to review
- [ ] Are the prices, payout share and pickup fee believable to students? Should we change them?
- [ ] Is the tone right for Erasmus and international students?
- [ ] Add a QR code poster version for residence noticeboards?
