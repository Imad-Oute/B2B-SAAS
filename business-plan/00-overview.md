# Overview — Moroccan B2B Trade Platform

**The short version.** Everything here is expanded in the numbered files. Read this first; open a section when you need the detail behind it.

*Version 0.3 · 13 August 2026 · MAD unless stated · 1 USD ≈ 9.30 MAD*

---

## What we are building

Moroccan B2B directories sell suppliers **visibility**. Nobody gets paid when a deal succeeds, and nobody carries any cost when it fails.

We are building the **referee**: verified supplier identity, structured quote requests, a reputation record built from real transactions, and eventually escrowed payment with dispute resolution.

**Two phases:**

| | What it is | How we earn | When |
|---|---|---|---|
| **Model A** | Verified profiles + RFQ routing. No money passes through us | Supplier subscriptions + verification fees | Months 3–15 |
| **Model B** | Same, plus payment held by a licensed partner, released on delivery | Transaction fee | Months 15–24 |

**Launch focus:** construction materials, one region, SME buyers and suppliers.

**Why this order:** escrow without deal flow is a compliance project with no users. Phase 1 earns the volume, relationships and evidence that Phase 2 needs. → [§3](03-solution-and-product-thesis.md)

---

## The one-line thesis

> Sell the outcome, not the visibility. Own the transaction record — the only asset in this market that compounds and cannot be copied.

A directory's asset decays: listings go stale and competitors scrape them. A transaction record appreciates: every completed deal improves matching and makes the trust signal more credible. → [§1](01-executive-summary.md)

---

## The plan in six lines

1. **Months 1–2** — Validate. 20 supplier + 10 buyer interviews. Register the SARL. Settle escrow with a lawyer. → [§15](15-milestones-and-gates.md)
2. **Months 3–8** — Build and launch Model A. 100 suppliers recruited by hand.
3. **Months 6–12** — Monetise. Subscriptions and verification fees.
4. **Months 9–15** — Prove the loop. Measure quote-to-deal conversion — the number everything hinges on.
5. **Months 12–24** — Add escrow with a licensed partner.
6. **Years 3–5** — Expand vertical by vertical, region by region.

---

## Money

**What we need:** ~MAD 420,000 for months 1–12; ~MAD 1.2M–2.0M for Phase 2.

**Where it likely comes from — the best news in this plan.** Tamwilcom's **Startup Venture Building** launched December 2025 and offers four **non-dilutive** instruments:

| Instrument | Amount |
|---|---|
| Bourse de Vie (founder stipend) | up to **MAD 40,000/month per founder**, 12 months |
| Bourse d'Incubation (grant) | up to **MAD 200,000** |
| Prêt d'Honneur (0% loan) | up to **MAD 500,000** |
| Prêt d'Amorçage (seed loan) | **MAD 500,000–2,000,000** |

The stipend ceiling alone is more than double our entire two-founder living-cost budget. **Phase 0–1 may be coverable without giving up equity or taking bank debt.** Eligibility: digital startup under 8 years old, applied for through a partner operator (Technopark, CEED, Flat6Labs…). → [§13](13-funding-strategy.md)

**Revenue plan (conservative):** ~MAD 60,000 in year 1, ~MAD 620,000 in year 2. Break-even on direct costs at ~50–55 paying suppliers, around month 15–16. → [§12](12-financial-plan.md)

---

## Pricing

| Tier | Monthly | What they get |
|---|---|---|
| Free | 0 | Listing, 3 RFQs/month, no badge |
| Verified | MAD 400 | Badge, unlimited RFQs, response stats |
| Verified+ | MAD 900 | Priority, featured slots, multi-user |

Plus MAD 1,500 one-off verification, MAD 500 annual renewal.

**Every price here is still a hypothesis.** The one real anchor: BTPro sells construction software to Moroccan firms at MAD 499/month, so our range is plausible. The interviews decide it. → [§6](06-business-model-and-pricing.md)

---

## What could kill this

1. **Cold start.** No suppliers means no value to buyers. The first 100 come from phone calls and site visits — roughly 13–17 weeks of one founder's full time. If neither of us will do months of unglamorous field sales, stop here.
2. **Escrow may stay out of reach.** Confirmed regulated; a licensed partner is the only lawful route. If none will work with a company our size, the defensible business is unreachable.
3. **Trust is not a feature.** Moroccan B2B runs on relationships and brokers. We must be obviously better than phoning a cousin — and only for deals the network can't reach.
4. **Competitors already occupy parts of Phase 1.** Procurement.ma routes RFQs free; BTPro publishes live material prices. **Verification being visibly real is our only Phase 1 differentiator.**

→ [§14](14-risk-register.md)

---

## What we learned that changed the plan

The 13 August research pass produced four corrections worth knowing before reading anything else:

- **Escrow is regulated, and stricter than we assumed.** Holding third-party funds without a licence carries 6 months–3 years imprisonment and MAD 100k–5M fines. Worse, **no Moroccan regulation yet governs digital escrow** — experts are lobbying the central bank to create one. Part of the Phase 2 timeline is outside our control. → [§9](09-regulatory-and-legal.md)
- **Tamwilcom is four months old, not an established programme.** We are early to a new instrument, not late to a crowded one. → [§13](13-funding-strategy.md)
- **We missed a whole competitor cluster.** BTPro, MABANI, BTP Business Market — plus Procurement.ma, which we had wrongly filed as tenders-only. → [§5](05-competitive-landscape.md)
- **Hosting in the EU is fine.** Morocco's data regulator has an adequacy list including France, Germany, Ireland and Spain — no extra authorisation needed. The US would need a 2-month approval. → [§8](08-product-and-technology.md)

---

## Decisions waiting on the two of you

Nothing below is a research question. These need a conversation.

| Decision | Why it matters | Where |
|---|---|---|
| **Equity, vesting, and who is CEO** | More likely to determine the outcome than the entire tech plan. Do it in month 1 | [§11](11-team-roles-equity.md) |
| **Launch region** | Pick where you can actually get meetings. Network beats market size | [§4](04-market-analysis.md) |
| **Frontend: Next.js or WordPress hybrid** | Settle it by answering: will either of you personally write the guides content? | [§8](08-product-and-technology.md) |
| **Hosting: managed or self-hosted VPS** | Needs one founder to accept the ops burden. Morocco or EU both fine legally | [§8](08-product-and-technology.md) |
| **Who pays the transaction fee** | A referee paid by one side is not a referee | [§6](06-business-model-and-pricing.md) |
| **Are our dispute rulings binding?** | Binding makes us an arbitrator, with the legal weight that carries | [§9](09-regulatory-and-legal.md) |

---

## How we get customers

Three channels, not two — the third exists to fix a gap that would otherwise kill us.

| | Channel | Who | When | Why |
|---|---|---|---|---|
| **CH1** | Field visits + phone to suppliers | Suppliers | m1–8 | Solve cold start. 100 verified, by hand |
| **CH2** | **Direct outbound to contractors** | **Buyers** | **m6–14** | **The bridge — SEO can't deliver buyers before ~m12, and suppliers churn without leads** |
| **CH3** | SEO and content | Mostly buyers | m9+ | The long-run engine. Where CAC finally drops |

**Two sequencing traps worth avoiding.** First, the Phase A calls are **interviews, not sales** — a supplier being polite about the idea tells you nothing, and Gate 0 needs recourse failures described *unprompted*. Second, you can't onboard anyone before the product exists; what you can do is build a **waiting list** from those interviews, then do concierge onboarding at launch.

**The number that decides everything:** quote-to-deal conversion. Every channel is upstream of it, and a channel delivering volume without deals is making things worse. → [§19](19-acquisition-playbook.md)

---

## The next five things to actually do

1. **Call Technopark or CEED** about Startup Venture Building — can the four instruments stack, do we qualify, when is the next cohort. *Highest-value call available.*
2. **Sign the founder agreement.** Equity, vesting, CEO. Before either of us writes production code.
3. **Book the payments lawyer.** One question above all: can a licensed partner hold and release funds on our instruction without us performing a regulated payment operation?
4. **Start the interviews.** 20 suppliers, 10 buyers. No pitching — ask, record, shut up.
5. **Register the SARL.** Under a week via the CRI single window; MAD 4,500–16,000; no minimum capital.

---

## Gate 0 — do not build until these are true

1. ≥12 of 20 suppliers describe a real problem finding qualified buyers
2. ≥6 of 10 buyers describe a trust or recourse failure, **unprompted**
3. ≥8 suppliers would list on a free verified directory
4. Escrow has a plausible legal route
5. Both founders have signed the founder agreement

**If Gate 0 fails, change the vertical or stop.** → [§15](15-milestones-and-gates.md)

---

## How to read the rest

| # | Section | Open it when you want… |
|---|---|---|
| [01](01-executive-summary.md) | Executive summary | The full argument in two pages |
| [02](02-the-problem.md) | The problem | What buyers and suppliers actually suffer |
| [03](03-solution-and-product-thesis.md) | Solution and thesis | Why two phases, and what we refuse to build |
| [04](04-market-analysis.md) | Market analysis | Sector size, target segments |
| [05](05-competitive-landscape.md) | Competitive landscape | Who else is here — read before any funder meeting |
| [06](06-business-model-and-pricing.md) | Business model | Pricing, unit economics |
| [07](07-go-to-market.md) | Go-to-market | Cold start, supplier acquisition, SEO |
| [08](08-product-and-technology.md) | Product and technology | Stack, data model, build sequence |
| [09](09-regulatory-and-legal.md) | Regulatory and legal | **The escrow law. Read before designing Phase 2** |
| [10](10-operations.md) | Operations | Verification, field capacity, metrics |
| [11](11-team-roles-equity.md) | Team and equity | Roles, hires, the equity conversation |
| [12](12-financial-plan.md) | Financial plan | Costs, projections, break-even |
| [13](13-funding-strategy.md) | Funding strategy | Tamwilcom, FM6I, timeline |
| [14](14-risk-register.md) | Risk register | Everything that could go wrong |
| [15](15-milestones-and-gates.md) | Milestones and gates | The checklists and go/no-go criteria |
| [16](16-exit-thesis.md) | Exit thesis | Who might buy this and what they'd want |
| [17](17-open-questions.md) | Open questions | The research backlog |
| [18](18-appendices.md) | Appendices | **Interview guides — use these verbatim** |
| [19](19-acquisition-playbook.md) | Acquisition playbook | **Scripts, lists, targets — the daily working document** |

---

**A note on the markers you'll see.** `[VERIFIED — A]` means confirmed from a primary source (statute, regulator, or the institution itself). `[VERIFIED — B]` means two independent sources agree. `[ASSUMPTION — verify]` means exactly that — a task, not a fact. **The blanks in §4's market sizing are deliberate:** the underlying data isn't published, and inventing a number would be worse than admitting the gap.

*Canonical single-file version: [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md). All research findings with sources and confidence ratings: [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
