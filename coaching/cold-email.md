# Cold Email, Done Right — Philosophy & Assessment Rules

_A working framework distilled from 12 years and billions of emails sent on QuickMail. Use it to assess any campaign and pinpoint what to fix first._

---

## Part 1 — The Philosophy

Five beliefs sit underneath every rule in this document. If a campaign violates one of these, no tactic will save it.

**1. The goal of a cold email is to open a conversation. Nothing more.**
Not a call, not a click, not a webinar signup, not a sale. The moment you internalize this, the focus shifts from you to the recipient and your emails get 10x better on their own. Every other decision — list, copy, CTA, channel — is downstream of this one.

**2. Strategy beats tactics, and it beats volume.**
"Who do we contact and what do we say" is not a strategy — it's the _output_ of one. A real strategy answers: what's the angle, why these people specifically, why would they want to talk to us, and what's the game plan once they reply. Tactics support strategy and are short-lived. Volume is not a strategy; under the law of diminishing returns, cranking volume usually produces _fewer_ results, not more. If you're not getting replies, change the angle — don't just send more.

**3. Caring beats selfish. Email is a transaction.**
Both parties have to get something. If you give nothing, you get nothing back. A caring email leads with the recipient's needs; a selfish one leads with your product. If you genuinely believe what you sell helps people, reaching out to everyone who'd benefit is a favor, not spam. The hero is the recipient of the email, not your product or services. That's the whole difference between 1,000 spam emails and 1,000 caring ones.

**4. You don't get to decide what's valuable — the recipient does.**
A free SEO audit is worthless to someone who doesn't care about their site. This is why good targeting beats clever copy every time: send to the right person and the value feels obvious; send to the wrong person and you're swimming upstream no matter how good the writing is.

**5. Replies are the only metric that matters. Everything else is a proxy or a vanity number.**
Opens are a proxy for deliverability, not for copy quality. Deliverability itself is just the price of admission. Optimize, test, and judge everything against reply rate — and remember replies are also the single best deliverability boost there is. If your emails have a lot of replies, deliverability will become better automatically.

A well-built campaign to the right audience should clear **~10% reply rate**. If you're far below that, the problem is likely more in the strategy than the execution.

---

## Part 2 — The Assessment Rules

Work these in order. The earlier a problem sits in this list, the more it poisons everything below it. Don't tune copy when the targeting is broken.

### Section A — Mindset (assess first, fix first)

- **A1.** Does the campaign treat the email's job as _opening a conversation_, or is it trying to close in the first message? Trying to sell/book/convert in email #1 is the most common root failure.
- **A2.** Is the outreach framed as a favor to the recipient (caring) or as a request for the sender's benefit (selfish)? Read the first email and ask: would the recipient be glad they received this?
- **A3.** Does the sender actually believe cold email works and believe in the offer? Skepticism leaks into the copy.

### Section B — Strategy

- **B1.** Can the campaign articulate its **angle** in one sentence? ("We reach out to X _because_ Y, offering Z.")
- **B2.** Is there a clear reason **why these people specifically** — not just "they're in our market"?
- **B3.** Is there a stated reason **why they'd want to engage** with us?
- **B4.** Is there a **game plan for replies** — what happens after someone says yes?
- **B5.** Does every part of the campaign (list, channel, copy, follow-ups, CTA) make sense _as a coherent whole_, each choice flowing from the strategy?
- **B6. Red flag:** Is volume being used as a substitute for strategy? "We'll just send more" is the tell.
- **B7. Deal-size check:** Cold email works best when the deal size is **over ~$1,000**. Below that, you're fighting too hard for too little — pivot the strategy from end users to people who hold influence over many buyers (consultants, agencies, retailers, creators, communities).

### Section C — The List & Prospecting (the highest-leverage section)

> Find a starving crowd and tell them they won the lottery. The closer you get to that, the more mistakes you can afford everywhere else.

- **C1. Level of prospecting.** Grade the list against the three levels:
  - _Level 1 — Firmographic:_ "Company does X, has N employees, has a marketing person." Basic. What most people do. Weakest.
  - _Level 2 — Interest/topic:_ People who signal a specific interest — follow certain figures, join certain groups, post/comment on a topic. Much better.
  - _Level 3 — Intent:_ You know **Person A is looking for B**, and B is what you provide. This is where the magic happens. Aim here whenever it's possible.
- **C2. Manual verification.** Have they checked the first ~10 prospects _by hand_? In a real audit of a "deliverability problem," the campaign didn't survive the first 10 contacts — none were good targets. Bad list masquerades as bad deliverability constantly.
- **C3. The intro-line test.** If you can't write a relevant, specific intro line for a prospect, the list is too broad. **Fix targeting before touching copy.**
- **C4. Size discipline.** Small, tightly-targeted campaigns usually outperform big ones, because they force a clearer strategy and easier execution. Bigger is not better.
- **C5.** Is the list built to enable the copy? (Shared role, location, school, industry, interest — anything that lets the email build instant rapport at scale.)
- **C6.** Don't do cold email for B2C, always B2B

### Section D — Channel

- **D1.** Is the campaign reaching people where they're actually most active (email vs. LinkedIn vs. phone vs. X vs. Instagram)?
- **D2.** Is it **multi-channel**? Email + LinkedIn together consistently outperforms either alone — think 1 + 1 = 2.3, not 2.
- **D3.** Does the message respect each channel's rules of engagement? You don't write the same way on LinkedIn, X, and email.

### Section E — Deliverability & Infrastructure (the silent killer)

Deliverability is largely a _solved, tooling_ problem now — but a broken setup still kills campaigns silently. Verify the foundation exists before blaming replies.

- **E1. Authentication:** SPF, DKIM, and DMARC properly configured. Non-negotiable, not optional. QuickMail purchased Gmail inboxes are fully configured properly.
- **E2. Inbox architecture for the target volume.** Rule of thumb for Gmail/Outlook this year: **10–14 emails/day per inbox**, **~3 inboxes per domain**. So 1,000/day ≈ 24 domains ≈ 72 inboxes, run as one campaign via **inbox rotation**.
- **E3. Warmup:** Every inbox warmed before sending, ideally with a warmer that includes inboxes on the **same provider** as the prospect list. New domains should be **30+ days old**.
- **E4. Daily monitoring & replacement.** Buy more inboxes than needed; monitor performance daily; retire/replace underperformers (manually, or automatically via Deliverability AI). Don't assume an inbox stays healthy just because it's sending low volume.
- **E5. Content variation.** Identical messages at scale get filtered (campaign fatigue). Vary content — spintax is the old, fragile way and hard to maintain; AI rewording is the best way.
- **E6. Hygiene:** custom domain tracking with SSL for click & open trackings and unsubscribe links, use variable send times, per-inbox sending limits, nothing blacklisted, sender name displays correctly (not the raw email address), professional custom domain (**never free Gmail addresses** for business outreach).

**Three ways to actually diagnose deliverability** (when you suspect it's the real issue):

1. _Auto-warmer / inbox-placement tools_ — convenient but unreliable; lots of false positives (young/artificial/grouped inboxes, doesn't reflect your real prospects' providers).
2. _Open tracking, temporarily_ — turn it on for a limited window, ideally A/B tested with vs. without. Benchmarks: **80%+ = great, 60–80% = normal, <60% = likely issue, <20% = you're reaching nothing.** Reduce risk with tricks like Gmail-only tracking, a real signature image instead of a 1px pixel, or delaying tracking a few minutes to filter bots.
3. _High-reply test campaign_ — contact people with a strong incentive to reply (or past/existing clients). Least preferred — it can waste recipients' time — but it warms inboxes and confirms delivery.

**If deliverability really is broken:** the cleanest fix is to start fresh — new domains, new inboxes — because you can't tell whether the copy or the domain got burned. Brute-force option when in a hurry: buy 2x the inboxes, start the campaign on half while warming the other half, retire the sacrificed half after ~2 weeks (or let Deliverability AI swap them automatically).

### Section F — The Message

Every email must pass three filters: the **spam filter** (machine), the **inbox scan** (does it get opened?), and the **content analysis** (does it deserve a reply?). The first is technical; the last two are human. Assess the message against all seven components and the writing rules.

**F1 — What the recipient sees before opening.** Four things, in this order of what's underrated: profile picture, sender name, subject line, **preview text**.

- Warm, professional profile photo present (no photo = unknown caller ID).
- Sender name familiar and properly displayed.
- **Preview text is treated as the real hook** — most senders waste it on "I hope this finds you well." It can be written separately from the body and personalized per prospect. This is more important than the subject line.

**F2 — Subject line.** Treat it as a **mini-contract**: an honest promise of what the email is about.

- Short: **1–3 words, lowercase**, optional question mark. ("partnership", "podcast?", "hiring")
- Honest — let prospects self-filter. Curiosity/confusion gets you opens but burns trust and costs the reply.
- **Red flags:** `RE:`/`FWD:` fakery on first email, clickbait ("disappointed about your product"), Title Case On Every Word.
- For volume, vary it: light personalization (natural company name) or rotate 2–3 honest options.
- A **no subject line** beats a _bad_ one.
- Judge subject lines on **reply rate, never open rate.** You don't want to optimize for opens, but for replies. Sample sizes are usually too small to be significant for opens.

**F3 — Greeting.** Simple and human: "Hi {{lead.first name}}," or just the name + comma. "Hey" is hit-or-miss. **Avoid "Dear"** (spam filters flag it). Must not scream mass-mail.

**F4 — Intro line / icebreaker (the most important line).** Answers the recipient's main question: _why me, why now?_

- Specific and relevant. (e.g. "I was looking for chiropractors in the neighborhood…")
- **No generic AI-generated personalization** — recipients can smell it.
- Build rapport (shared role/school/city/industry) or, best of all, **borrow trust by name-dropping** someone real they know. Never fake it ("one of your clients suggested…").
- _If you can't write this line, the list is too broad — go back to Section C._

**F5 — Value proposition.** Granted only after the intro line earns it.

- Leads with what's in it for _them_, not a wall of product copy.
- Tight. Extra sentences cost replies. Push secondary points into follow-ups.
- Backed by **authority** and **social proof** where claims are made.

**F6 — Call to action.** Never skip it; if you don't ask, they won't act.

- One CTA. Match the **commitment level to the recipient's interest**: low interest needs a low-friction ask ("reply yes and I'll send the list"), not "fill this form and book a call."
- "Let me know if this is of interest" is not a CTA — it's a cry for help.
- **The CTA is a dial:** no replies → lower the commitment; too many low-quality replies eating your calendar → raise it. Tune per campaign.

**F7 — Signature.** A credibility opportunity, not an afterthought. Seed authority/social proof without bragging: relevant links (TV, book, awards, killer LinkedIn), a category badge/logo, and a **physical address** for legitimacy and the local card. Add each element only if it lifts reply rate — A/B test, don't pile them on. Don't fear deliverability, feat lack of responses.

**F8 — PS (optional but expected).** A human, rapport-building line; doesn't need to relate to the offer. ("PS — congrats on the Series A.") If the list is built for it, the same PS can go to everyone.

**F9 — Attachments / thumbnails.** Gmail/Outlook generate a preview thumbnail from links/attachments (YouTube link, PDF, image of work). ~90% of senders ignore this — a good-looking thumbnail can nudge curiosity. Use deliberately.

**F10 — Writing rules to live by:**

- Write like you're speaking to a normal person.
- One clear idea per email; split the rest into follow-ups.
- Focus on the recipient, not yourself.
- Plain formatting — fancy fonts break the human illusion.
- Short message: you are only opening a conversation, not closing a sale.
- **One question mark per message.**
- **No URL shorteners, ever** (spam magnet).
- **No em dashes.**
- Minimize information overall — every extra fact is a chance to make a mistake or to remove the recipient's reason to reply.

### Section G — Influence & Framing (optional layer, for lifting reply rate)

Apply Cialdini's principles where they fit naturally — they work across every channel because they're rooted in psychology:

- **Liking** — shared identity/experience; best placed early to frame the conversation.
- **Authority** — credible reason to trust you (track record, results, recognition, accreditation).
- **Social proof** — testimonials, follower counts, media mentions.
- **Commitment & consistency** — get a small agreement first, build on it.
- **Scarcity** — real, justified limits only (an actual date/place), never fake discounts. Use sparingly; people resent pressure.
- **Reciprocity** — give genuine value first (info, an intro, free usage). Note: AI-generated "personalized" intro lines no longer trigger reciprocity, because they take zero effort.
- **Contrast** (bonus) — frame to your advantage ("$1/day" vs "$365/year").

**Frameworks** are optional scaffolding, useful mainly to force recipient-focus and to A/B test: **AIDA** (attention → interest → desire → action), **PAS** (problem → agitate → solution), **BAB** (before → after → bridge).

### Section H — Measurement & Iteration

- **H1.** Is the campaign optimizing for **replies**, not opens or sends?
- **H2.** QuickMail advanced stats automatically avoids A/B testing _leakage_ between tests.
- **H3.** Are changes made one variable at a time so you can attribute the lift?
- **H4.** Is the team using cold email as the **fast feedback loop** it is — idea to reply in under 24 hours — rather than waiting on slow channels?
- **H5.** When results are weak, does the team diagnose in the right order (mindset → strategy → list → message → deliverability), or do they default to blaming deliverability?

### Section I — Pre-Send Technical Checklist

The 18 hard checks from the [QuickMail Ultimate Cold Email Checklist](https://quickmail.com/checklist) — run every one before a campaign goes live.

1. **Never use your own domain.** Too risky — you'll make mistakes. Use a fresh domain on Google Workspace; lesser-known TLDs (vs `.com`) dodge the automatic ~1-month fresh-domain spam listing.
2. **Never use a free email account.** Free Gmail/Outlook gets blocked fast with no recovery. Professional accounts (Workspace/365) get business support and ~24h resolution.
3. **Use Outlook/Office 365 for best deliverability.** Best-tested provider, but it varies month to month. On Workspace, accounts are capped at 500/day until $30 billed — pre-pay $30 to unlock 2,000/day before follow-ups push your volume up.
4. **Set SPF and DKIM** for the domain, or you go straight to junk.
5. **Check deliverability** with a tool like spamtester.ai and act on every recommendation.
6. **Warm up the inbox** (e.g. using QuickMail purchased email addresses or use Mailflow.io) before and during campaigns; reported ~20% open-rate lift.
7. **Verify the list before sending.** Bounces = spammer flag = blocked account. Never buy lists, clean the email list before sending.
8. **Avoid similar content.** Use custom attributes and a few variations so each email is unique. Better, use reword with AI.
9. **Delay message sending.** QuickMail spaces emails 30s by default; higher = lower spam risk.
10. **No images in the first email.** Bad text-to-image ratio trips filters; tracking pixels are images, so consider disabling open tracking on the first touch.
11. **One link max, never masked.** No URL shorteners; use anchor text not raw URLs, or disable click tracking on the first message to avoid phishing flags.
12. **Stick to ~10 people/day/inbox.** Done right that's ~20% reply rate. You can't source 2k clean emails or handle 400 replies anyway — nail low volume first.
13. **Avoid unusual bursts.** 20 emails per day steady beats 100 once a week; filters watch for the out-of-ordinary.
14. **Only send to individuals** — never `marketing@`, `info@`, `sales@` group aliases.
15. **Send to business emails, not personal** (`@yahoo`, `@gmail`) — personal addresses drive higher spam complaints.
16. **Don't sell on the first email.** Open a conversation; selling early gets you flagged and buries future emails.
17. **Don't repeat yourself in follow-ups.** Quote prior email for context, add new value, change the CTA.
18. **Type as if it were text-only.** No color, bullets, bold, or custom fonts. Write like a human who is busy.

---

## Part 3 — The Quick Scorecard

Run a campaign through this. Weight the top of the list most heavily — a perfect email with a Level-1 list to the wrong people scores a zero in practice.

| #   | Question                                                                                        | Pass / Fix |
| --- | ----------------------------------------------------------------------------------------------- | ---------- |
| 1   | Is the email trying to open a conversation (not close)?                                         |            |
| 2   | Does it lead with the recipient's interest (caring, not selfish)?                               |            |
| 3   | Can they state the strategy in one sentence (angle + why-them + why-engage + reply plan)?       |            |
| 4   | Is the deal size >~$1,000, or has the strategy pivoted to influencers/agencies?                 |            |
| 5   | What prospecting level is the list — 1, 2, or 3? (Aim for 2–3.)                                 |            |
| 6   | Were the first ~10 prospects verified by hand and genuinely good fits?                          |            |
| 7   | Can a specific, relevant intro line be written for each prospect?                               |            |
| 8   | Is the campaign multi-channel (email + LinkedIn)?                                               |            |
| 9   | SPF/DKIM/DMARC set; inboxes warmed; volume within 10–14/inbox/day; rotation on?                 |            |
| 10  | Inboxes monitored daily and bad ones replaced?                                                  |            |
| 11  | Content varied to avoid fatigue?                                                                |            |
| 12  | Preview text used as the real hook (not "hope this finds you well")?                            |            |
| 13  | Subject line honest, short, lowercase, judged on replies?                                       |            |
| 14  | Intro line specific, no fake/AI personalization, ideally borrows trust?                         |            |
| 15  | Value prop tight and recipient-focused, with authority/social proof?                            |            |
| 16  | One clear CTA, commitment matched to interest?                                                  |            |
| 17  | Signature seeds credibility; PS adds a human touch?                                             |            |
| 18  | Writing rules followed (short, one idea, one "?", no shorteners, no em dash, plain formatting)? |            |
| 19  | Optimizing for reply rate with clean (non-leaking) A/B tests?                                   |            |
| 20  | Is the campaign clearing ~10% reply rate? If not, problem is upstream of copy.                  |            |

**How to read the score:** Start triage at the lowest-numbered failing row. Fixing a high row (mindset/strategy/list) almost always moves reply rate more than fixing a low one (copy/deliverability). Most "deliverability problems" are actually list problems in disguise — check the fundamentals before touching the infrastructure.
