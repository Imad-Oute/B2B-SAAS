# Business Plan — Moroccan B2B Trade Platform

**Working name:** TBD (see §14.1)
**Document type:** Internal co-founder operating plan — not a pitch deck, not a funding application
**Version:** 0.3 — 13 August 2026
**Authors:** [Founder A] and [Founder B]
**Status:** Draft for joint review. Sections marked ❓ require a decision from both founders before this document is treated as agreed.
**Changes in 0.2:** Desk research pass on regulatory, funding, market sizing and competitive landscape. See `RESEARCH-LOG.md` for every finding with source and confidence rating. Verified facts are marked **`[VERIFIED — A/B]`** inline; everything else remains an assumption.

---

## How to read this document

This is an honest internal plan, not a sales document. It is written to be argued with. Three conventions:

- **`[ASSUMPTION — verify]`** marks a number or claim that is directionally reasonable but not yet confirmed by primary research. There are a lot of them, deliberately. Every one is a task, not a fact.
- **`[VERIFIED — A]`** marks a fact confirmed from a primary source (statute, regulator, or the institution's own publication). **`[VERIFIED — B]`** marks agreement between two or more independent secondary sources. Both are quotable; the source is in `RESEARCH-LOG.md`.
- **❓ DECISION** marks a fork where the two of you must agree before work proceeds. Building past an unresolved ❓ is how co-founder disputes get expensive.
- **Numbers in MAD** unless stated. USD conversions use **1 USD ≈ 9.30 MAD** `[VERIFIED — B, 13 Aug 2026]`. Prefer MAD; the rate moves and a stale conversion undermines confidence in everything around it.

**A note on what desk research can and cannot settle.** The 0.2 pass resolved the regulatory, funding, and competitive questions because those have published answers. It could not resolve pricing, unit economics, conversion rates, verification costs, or whether buyers actually experience recourse failure — those have no published answer and are resolved only by the Phase A interviews in §7.1. Where research would have produced a plausible-looking proxy instead of a fact, the blank was left deliberately. **A blank marked as an assumption is a task; a borrowed number is a fact you stop questioning.**

The plan assumes the framing settled in the pre-meeting brief: **launch as Model A (verified discovery + RFQ routing), graduate to Model B (escrow and referee) on explicit triggers.** It assumes **construction materials** as the launch vertical. Both assumptions are revisable, and §3 and §5.4 tell you what evidence would change them.

---

## Table of contents

1. [Executive summary](#1-executive-summary)
2. [The problem](#2-the-problem)
3. [The solution and product thesis](#3-the-solution-and-product-thesis)
4. [Market analysis](#4-market-analysis)
5. [Competitive landscape](#5-competitive-landscape)
6. [Business model and pricing](#6-business-model-and-pricing)
7. [Go-to-market strategy](#7-go-to-market-strategy)
8. [Product and technology plan](#8-product-and-technology-plan)
9. [Regulatory and legal](#9-regulatory-and-legal)
10. [Operations](#10-operations)
11. [Team, roles, and equity](#11-team-roles-and-equity)
12. [Financial plan](#12-financial-plan)
13. [Funding strategy](#13-funding-strategy)
14. [Risk register](#14-risk-register)
15. [Milestones and decision gates](#15-milestones-and-decision-gates)
16. [Exit thesis](#16-exit-thesis)
17. [Open questions and research backlog](#17-open-questions-and-research-backlog)
18. [Appendices](#18-appendices)

---

## 1. Executive summary

### 1.1 The one-paragraph version

Morocco's B2B supplier directories monetize a seller's *hope of being found* — premium placement, contact-file exports, visibility boosts. Nobody is paid for a transaction succeeding, and nobody carries any consequence when it fails. We are building the referee layer: verified supplier identity, structured RFQ routing, a portable reputation record built from real transactions, and eventually escrowed payment with dispute resolution. We launch in construction materials, in one region, as a verified-discovery and quote-routing product monetized by supplier subscription and verification fees. Once we have demonstrable deal flow, we add escrow — the regulated, defensible, acquirable version of the business.

### 1.2 Why this is a business and not a directory

The distinction that governs everything downstream:

| | Incumbent directories | This platform |
|---|---|---|
| **Paid for** | Visibility | Outcomes |
| **Payer** | Seller only | Seller, and eventually both sides |
| **Data owned** | Listings (copyable) | Transaction history (not copyable) |
| **Liability** | None | Real, and that is the point |
| **Moat** | SEO tenure | Compounding transaction record |
| **Buyer's reason to return** | None | Recourse |

A directory's asset depreciates — listings go stale, competitors scrape them. A transaction record appreciates — every completed deal makes the next match better and the reputation signal more trustworthy. That asymmetry is the whole thesis.

### 1.3 The plan in six lines

1. **Months 1–2:** Validate by phone and in person. 20 supplier interviews, 10 buyer interviews, in construction materials, in one region. Register the SARL. Settle the escrow question with a lawyer.
2. **Months 3–8:** Build and launch Model A — verified profiles, faceted search, programmatic SEO pages, RFQ flow, admin tooling. 100 verified suppliers acquired by hand.
3. **Months 6–12:** Monetize. Supplier subscriptions and verification fees. Target break-even on direct costs.
4. **Months 9–15:** Prove the loop. Instrument quote-to-deal conversion. This number is the trigger for Phase 2.
5. **Months 12–24:** Add escrow with a licensed payment partner. Regulated, slow, and the reason the company is worth acquiring.
6. **Years 3–5:** Expand vertical-by-vertical and region-by-region. Position for a strategic acquirer.

### 1.4 What we need

`[ASSUMPTION — verify: all figures in this subsection depend on §12, which is itself assumption-heavy]`

- **Phase 0–1 (months 1–12):** ~MAD 420,000 (~$45,200) total, of which ~MAD 180,000 is founder living costs and the rest is direct spend. Target source: Tamwilcom Startup Venture Building, plus founder contribution.
- **Phase 2 (months 12–24):** ~MAD 1.2M–2.0M, primarily legal, licensing, payment-partner integration, and a third hire. Target source: Tamwilcom loan facility and/or a Fonds Startups manager under the Mohammed VI Investment Fund.

**Revised view after the 0.2 research pass:** the Phase 0–1 figure may be substantially over-stated as a *funding need*. Tamwilcom's Startup Venture Building — launched December 2025, four months old — offers four **non-dilutive** instruments `[VERIFIED — A]`: a *Bourse de Vie* worth up to 70% of prior salary capped at **MAD 40,000/month per founder for 12 months**, a *Bourse d'Incubation* of up to **MAD 200,000**, an interest-free *Prêt d'Honneur* up to **MAD 500,000**, and a *Prêt d'Amorçage* of **MAD 500,000–2,000,000**.

The Bourse de Vie ceiling alone is more than twice the entire two-founder living-cost line in §12.1. **Phase 0–1 may be almost entirely coverable without equity or bank debt.** What we do not yet know is whether the instruments stack, and what the Bourse de Vie requires by way of salary history — both are questions for the operator, not for further research. See §13.2.

### 1.5 The three things most likely to kill this

Stated up front because a plan that buries its risks is a brochure.

1. **Cold start.** A marketplace with no suppliers is worthless to buyers. Our first 100 suppliers come from phone calls and site visits, not from the product. If neither founder is willing to do months of unglamorous field sales, stop here.
2. **Escrow is legally out of reach without a licensed partner — confirmed, and the framework for it does not yet exist.** `[VERIFIED — A/B]` Holding third-party funds is a regulated payment service under Articles 15–16 of Law 103-12; performing it without a licence carries 6 months to 3 years imprisonment and a fine of MAD 100,000–5,000,000 (Art. 183). Worse for the schedule: Moroccan experts state publicly that **no specific text governs digital transactional escrow**, and are lobbying Bank Al-Maghrib to issue a circular that would authorise payment institutions to act as escrow agents. So Phase 2 depends partly on regulation that has not been written. A licensed partner operating under existing Article 17 cantonment rules is the only near-term route. If no partner will work with us at our size, the defensible version of the business is unreachable and we are building a better Kerix. That is a real business, but it is a different one with a much lower ceiling. See §9.3.
3. **Trust is not a feature.** Moroccan B2B trade runs on personal relationships, brokers, and long-standing credit arrangements. A platform that asks two parties to trust software instead of each other is fighting a cultural default, not just a competitor. Our verification and recourse story has to be *obviously* better than a phone call to a cousin.

---

## 2. The problem

### 2.1 Three parties, three unaddressed problems

**The buyer** (a contractor, a project manager, a procurement officer at an SME) needs to source materials from a supplier they have not worked with before. Today they:

- Ask their network first, which limits them to known suppliers and known prices
- Search directories that list everyone and vouch for no one
- Have no way to distinguish a legitimate operator from a shell company with a good listing
- Have no recourse when goods arrive late, short, or wrong — the dispute is a phone argument, then a lawyer, then nothing
- Cannot compare prices without individually calling every supplier and negotiating from zero information

**The supplier** (a materials distributor, a small manufacturer, an importer) needs to find buyers beyond their existing relationships. Today they:

- Pay directories for visibility, with no attribution of whether a paid listing ever produced a deal
- Receive unqualified enquiries — tyre-kickers, competitors pricing them, buyers with no budget
- Extend informal credit and absorb the default risk themselves
- Have no way to convert a good delivery record into a competitive advantage, because reputation is not portable

**The market as a whole** has no shared source of truth about who is real, who delivers, and what things cost.

### 2.2 The cost of the status quo

`[ASSUMPTION — verify: this entire subsection needs primary evidence from the interviews in §7.2. Do not quote these figures to anyone until verified.]`

We hypothesise, and must confirm, that:

- A mid-size contractor loses meaningful margin per project to price opacity — paying above market because comparison is expensive `[ASSUMPTION — quantify in buyer interviews]`
- Supplier default and delivery disputes are common enough that buyers systematically prefer known suppliers even at a price premium `[ASSUMPTION — this is the core hypothesis; if false, the referee model has no buyer-side pull]`
- Suppliers spend meaningful time on unqualified enquiries `[ASSUMPTION — quantify in supplier interviews]`

**If the buyer interviews do not surface "I got burned and had no recourse" unprompted and repeatedly, the referee thesis is weak and this plan needs rewriting, not adjusting.**

### 2.3 Why now

Four things that were not simultaneously true five years ago `[ASSUMPTION — verify each]`:

1. **Digital payment rails matured.** Morocco's payment infrastructure and PSP ecosystem can now support programmatic disbursement in a way that was impractical before.
2. **Government funding is aimed precisely at this stage.** Tamwilcom and Digital Morocco 2030 instruments are deploying at ideation and prototype stage (§13).
3. **B2B search behaviour moved online.** Buyers under 45 search before they call. Incumbent traffic proves the demand.
4. **The incumbents have not modernised.** Their product and monetization are functionally unchanged. A decade of accumulated SEO tenure is their entire defence.

---

## 3. The solution and product thesis

### 3.1 Core thesis

> Sell the outcome, not the visibility. Own the transaction record, because it is the only asset in this market that compounds and cannot be scraped.

### 3.2 The two-phase product

**Phase 1 — Verified discovery and RFQ routing (Model A)**

The buyer describes what they need once. We route it to verified suppliers who actually serve that category and region. Quotes come back into a structured comparison. The buyer sees, next to each supplier: verification status, response time, quote-acceptance history, and completed-deal count.

Revenue: supplier subscription and verification fees. No money changes hands through us.

**Phase 2 — Escrow and referee (Model B)**

Same loop, plus: the buyer's payment is held by a licensed partner, released on confirmed delivery. Disputes go to a defined resolution process with published rules. Both sides' behaviour is recorded permanently.

Revenue: transaction fee, on top of Phase 1 lines.

### 3.3 Why the sequencing is this way and not the reverse

Escrow without deal flow is a compliance project with no users. Deal flow without escrow is a business, just a less defensible one. Phase 1 generates the three things Phase 2 requires: transaction volume to justify the licensing cost, supplier relationships to onboard onto a new payment flow, and evidence of demand for a funder or partner.

The risk of this sequencing is that we get comfortable in Phase 1 and never do the hard regulated work. §15 sets explicit triggers to prevent that.

### 3.4 The compounding-data argument

Each completed transaction produces data no competitor can publish:

- **Verification records** — this company is real, here is the evidence
- **Response behaviour** — who answers, how fast, how often
- **Quote data** — what things actually cost, by category, region, and volume
- **Fulfilment records** — who delivers as promised
- **Dispute outcomes** — who behaves badly under pressure

That data feeds directly back into two engines: better matching (a product advantage) and programmatic content (a growth advantage — see §7.3). Kerix can publish listings; it has no transaction data and no way to start accumulating it without rebuilding its product.

**Corrected in 0.2 — this claim was previously over-stated.** The original draft said no competitor could publish price data. **BTPro (`btpro.ma`) already publishes live cement, steel, sand and concrete prices by Moroccan city, with variation alerts and history** `[VERIFIED — A]`. The defensible claim is narrower and still worth making: their price data's provenance is unknown and probably surveyed, scraped, or supplier-declared, whereas ours would be *derived from real quotes on real RFQs* — which is what makes "average lead time for cement in Casablanca, from 340 real quotes" a statement only we can make. **Do not claim competitors cannot publish price pages. One does.** See §5.1.

### 3.5 What we are explicitly not building

Scope discipline is the difference between shipping in eight months and shipping in twenty. Not in Phase 1:

- Logistics, delivery, or fulfilment
- Inventory or stock management for suppliers
- Financing, factoring, or credit provision — a genuinely attractive adjacent business, and a completely different regulatory problem
- A mobile app (responsive web only; revisit at Phase 2) ❓
- Multi-vertical anything
- Buyer-side procurement SaaS (a possible Phase 3 revenue line, §6.5)

---

## 4. Market analysis

### 4.1 Sizing — and why these numbers are soft

Honest statement: we do not yet have defensible market-size figures, and a plan that invents them is worse than one that admits the gap. What follows is a *method* with placeholder inputs, to be filled from primary and desk research (§17).

**Top-down**

| Input | Value | Source status |
|---|---|---|
| Morocco GDP at current prices (2025) | **MAD 1,720.2 bn** | `[VERIFIED — A]` HCP |
| BTP sector value added (2025) | **~MAD 100 bn**, ~6% of GDP | `[VERIFIED — A]` HCP / FNBTP |
| BTP sector growth | **~6% (2025), 4.1% forecast (2026)** | `[VERIFIED — A]` HCP BEP 2026 |
| BTP employment | **1.2 million+** | `[VERIFIED — B]` FNBTP |
| Share that is materials procurement | ___% | **NOT PUBLISHED — see note** |
| Share transacted B2B between SMEs (our reachable segment) | ___% | **NOT PUBLISHED — see note** |
| **Serviceable market (transaction value)** | MAD ___ | Cannot be derived — see note |
| Our realistic take rate at maturity | 0.5–1.5% | §6 |
| **Revenue ceiling at 5% market penetration** | MAD ___ | Cannot be derived — see note |

**Why the last three rows are still blank, and should stay blank.** Value added is not materials spend. Value added *excludes* intermediate consumption, which is exactly where construction materials sit — so materials procurement cannot be derived from the ~MAD 100bn figure by any honest arithmetic. Neither the materials share nor the SME-B2B share is published anywhere we could find.

Filling these with plausible percentages would produce a TAM that looks authoritative and means nothing. **In front of a funder, "sector value added is MAD ~100bn per HCP; materials procurement share is not published, so we plan bottom-up" is a stronger answer than a confident derived number that collapses under one question.** If we want the top-down figure properly, HCP publishes input-output tables (*tableaux entrées-sorties*) in the full national accounts that would give materials' intermediate consumption in construction — a manual retrieval task, not a research blocker.

**Bottom-up (the one we should actually plan against)**

| Input | Value | Basis |
|---|---|---|
| Construction-materials suppliers in target region | ~___ | `[ASSUMPTION — count from Kerix, Telecontact, and the trade association]` |
| Realistically reachable in 24 months | 400–600 | Field capacity, §10.2 |
| Of those, convertible to paid | 25–35% | `[ASSUMPTION — no basis yet; test in Phase 1]` |
| Paying suppliers at month 24 | 100–200 | Derived |
| Blended ARPA per month | MAD 400–900 | §6.2 |
| **Monthly revenue at month 24** | MAD 40,000–180,000 | Derived |

The bottom-up number is the one that constrains hiring and burn. The top-down number is for the funding narrative, and should not be believed by us.

### 4.2 Target segment definition

**Launch vertical:** Construction materials — cement, steel, aggregates, timber, tiling, plumbing and electrical supply, finishing materials.

**Why this vertical** (revisit against the rubric in §5.4):

- Large, fragmented supplier base — no single dominant player controls distribution
- High individual deal values, so a percentage take rate is meaningful
- Chronic and well-known trust problems: quality variance, short deliveries, payment disputes
- Buyers are repeat purchasers with predictable, seasonal needs
- Both founders can plausibly reach fifty suppliers in person `[ASSUMPTION — verify this is actually true for at least one of you before committing]`

**Launch region:** ❓ **DECISION.** Casablanca–Settat is the largest concentration of both supply and demand and the obvious default; Tanger–Tétouan or Rabat–Salé–Kénitra are alternatives if either founder has stronger local networks there. Network beats market size at this stage. Pick where you can get meetings.

**Initial buyer profile:** SME contractors and construction firms, roughly 5–50 employees. Large enough to have real procurement volume, small enough to lack a formal procurement department and existing supplier framework agreements.

**Initial supplier profile:** Distributors and small manufacturers, roughly 3–50 employees, already selling B2B, with at least one person who answers a phone during business hours.

### 4.3 Customer segments and their jobs

| Segment | Primary job | What they will pay for | What they will not pay for |
|---|---|---|---|
| SME contractor (buyer) | Source reliably at a fair price | Recourse; time saved | A directory subscription |
| Procurement officer at a mid-size firm | Defensible sourcing decisions | Audit trail; comparison data | Anything requiring IT approval |
| Materials distributor (supplier) | Fill order book beyond known network | Qualified leads; credible trust badge | Visibility with no attribution |
| Small manufacturer (supplier) | Reach beyond own region | Regional expansion; verified status | Complex software |

### 4.4 Market trends

- **Public-sector infrastructure investment sustaining construction demand** `[VERIFIED — A]`. HCP attributes 2025's ~6% BTP growth to "l'accélération des projets d'infrastructures stratégiques," with CAN 2025, the 2030 World Cup, and the direct housing-aid programme named across sources. BTP represents **55% of gross fixed capital formation** (FNBTP, 2021).
- **Rising input-cost volatility, increasing the value of price transparency** `[VERIFIED — A]`. HCP's *Budget Économique Prévisionnel 2026* states the sector grew "**malgré les coûts élevés des matériaux de construction** et la persistance de la pénurie de main-d'œuvre qualifiée." **The national statistics agency naming high materials costs as a sector headwind is the single best citation we have for the price-transparency thesis.** Use it.
- Formalisation pressure on SMEs (invoicing, tax digitalisation) making verified identity more valuable `[ASSUMPTION — needs a citation before external use]`
- Generational handover in family businesses, bringing more digital-first decision-makers `[ASSUMPTION — needs a citation before external use]`

---

## 5. Competitive landscape

### 5.1 Direct and adjacent players

**Rebuilt in 0.2. The original table listed six players and missed an entire cluster of construction-specific and B2B platforms, two of which overlap directly with our Phase 1 thesis. This was the most consequential gap found in the research pass.**

**General directories**

| Player | What it is | Monetization | Their strength | Their structural weakness |
|---|---|---|---|---|
| **Kerix** | Moroccan company directory | Premium placement, contact-file export | SEO tenure; **~30,000 companies** `[VERIFIED — C]`; claims 500k+ monthly visitors across its network | Sells visibility; no transaction involvement; stale data. **~5× smaller than the 150k this plan previously assumed** |
| **Telecontact** | Moroccan Yellow Pages | Free basic listings, paid boosts, analytics | Brand recognition, broad coverage | Consumer-oriented; shallow B2B depth `[ASSUMPTION — not yet researched]` |
| **Maroc Business** | Business info aggregator | Advertising `[verify]` | — | Thin product `[ASSUMPTION — not yet researched]` |

**Construction-specific — none of these were in v0.1**

| Player | What it is | Monetization | Overlap with us |
|---|---|---|---|
| **BTPro** (`btpro.ma`) | Construction project-management SaaS for Moroccan professionals. **Publishes live cement/steel/sand/concrete prices by city** with variation alerts and history. Moroccan-compliant invoicing (ICE, 20% VAT). Order tracking quote→delivery. | Free tier (1 project, 5 orders/mo); **Pro MAD 499/mo**; Enterprise custom `[VERIFIED — A]` | **HIGH.** Ships the `/prix/` feature §7.3 called unreplicable. Buyer-side, so possibly a partner rather than a rival — see §5.3 |
| **MABANI** (`mabani.ma`) | Materials directory (*matériauthèque*) for architects and prescribers. 1,600+ products, 60 categories | Sells **brand visibility** to manufacturers | Medium. The incumbent model, but construction-specific and aimed at prescribers rather than contractors |
| **BTP Business Market** | Integrated buying group (*centrale d'achat*) with **its own factories**. Sells at "factory prices" via order pooling. Claims 100+ sites supplied, ~20% cost reduction | Margin on goods sold | Medium. Competes for the same buyer with a fundamentally different model — they take inventory risk, we do not |
| **Batimis** | Free platform to buy/sell/rent BTP **equipment** | Unclear | Low — equipment, not materials |

**B2B routing and marketplaces**

| Player | What it is | Monetization | Overlap with us |
|---|---|---|---|
| **Procurement.ma** | **Reclassified — v0.1 had this wrong.** Not tender aggregation. Self-describes as "N°1 de la mise en relation B2B au Maroc." Buyer posts a purchase request free, **AI notifies relevant suppliers**, parties conclude "**sans intermédiaire ni commission**." Directory spans ~21 pages; BTP & Construction is a listed sector `[VERIFIED — B]` | Not visible | **HIGH. This is RFQ routing — our core Phase 1 loop — live in Morocco and free.** Their explicit no-intermediary stance is the opposite of our thesis, which is precisely the opening |
| **Business Hub** (`businesshub.ma`) | "L'infrastructure B2B Marocaine" — claims verified opportunities | Unknown | Unknown — site blocked automated access, **check manually** |
| **Evollume / Solidaire Market / B2B Maroc / b2bconnect** | General B2B marketplaces | Various | Low–medium `[ASSUMPTION — not individually researched]` |

**The actual incumbents**

| Player | What it is | Monetization | Their strength | Their structural weakness |
|---|---|---|---|---|
| **WhatsApp / phone / brokers** | The real competitor — see §5.2 | Broker commission | Trust, ubiquity, zero friction | Not scalable; no record; no price discovery |
| **Alibaba / global marketplaces** | Cross-border B2B | Transaction fees, subscriptions | Escrow exists and is proven | Import-oriented; wrong for domestic trade; no local recourse |

**What none of them do — and this is still the gap:** verified identity *plus* a transaction record *plus* recourse. Procurement.ma routes and steps away. BTPro manages the buyer's own projects. MABANI sells visibility. Nobody carries consequence when a deal fails. **But "nobody has tried this" is no longer a defensible sentence, and §17's blocking question 1 is now partly answered: adjacent attempts exist and are live.**

`[ASSUMPTION — a live homepage is not a live business.]` We do not know these platforms' scale, funding, or whether any have quietly failed. **This is answered in Phase A for the price of one interview question — see Appendix B.**

### 5.2 The competitor that matters

**It is not Kerix. It is the phone.** Most Moroccan B2B materials trade happens through personal networks and brokers who arrange deals on trust and take a cut. That system works, is deeply embedded, and offers something we currently cannot: a human who is personally accountable and known to both parties.

Our answer has to be that we are better precisely where the network fails: when the buyer needs a supplier *outside* their network, when they want price comparison, and when they want recourse that does not depend on a shared relative. We do not displace the network. We serve the transactions the network cannot reach.

**This reframing should change how we pitch to suppliers.** Not "replace your relationships" but "fill your order book in the weeks your relationships don't."

### 5.3 Why we can win, and honestly why we might not

**Structural advantages**
- **Against the directories** (Kerix, Telecontact, MABANI): their revenue depends on sellers paying for visibility; adding transaction guarantees would cannibalise it. Classic innovator's dilemma, and it still holds.
- They have no transaction data and no way to start accumulating it without rebuilding their product.
- Our programmatic-content engine is fed by quote-derived data — see the corrected claim in §3.4.

**The innovator's-dilemma argument does not apply to the new entrants, and 0.2 makes that explicit.** BTPro sells SaaS subscriptions and has no visibility revenue to protect. Procurement.ma routes RFQs for free and has no visible revenue model at all. **Neither is structurally prevented from adding verification and transaction records.** The dilemma argument was written against directories and should not be stretched to cover platforms it does not fit — that is the kind of reasoning that survives a co-founder review and then fails in a funder meeting.

What actually separates us from them is narrower and worth stating precisely: BTPro is buyer-side project management; Procurement.ma is disintermediated matchmaking that explicitly declines to sit in the transaction. **We are the only model proposing to carry consequence.** That is a positioning advantage, not a structural moat — the structural moat is Phase 2 (§16.3).

**Honest disadvantages**
- Kerix has a decade of domain authority and backlinks. We have none. (Though at ~30,000 companies rather than 150,000, it is a smaller incumbent than we assumed.)
- They have existing sales relationships with thousands of suppliers.
- They have revenue. We have savings.
- **BTPro already ships a price-benchmark feature we had assumed was ours to build first.**
- **Procurement.ma already routes RFQs, free, with AI supplier matching.** Our Phase 1 is not a novel product in this market — it is a better-executed, verified, accountable version of something buyers can already do for nothing. **That raises the bar on verification being visibly real (§7.2), because it is our only Phase 1 differentiator.**
- If we prove the model, a well-capitalised incumbent or a bank could copy the Phase 1 product in a quarter. **Our only durable protection is reaching Phase 2 before they bother** — the licensing and trust burden is the real barrier, not the code. §9.3 now shows that barrier is higher than we thought, which cuts both ways: harder for us, harder for them.

### 5.4 Vertical-selection rubric (if construction is wrong)

Score any candidate vertical 1–5 on each; construction materials is the working assumption but this is how to argue for a different one:

| Criterion | Weight | Why it matters |
|---|---|---|
| Supplier fragmentation | High | Concentrated supply means a few players can refuse to participate and kill it |
| Average deal value | High | Determines whether a take rate is worth anything |
| Frequency of trust failure | High | This is the wedge; low-dispute verticals don't need a referee |
| Repeat purchase rate | Medium | Drives retention and LTV |
| Founder network access | **Highest** | Cold start is won by relationships, not analysis |
| Existing digital behaviour | Medium | Determines acquisition cost |
| Regulatory simplicity | Medium | Food, pharma, chemicals add compliance load |

---

## 6. Business model and pricing

### 6.1 Revenue lines by phase

| # | Line | Phase | Payer | Basis |
|---|---|---|---|---|
| R1 | Supplier subscription | 1 | Supplier | Monthly/annual tiers |
| R2 | Verification fee | 1 | Supplier | One-time + annual renewal |
| R3 | Featured placement | 1 | Supplier | Monthly, capped inventory |
| R4 | Transaction fee | 2 | Split or supplier | % of escrowed deal value |
| R5 | Buyer procurement tools | 3 | Buyer | SaaS seat |
| R6 | Data and benchmarking | 3 | Either | Report or API subscription |

### 6.2 Phase 1 pricing

`[ASSUMPTION — every price here is a hypothesis to be tested in the supplier interviews. Ask what they pay Kerix today and what a qualified lead is worth to them.]`

| Tier | Monthly (MAD) | Annual (MAD) | Includes |
|---|---|---|---|
| **Free** | 0 | 0 | Basic listing, receive up to 3 RFQs/month, no verified badge |
| **Verified** | 400 | 4,000 | Verification badge, unlimited RFQs, response-rate display, basic analytics |
| **Verified+** | 900 | 9,000 | Above, plus category priority, featured slots, quote templates, multi-user |

**Verification fee:** MAD 1,500 one-time, MAD 500 annual renewal. Covers our actual cost of checking documents and, where practical, visiting the site.

**Design principles behind this:**
- Free tier exists to solve cold start, not to convert. Suppliers must be listable without a sales call.
- The RFQ cap on free is the conversion mechanism. Suppliers upgrade when leads arrive, not when we ask.
- Verification is priced as a real service with real cost, not as a badge. That is what makes it credible.
- Annual is ~17% discounted to pull cash forward — meaningful when we are funding operations from revenue.

**A real market anchor, new in 0.2** `[VERIFIED — A]`**.** BTPro sells construction project-management software to Moroccan professionals at **MAD 499/month** for its Pro tier, with a free tier capped by usage (1 project, 5 orders/month) converting to paid. Two things follow:

1. **Our MAD 400 Verified tier is not an invented price.** There is a live Moroccan construction-tech product within 25% of it. Moroccan construction firms demonstrably pay ~MAD 500/month for software.
2. **The free-tier-with-usage-caps mechanic is not novel** — BTPro uses the same conversion design. Fine; it works. But do not present it as innovative.

This is *supportive* evidence, not proof. BTPro sells to buyers; we are pricing to suppliers, whose willingness to pay is a different question entirely. **The interview question in Appendix B — "what would a genuinely qualified enquiry be worth to you, in dirhams?" — remains the only thing that actually validates this table.**

### 6.3 Phase 2 transaction pricing

`[ASSUMPTION — depends entirely on the payment-partner cost structure discovered in §9]`

- **Take rate:** 1.0–1.5% of transaction value, floor MAD 200, cap MAD 5,000 per transaction
- **Who pays:** ❓ **DECISION.** Supplier-paid is easier to sell (they are used to paying for leads) but distorts neutrality — a referee paid by one side is not a referee. Split (0.5% each) is more honest and harder to sell. **Recommendation: supplier-paid at launch for adoption, with a stated intent to move to split as buyer-side value grows. Document the neutrality risk explicitly and put dispute resolution under published rules that we cannot quietly bend.**
- **Cap rationale:** without a cap, large deals move off-platform and we get selected against on exactly the transactions we most want.

### 6.4 Unit economics

`[ASSUMPTION — no real data behind these; recompute after 20 supplier acquisitions]`

**Supplier (Verified tier, Phase 1)**

| Metric | Value | Note |
|---|---|---|
| ARPA/month | MAD 400 | |
| Gross margin | ~85% | Hosting, verification amortised |
| CAC (field sales, months 1–12) | MAD 800–1,500 | Founder time at opportunity cost |
| CAC (SEO/inbound, month 12+) | MAD 200–400 | The reason SEO matters |
| Expected lifetime | 18–30 months | `[ASSUMPTION — pure guess; measure it]` |
| LTV | MAD 6,100–10,200 | |
| **LTV:CAC (field)** | **4:1 – 12:1** | Healthy *if* retention holds |
| Payback period | 2–4 months | |

The dominant sensitivity is retention. If suppliers churn at 6 months because leads do not convert, LTV:CAC collapses below 2:1 and the model does not work. **Quote-to-deal conversion is therefore the single most important metric in the business** (§15.3).

### 6.5 Why not the obvious alternatives

- **Buyer subscription:** Buyers will not pay to search. Every marketplace learns this expensively.
- **Pure lead-sale (pay-per-lead):** Aligns us to volume over quality, which destroys the trust proposition — the exact thing we are selling.
- **Pure advertising:** That is Kerix's model, on Kerix's turf, with Kerix's ten-year head start.
- **Free with a data play:** No, not at this scale. Data monetization requires volume we will not have for years.

---

## 7. Go-to-market strategy

### 7.1 The cold-start sequence

The order is non-negotiable, and it is supply first.

```
Phase A (m1-2)    Phase B (m3-6)      Phase C (m6-12)     Phase D (m12+)
Validation    →   Supply build    →   Demand build    →   Flywheel
20 supplier       100 verified        SEO + outbound      Organic supply
interviews        suppliers,          to buyers;          via inbound;
10 buyer          hand-recruited,     first RFQs          suppliers refer
interviews        free tier           routed              suppliers
```

**Phase A — Validation (months 1–2).** No code. Twenty supplier conversations and ten buyer conversations, in person where possible. Structured (Appendix B) so answers are comparable. Deliverable: a written go/no-go with quotes.

**Phase B — Supply (months 3–6).** Hand-recruit 100 suppliers onto the free tier. Concierge onboarding: we build their profile for them from their existing materials. Nobody fills in a form. Target: 100 profiles, 60+ verified, in one region and one vertical.

**Phase C — Demand (months 6–12).** Programmatic SEO pages go live as supply is populated. Direct outbound to buyers. Manual RFQ routing at first — a founder can be the routing engine for the first fifty requests, and should be, because that is how the matching logic gets designed.

**Phase D — Flywheel (month 12+).** More suppliers → more content → more search traffic → more buyers → more RFQs → more suppliers. Supplier acquisition shifts from field sales to inbound. This is when CAC drops and the model becomes attractive.

### 7.2 Supplier acquisition (Phase B detail)

**Channels, in priority order:**
1. **In-person visits to supplier premises.** Highest conversion, does not scale, absolutely required for the first 100.
2. **Phone outbound** from existing directory data. Cheap, low conversion, good for booking visits.
3. **Trade association and sector-body introductions** `[ASSUMPTION — identify the relevant construction-materials bodies]`.
4. **Trade fairs and sector events** — dense supplier concentration, one day of work for many conversations.
5. **Referral** from onboarded suppliers, incentivised with free verified months.

**The pitch (draft, to be tested):**
> "You already pay for a listing that can't tell you whether it ever won you a deal. We're building the opposite: free to list, and you only hear from us when a buyer with a real project asks for a quote in your category. We verify you once so buyers know you're real. Right now we're onboarding the first hundred suppliers in [region] and I wanted to show you what we're doing."

**What makes this credible:** verification has to be visibly real. If the badge is granted by ticking a box, suppliers will know within a week and the whole proposition is dead.

### 7.3 Buyer acquisition and the SEO engine

SEO is the primary long-run channel. The argument from the brief holds: French-language B2B search intent is high, paid acquisition is expensive relative to deal size, and incumbent traffic proves the demand.

**Programmatic page architecture:**

```
/fournisseurs/{secteur}/{ville}                    e.g. /fournisseurs/ciment/casablanca
/fournisseurs/{secteur}/{ville}/{sous-categorie}
/entreprise/{slug}                                  verified supplier profile
/guides/{topic}                                     editorial, buyer-education
/prix/{materiau}/{region}                           price benchmark pages — Phase 2+
```

The `/prix/` tree is the one incumbents cannot replicate, because it requires real quote data. It should be built as soon as we have statistically meaningful volume, and it is a good reason to instrument quote data properly from day one.

**Content that is not programmatic:** buyer-education guides — how to verify a supplier, what a materials contract should specify, how to structure staged payment. This content ranks, builds trust, and pre-sells the referee proposition.

**Non-SEO buyer channels:** direct outbound to contractors, LinkedIn for procurement roles, sector publications, and — most underrated — asking onboarded suppliers which buyers they wish would find them.

**On the aged-domain question** ❓: budget up to ~MAD 5,000 and buy one only if a genuinely topically relevant francophone or Moroccan B2B domain surfaces. Do not let the search block month one. Do not treat DR as predictive. If nothing relevant appears in a fortnight of casual looking, register a clean domain and move on.

### 7.4 Positioning and messaging

**Positioning statement:**
> For Moroccan SME buyers who need to source from suppliers outside their existing network, [Name] is the B2B trade platform that verifies who you are dealing with and holds you both to the deal — unlike directories, which sell visibility and guarantee nothing.

**Message by audience:**

| Audience | Lead with | Avoid |
|---|---|---|
| Supplier | "Qualified enquiries, not visibility you can't measure" | "Disrupting", anything implying their current methods are stupid |
| Buyer | "Know who you're dealing with before you pay" | Implying their network is untrustworthy |
| Funder | "Transaction infrastructure for SME trade" | "Directory" — it anchors to a low valuation |
| Press | "Formalising SME trade" | Overclaiming scale before we have it |

**Language:** French primary. Arabic essential for supplier-facing surfaces and field material. English for funders and international audiences only. `[ASSUMPTION — confirm in interviews which language suppliers actually prefer for a business tool; do not assume French because the web is French]`

---

## 8. Product and technology plan

### 8.1 Stack decision

**Status changed in 0.2.** v0.1 recorded the frontend as settled. Two layers — **frontend** and **hosting** — are now reopened as ❓ **DECISION** items at a founder's request. The rest stands.

| Layer | Choice | Status | Rationale |
|---|---|---|---|
| Frontend + rendering | Next.js (App Router) **or** WP/Next.js hybrid | ❓ **OPEN** — §8.1.1 | See evaluation below |
| Language | TypeScript throughout | Settled | One language across the stack for a two-person team |
| Database | PostgreSQL | Settled | Relational data, full-text search available before we need anything specialised |
| Search | Postgres FTS initially; dedicated engine (Typesense/Meilisearch) when facets demand it | Settled | Do not buy search infrastructure before you have a search problem |
| Auth | Managed provider | Settled | Never build auth |
| Hosting | Managed platform **or** self-hosted VPS | ❓ **OPEN** — §8.1.2 | See evaluation below |
| CI/CD + source control | Self-hosted GitLab, or GitHub/GitLab SaaS | ❓ Open, low stakes | **Note: this is CI and source control, not hosting.** It runs alongside whatever serves the site |
| Editorial CMS | Depends on §8.1.1 | ❓ Follows frontend | |
| Email/notifications | Transactional provider | Settled | |
| Payments (Phase 1) | PSP for subscriptions only | Settled | Not escrow. Subscriptions only. |
| Payments (Phase 2) | Licensed partner — see §9 | Settled | The gating dependency |

#### 8.1.1 ❓ DECISION — Frontend: Next.js, or a WordPress/Next.js hybrid

**The option on the table:** WordPress owns editorial content (`/guides/`), where its authoring experience genuinely wins. Next.js owns the programmatic SEO pages, verified profiles, and the RFQ/quote flows. Recorded as **open**, not decided.

**First, the SEO premise, addressed directly — because this is why v0.1 closed the question.**

The argument for WordPress here was its "strong SEO capabilities, history, and indexing." That premise does not survive contact with how ranking actually works, and it matters enough to state plainly:

- **Google ranks pages, not content-management systems.** What it evaluates is server-rendered HTML, crawlable structure, internal linking, page speed, and Core Web Vitals. Next.js with SSG/ISR produces all of these at least as well as WordPress, and for tens of thousands of generated pages, better.
- **WordPress's SEO reputation comes from Yoast and a mature plugin ecosystem** that make good practice easy and legible. That is a real advantage for a non-technical editor. It is not a ranking advantage over well-built server-rendered pages.
- **"History and indexing" does not transfer.** A new WordPress install on a new domain has no more tenure than a new Next.js install on the same domain. Domain age belongs to the domain (§7.3's aged-domain question), not to the CMS.
- **CWV cuts the other way.** A plugin-laden WP install typically *loses* on Core Web Vitals, which is itself a ranking input.

**Where WordPress genuinely wins, stated fairly:** editorial authoring UX; a large Moroccan freelance pool who know it; faster time-to-first-content-page; and no engineering time spent building an editorial interface. For §7.3's buyer-education guides — content written by a freelancer in FR/AR — these are real advantages, and they are the honest case for the hybrid.

**Scorecard**

| Axis | Next.js only | WP + Next.js hybrid |
|---|---|---|
| Programmatic SEO at 10k+ pages | Native — the thing SSG frameworks are for | WP does this badly; would need the Next.js side anyway |
| Editorial authoring UX | Needs a CMS choice regardless | **Best available** |
| Core Web Vitals | Strong by default | Depends entirely on plugin discipline |
| Build cost of anything crossing the boundary | One runtime | **Two runtimes — the main cost** |
| Security surface under §9.2 | Small | **Plugin CVE surface, holding verified records and ID documents** |
| Hiring in Morocco | Smaller pool | **Larger pool** |
| Ops burden (2 people) | One thing to run | Two things to run, one needing regular patching |

**The two costs that should decide it.** First, **two runtimes doubles the build cost of anything crossing the boundary** — and the boundary is where the interesting work lives (a guide page linking to live verified suppliers, a price page pulling quote data). Second, **§9.2's finding sharpens the security argument beyond v0.1**: we hold verified company records and ID documents under a CNDP regime that may require F112 authorisation. A plugin-laden install is the largest attack surface in this stack, and a breach is not merely an outage — it is a regulatory event and the end of the trust proposition we are selling.

**Note the hybrid is close to what v0.1 already conceded** ("headless WP is acceptable **as CMS only**"). The distance between the recorded decision and this option is smaller than it appears: if WordPress is headless and confined to `/guides/`, that is the v0.1 position. If WordPress *serves* pages on its own runtime, that is the genuinely new proposal, and it carries both costs above.

**What would settle this:** decide whether either founder will personally write and maintain editorial content. If yes, the authoring UX argument is real and the hybrid earns its cost. If content is outsourced to a freelancer who can be handed any CMS, it does not.

#### 8.1.2 ❓ DECISION — Hosting: managed platform or self-hosted VPS

**A founder's position:** a VPS (self-hosted, potentially with self-hosted GitLab for CI) is the more scalable and controllable option.

**The 0.2 research strengthens this argument, though for a different reason than scalability** — and then partly resolves it.

v0.1 chose "Vercel or equivalent" for zero-ops. §9.2 then found that transferring personal data abroad engages Articles 43–44 of Law 09-08, which looked like a ~2-month authorisation on the critical path. That was a real cost to offshore hosting that v0.1 did not know about.

**Resolved: a European VPS is very likely fine** `[VERIFIED — A]`

The CNDP maintains an **adequacy list** of countries deemed to provide adequate protection, established by **Deliberation 236-2015** (amending 465-2013). **Named EU/EEA states on it include Germany, France, Ireland, Spain, Italy, Denmark, Finland, Austria, Bulgaria, Cyprus, Estonia, Greece, Hungary, Iceland, Latvia, Liechtenstein — plus Canada.**

The procedural difference is significant:

| Destination | What is required | Timeline |
|---|---|---|
| **On the adequacy list** (e.g. Germany, France, Ireland) | **No separate authorisation.** The transfer proceeds under the existing F211 declaration or F112 authorisation for the underlying processing | **None beyond the base declaration** |
| **Not on the list** | **Form F118** authorisation, requiring explicit consent, contractual clauses, or binding corporate rules | **2 months, extendable once** |
| **Morocco (no transfer)** | Nothing | None |

**So the choice is now genuinely open on the merits, not forced by regulation:**

| | Managed (Vercel) | VPS in Morocco | VPS in EU (adequacy list) | VPS elsewhere (e.g. US) |
|---|---|---|---|---|
| CNDP transfer burden | Depends on region — **verify where data actually sits** | **None** | **None beyond base declaration** | **F118, ~2 months** |
| Ops burden | None | Full | Full | Full |
| Cost at our scale | Higher | Lower | Lower | Lower |
| Latency to Moroccan users | Good via CDN | **Best** | Good | Poor |

**The honest counterweight to the VPS argument.** "Scalable" is not where a VPS wins at our scale — a managed platform scales further with less work. Where a VPS genuinely wins is **cost, control, data residency, and not being locked to a vendor's pricing.** Those are good reasons. The cost is that **a two-person team with no ops person now owns patching, backups, monitoring, TLS renewal, and 3am uptime** — and §8.4's own principle is "every hour on a clever stack is an hour not spent on supplier acquisition." §11.1 gives one founder infrastructure ownership; this decision converts that from a light duty to a standing one.

**Recommendation, offered but not recorded as decided:** a VPS in Morocco or on the CNDP adequacy list, with managed Postgres if available, once someone has explicitly accepted the ops burden. If neither founder wants to carry it, managed hosting in an EU region is the lower-risk default and now carries no extra regulatory cost.

**Verify before committing** `[ASSUMPTION — for counsel or the CNDP directly]`**:** retrieve Deliberation 236-2015 in full and confirm the current list — it dates from 2015 and may have been amended. **The `[VERIFIED — A]` above covers the *mechanism* (list exists, listed countries need no separate authorisation, F118 and 2 months otherwise); the specific country roster comes from secondary reporting of the deliberation and should be confirmed against the source document.** CNDP publishes it for download and answers on +212 537 57 11 24.

#### 8.1.3 What remains settled, and why

Everything else in the table above is unchanged. In particular, on **whichever frontend is chosen**: programmatic page generation for `/fournisseurs/{secteur}/{ville}` at scale is a Next.js/SSG job, not a WordPress job. **No option on the table moves the programmatic SEO tree onto WordPress** — the disagreement is only about who serves `/guides/`.

**If the frontend question is reopened again,** reopen it against the two costs in §8.1.1 — the cross-boundary build cost and the §9.2 security surface — rather than against SEO capability, which §8.1.1 addresses on the merits.

### 8.2 Data model — core entities

```
Company           id, legal_name, trade_name, ICE, RC, city, region,
                  sectors[], verification_status, verified_at, created_at
User              id, company_id, name, email, phone, role, locale
Verification      id, company_id, method, documents[], verified_by,
                  verified_at, expires_at, notes
Listing           id, company_id, category_id, description, attributes{}
Category          id, parent_id, name_fr, name_ar, name_en, slug
RFQ               id, buyer_company_id, category_id, spec, quantity, unit,
                  delivery_city, needed_by, budget_range, status, created_at
RFQInvite         id, rfq_id, supplier_company_id, sent_at, viewed_at, status
Quote             id, rfq_id, supplier_company_id, unit_price, total,
                  lead_time_days, validity, terms, status, submitted_at
Deal              id, quote_id, agreed_total, status, closed_at        [Phase 1: self-reported]
Transaction       id, deal_id, escrow_ref, funded_at, released_at      [Phase 2]
Dispute           id, deal_id, raised_by, reason, evidence[], resolution, resolved_at  [Phase 2]
Review            id, deal_id, author_company_id, subject_company_id,
                  ratings{}, text, status
```

**Two notes that matter more than they look:**
- **`Deal` exists in Phase 1 even though we do not touch the money.** Self-reported outcomes ("did this quote become an order?") are how we measure the metric that gates Phase 2. Instrument it from launch even though the data will be incomplete.
- **The `Category` taxonomy is the hardest part of the build**, not the search. Get it wrong and every SEO URL, every RFQ route, and every facet is wrong downstream. Build it *with* suppliers during Phase A, from the words they actually use.

### 8.3 Build sequence and effort

Two people, mixed part-time to full-time. Effort in person-weeks.

| # | Component | Effort | Phase | Notes |
|---|---|---|---|---|
| 1 | Foundations: repo, CI, auth, roles, deploy | 2–3 | 1 | Do not gold-plate |
| 2 | Company profiles + admin CRUD | 3–4 | 1 | |
| 3 | Taxonomy + faceted search | 4–6 | 1 | The taxonomy is the hard part |
| 4 | Programmatic SEO generation + sitemaps | 3–4 | 1 | Build early, iterate constantly |
| 5 | RFQ creation and routing | 4–5 | 1 | The core loop |
| 6 | Quote submission and comparison | 3–4 | 1 | |
| 7 | Verification workflow + admin tooling | 4–8 | 1 | Manual-first is 4; automated is 8+ |
| 8 | Reviews and reputation | 3–4 | 1 | Moderation is most of the work |
| 9 | Admin, moderation, support tooling | 3–4 | 1 | Always underestimated; you live here daily |
| 10 | i18n FR/AR/EN including RTL | 2–4 | 1 | RTL is a layout task, not a translation task |
| 11 | Subscription billing | 2–3 | 1 | |
| 12 | Analytics and metric instrumentation | 2 | 1 | Non-negotiable; you cannot gate Phase 2 without it |
| | **Phase 1 subtotal** | **35–51 pw** | | ≈ 5–7 months at two people |
| 13 | Escrow integration | 6–10 | 2 | Gated on payment partner |
| 14 | Dispute resolution workflow | 4–6 | 2 | Process design > code |
| 15 | KYB automation | 4–6 | 2 | |
| | **Phase 2 subtotal** | **14–22 pw** | | Plus legal in parallel |

**The estimate is defensible for Model A in one vertical.** It is not defensible for a full escrow platform in six months, and neither of you should quote six months for Model B in front of anyone.

### 8.4 Engineering principles for a two-person team

1. **Manual before automated.** The first fifty verifications are done by hand. Automate the path you have actually walked.
2. **Admin tooling is product.** Every hour saved in daily operations is an hour returned to building.
3. **Instrument first.** If a decision gate depends on a metric, the metric ships before the feature.
4. **Boring technology.** No novel infrastructure. Every hour on a clever stack is an hour not spent on supplier acquisition.
5. **One frontend.** Recorded above; stated again because it will be tempting.

---

## 9. Regulatory and legal

**This section is the highest-uncertainty part of the plan and the one most likely to change the business. Every claim here is `[ASSUMPTION — verify with a Moroccan payments lawyer]`. Do not act on this section without professional advice.**

### 9.1 Entity

- **Structure:** SARL (or SARL-AU if a single founder holds initially, converting on the second founder's entry) `[verify current preference with an accountant]`. Note that **a SARL is an eligible form for a payment-institution licence** under Art. 34(2) of Law 103-12 `[VERIFIED — A]` — so this choice does not foreclose Phase 2, though §9.3 explains why we will not be seeking that licence ourselves.
- **No minimum capital** `[VERIFIED — B]`. Since Law 24-10 amending Law 5-96, a SARL can be formed with symbolic capital (1 MAD).
- **Timing:** Register in month 1–2, not after funding. Most public funding instruments require a registered entity, so "no company until funding" and "get funding from a country program" are in direct conflict. **The 0.2 research resolves this tension entirely in favour of registering early:** Tamwilcom's Startup VB requires a company constituted **within the last 8 years**, so early registration creates eligibility rather than risking it (§13.2).
- **Cost: MAD 4,500–16,000** excluding share capital `[VERIFIED — B]`. Components: OMPIC negative certificate MAD 230; statutes drafting MAD 3,000–6,000; RC registration MAD 350; legal publication MAD 900–1,600; accountant fees MAD 3,000–8,000. Registration duties are **exempt** for company-formation instruments. (Sources are company-formation providers and commercially motivated — budget the upper end.)
- **Timeline: 7–15 working days** via a professional; 15–30 DIY; **under a week via the CRI *guichet unique*** with a complete file `[VERIFIED — B]`. One form at the CRI triggers RC registration, tax registration and CNSS affiliation together.
- **Required from the start:** ICE, RC, TP/tax registration, CNSS registration when hiring
- ❓ **DECISION:** who holds the shares at registration, and the vesting arrangement (§11.3). Registering with a split that is not backed by a written vesting agreement is the single most common founder mistake.

### 9.2 Phase 1 — light regulatory load

Phase 1 does not touch third-party funds. We collect subscription payments for our own services, which is ordinary commercial activity. Obligations:

- **Data protection (Law 09-08 / CNDP)** `[VERIFIED — A]`**:** declaration is **required**, not merely possible. Prior declaration (*déclaration préalable*) uses **form F211**, is **free**, and the CNDP issues a receipt within **24 hours**. This is a month-1 admin task, not a legal project. Still needed alongside it: privacy policy, lawful basis, retention policy.
  - **Prior *authorisation* (form F112) — a different and much slower regime.** Required for sensitive categories including **national ID numbers** and **file interconnections**. Processing takes **2 months, extendable once**. Our verification workflow (§10.1) reviews identity documents, so parts of it may fall here rather than under simple declaration. **Confirm scope with counsel before building the verification flow, not after.**
  - **Articles 43–44 — transferring personal data abroad. Largely resolved; see §8.1.2** `[VERIFIED — A]`**.** The CNDP maintains an **adequacy list** (Deliberation 236-2015, amending 465-2013). Transfers to listed countries — **which include Germany, France, Ireland, Spain, Italy and other EU/EEA states, plus Canada** — require **no separate authorisation**; they proceed under the existing F211 declaration for the underlying processing. Transfers to unlisted countries (the **United States** among them) require **Form F118** authorisation, taking **2 months, extendable once**, and justified by explicit consent, standard contractual clauses, or binding corporate rules.
  - **What this means for the hosting decision:** hosting in Morocco or an EU/adequacy-list country carries **no additional CNDP burden**. Hosting in the US does, and puts a 2-month authorisation on the critical path. **This changes the §8.1 hosting question from a regulatory constraint into an ordinary engineering trade-off.** `[ASSUMPTION — confirm the current country list against Deliberation 236-2015 itself; it dates from 2015 and the roster here comes from secondary reporting.]`
- **Consumer/commercial terms:** clear T&Cs, particularly around what verification does and does not warrant
- **Defamation exposure from reviews:** a published reputation system creates real liability. Moderation policy, right of reply, and a takedown process needed before reviews launch. `[verify with counsel]`
- **Liability for verification:** ❓ our T&Cs must be precise about what a "verified" badge asserts. Over-claiming creates liability for deals that go wrong; under-claiming destroys the product's value. This wording is worth paying a lawyer for.

### 9.3 Phase 2 — the regulated question

**Rewritten in 0.2 from the primary statute. This is no longer an open question — the legal position is confirmed and it is stricter than v0.1 assumed.**

#### What the law actually says `[VERIFIED — A]`

Source: Law 103-12 on credit institutions (Dahir 1-14-193, 24 December 2014, as amended by Law 44-20 and Law 50-20). Full text saved to `research-sources/`.

- **Article 15** — payment institutions (*établissements de paiement*) are those offering payment services under Article 16.
- **Article 16** defines payment services to include: « *l'exécution d'opérations de paiement par tout moyen de communication à distance, à condition que l'opérateur agisse uniquement en qualité d'intermédiaire entre le payeur et le fournisseur de biens et services* ». **This describes the Model B escrow flow almost exactly** — a platform acting as intermediary between payer and goods supplier, executing payment remotely.
- **Article 18** prohibits any person not licensed as a credit institution or payment institution from performing Article 16 operations *à titre de profession habituelle*. A platform doing this as its business model is the definition of habitual professional activity.
- **Article 183** — the penalty: **imprisonment of 6 months to 3 years and a fine of MAD 100,000 to 5,000,000**, or one of the two.
- **Article 184** — the court may additionally order closure of the establishment and publication of the judgment at our expense.
- **Article 17** — the safeguarding regime, and genuinely good news for the *product*: funds in payment accounts must sit in a global, separate, individualised account at a deposit-taking credit institution, ring-fenced (*cantonnés*) in the institution's accounts, immune from its own creditors' claims, and in liquidation allocated to the payment-account holders. **That is a real, citable trust guarantee to offer buyers — but only via a licensed partner.**

#### The routes, re-assessed

| Route | Structure | Assessment after 0.2 |
|---|---|---|
| **A. Licensed partner** | A PSP or bank holds funds; we orchestrate and never touch money | **Effectively the only lawful route at our size.** Partner dependency and shared margin remain real risks |
| **B. Trust/escrow account** | ~~Funds in a segregated account we control~~ | **Downgraded — likely unlawful as described in v0.1.** Read against Art. 18, routing customer payments through our own segregated account as a routine part of the business model is very likely the prohibited activity, regardless of manual operation or low volume. The Art. 18 exemptions (commercial credit to one's own contractors, intra-group treasury, salary advances, vouchers for goods sold by the issuer) do not cover third-party escrow. A **notary or lawyer client account** is a genuinely different regime — but then *the notary is the escrow agent, not us*, making it a per-deal legal service rather than a platform feature |
| **C. Own licence** | We become a licensed payment institution | Correctly ruled out. Requires BAM Governor approval on the Credit Institutions Committee's opinion, DGSSI cybersecurity certification, AML/KYC framework, and a compliance officer. **Minimum capital is set by circular, not the statute — secondary sources conflicted (MAD 3M vs 5M) so no figure is quoted here.** Not a two-founder project either way |

**Recommendation: Route A. Route B is not a fallback — treat it as closed unless counsel says otherwise.**

#### The finding that changes the Phase 2 schedule `[VERIFIED — B]`

Moroccan compliance and economics experts state publicly that **« aucun texte spécifique ne régit l'Escrow numérique transactionnel »** — no specific regulation governs digital transactional escrow in Morocco. They are actively calling for Bank Al-Maghrib to issue a dedicated circular authorising payment institutions to act as escrow agents in e-commerce, and for CMI to build a conditional-payment API. Open questions they themselves flag: **escrow agent liability, client-fund cantonment procedures, and maximum blocking periods.**

Three consequences:

1. **The moat thesis is confirmed and strengthened.** §16.3 argues our regulatory position is the real barrier to competition. Independent experts publicly confirm the framework does not yet exist. If we reach Phase 2 with a working arrangement, that barrier is exactly as high as §16.3 hopes.
2. **But the Phase 2 timeline is partly outside our control.** §15.4 schedules escrow pilot at month 18 and general availability at month 21. If it depends on a circular that has not been written, that is not a schedule we own. **§14.1 R3's likelihood is raised accordingly.**
3. **Infrastructure constraint nobody had costed:** SIMT settlement runs at **J+1 to J+2**, described by these experts as incompatible with immediate conditional payment. "Released on confirmed delivery" therefore carries a two-day tail — which lands precisely on supplier cash flow, the reason suppliers extend informal credit today (§2.1). **Raise this in the supplier interviews.**

**Critical dependency, sharpened.** The month-1–2 PSP conversation in §15.1 is no longer "will you work with a company our size." Ask instead: **does your licence permit conditional release on delivery confirmation, what is your maximum permitted hold period, and would you support an orchestration model where we never touch funds?** That is the question whose answer determines the architecture.

**Governing circulars to name in the lawyer meeting** `[VERIFIED — A]`: **7/W/2016** (modified 2/W/2022, 2/W/2024) on payment-service modalities; **6/W/2016** (amended 1/W/2022) on Art. 22; **20/G/2006** (modified 1/G/11, 8/W/16) on minimum capital; **5/W/2015** on licensing application documents.

**Still unresolved and genuinely legal judgement, not research** `[ASSUMPTION — for counsel]`: whether a pure orchestration model (licensed PSP holds and releases on our API instruction, we never touch funds) falls outside Art. 18 altogether. **This is the single question that determines whether Phase 2 is buildable as designed.**

### 9.4 Dispute resolution design

Escrow is the easy half. The hard half is deciding who is right.

- Published rules, written before the first dispute, not during it
- Evidence requirements defined per dispute type (non-delivery, quality, quantity, lateness)
- Escalation: automated → human review → binding platform decision → external arbitration
- ❓ **DECISION:** are our decisions contractually binding on both parties? Binding decisions make us effectively an arbitrator, with the legal weight that carries. Non-binding decisions make the guarantee weak. `[verify what is enforceable under Moroccan law]`
- Reserve fund for goodwill payouts in ambiguous cases — a real line item, not a rounding error

### 9.5 Legal budget

| Item | Cost (MAD) | When |
|---|---|---|
| Company registration | 5,000–15,000 | Month 1–2 |
| T&Cs, privacy policy, verification wording | 10,000–25,000 | Month 3–4 |
| Payments/escrow consultation | 15,000–40,000 | Month 2 (scoping), month 12 (full) |
| Dispute framework and arbitration clauses | 20,000–50,000 | Month 12–15 |
| Founder agreement and vesting | 5,000–15,000 | **Month 1** |
| **Total through month 24** | **55,000–145,000** | |

`[ASSUMPTION — all figures need quotes from actual Moroccan firms]`

---

## 10. Operations

### 10.1 Verification — the operational core

Verification is the product. If it is not genuinely rigorous, nothing else works.

**Tiered model:**

| Tier | Checks | Cost to us | Time |
|---|---|---|---|
| **Basic** | ICE/RC exists and matches; phone answered; email confirmed | ~MAD 30 | 15 min |
| **Verified** | Above + documents reviewed, address confirmed, bank details matched to entity | ~MAD 150 | 1–2 hrs |
| **Verified+** | Above + site visit or video walkthrough, reference calls to two prior buyers | ~MAD 400 | 3–4 hrs |

`[ASSUMPTION — costs are estimates; measure after the first twenty]`

**Renewal:** annual re-verification. Stale verification is worse than none, because it carries authority it has not earned.

**Fraud vectors to design against from day one:** shell companies with real registration documents; hijacked listings of legitimate businesses; review manipulation via fake deals between colluding accounts; suppliers who verify honestly then subcontract to unverified third parties.

### 10.2 Field operations capacity

The number that governs the whole Phase B plan:

| Activity | Time per unit | Units/week/person |
|---|---|---|
| Cold call → booked meeting | 20 min, ~15% conversion | ~40 calls |
| Site visit + pitch | 2 hrs including travel | 8–10 |
| Onboarding (concierge profile build) | 1.5 hrs | 10–12 |
| Verification (Verified tier) | 1.5 hrs | 12–15 |

**One person doing field work full-time acquires roughly 6–8 verified suppliers per week.** 100 suppliers is therefore 13–17 person-weeks of field work — three to four months of one founder's full time. **This does not appear in any engineering estimate and it is the most commonly fatal omission in marketplace plans.** Whoever is not writing the RFQ logic should be doing this.

### 10.3 Support

Phase 1: founders handle support directly, shared inbox, WhatsApp Business for suppliers `[most suppliers will prefer WhatsApp to email — verify in interviews]`. Target: same-business-day response. Founders doing support is not a temporary inefficiency; it is the primary product-feedback channel for the first year.

### 10.4 Key operating metrics

| Metric | Why | Target by m12 |
|---|---|---|
| Verified suppliers | Supply-side liquidity | 100 |
| Supplier response rate | Marketplace health | >60% within 48h |
| RFQs submitted/month | Demand-side liquidity | 80 |
| RFQs receiving ≥3 quotes | Match quality | >70% |
| **Quote-to-deal conversion** | **The gate metric** | **>15%** |
| Paying suppliers | Revenue | 30 |
| Supplier monthly churn | Retention | <5% |
| Organic sessions/month | SEO engine | 8,000 |

---

## 11. Team, roles, and equity

### 11.1 The split

Not by technology. By outcome ownership — each founder owns metrics end to end.

**Founder — Product & Platform**
- Data model, taxonomy, search
- RFQ and transaction flows
- Verification systems and admin tooling
- Infrastructure and security
- **Owns:** does the core loop work, and does it stay up

**Founder — Growth & Supply**
- SEO architecture and content system
- Supplier acquisition and onboarding (the field work in §10.2)
- Funding applications and program relationships
- Pricing and monetization
- **Owns:** qualified traffic in, verified suppliers on

Both write code. Both talk to users. The split is accountability when a number moves the wrong way — not permission to touch files.

### 11.2 First hires

`[ASSUMPTION — contingent on funding; see §12]`

| Role | When | Why |
|---|---|---|
| Field sales / supplier success | Month 9–12 | Field capacity is the binding constraint on growth |
| Full-stack engineer | Month 12–15 | Phase 2 build |
| Operations / verification analyst | Month 15–18 | Verification volume exceeds founder capacity |

### 11.3 Equity and vesting ❓ **DECISION — before either of you writes production code**

The uncomfortable conversation that resolves cheaply now and expensively later.

**Recommended structure:**
- **Split:** an even or near-even split between two committed full-time founders is usually right. Idea origination is worth less than eighteen months of execution — but if one founder is part-time or contributing capital, adjust deliberately and write down the reasoning.
- **Vesting:** four-year vest, one-year cliff, for both founders, including the originator. This exists precisely so neither of you has to rely on the other's future enthusiasm.
- **Acceleration:** single-trigger on acquisition for both, or double-trigger. Decide now.
- **Departure:** unvested shares return to the company. Vested shares are kept, subject to a buyback right at fair value.
- **IP assignment:** all work product assigned to the company, in writing, from day one.
- **CEO:** ❓ **decide who it is.** Two-founder companies with no designated decision-maker stall on exactly the kind of disagreement you have already had about WordPress. This is not about status; it is about who breaks a tie at 11pm.

**Do not skip this because it is awkward. This section is more likely to determine the outcome than the entire technology plan.**

---

## 12. Financial plan

**All figures are planning estimates with weak inputs. Rebuild this section with real numbers after the Phase A interviews.**

### 12.1 Cost structure — Year 1

| Category | Monthly (MAD) | Annual (MAD) | Notes |
|---|---|---|---|
| Founder living costs (2) | 15,000 | 180,000 | Minimal; assumes low personal burn |
| Hosting and infrastructure | 800 | 9,600 | Small at this scale |
| SaaS tooling | 1,200 | 14,400 | Auth, email, analytics, monitoring |
| Domain and SEO tools | 700 | 8,400 | Ahrefs/Semrush tier |
| Legal and accounting | — | 60,000 | Lumpy; see §9.5 |
| Company registration | — | 10,000 | One-time |
| Field costs (travel, meetings) | 2,000 | 24,000 | Fuel, meals, materials |
| Verification costs | 1,500 | 18,000 | Scales with supplier count |
| Marketing and content | 2,000 | 24,000 | Freelance FR/AR writing |
| Contingency (15%) | — | 52,000 | |
| **Total Year 1** | | **~400,000** | ~$39,600 |

### 12.2 Revenue projection — conservative case

`[ASSUMPTION — the conversion rates here are guesses. This is the case to plan against.]`

| Month | Verified suppliers | Paying | ARPA (MAD) | MRR (MAD) |
|---|---|---|---|---|
| 6 | 40 | 0 | — | 0 |
| 9 | 70 | 8 | 400 | 3,200 |
| 12 | 100 | 30 | 450 | 13,500 |
| 15 | 140 | 50 | 480 | 24,000 |
| 18 | 190 | 75 | 500 | 37,500 |
| 21 | 250 | 105 | 520 | 54,600 |
| 24 | 320 | 145 | 550 | 79,750 |

**Year 1 revenue:** ~MAD 60,000. **Year 2 revenue:** ~MAD 620,000.

### 12.3 Three scenarios

| | Pessimistic | Conservative | Optimistic |
|---|---|---|---|
| Paying suppliers, m24 | 60 | 145 | 300 |
| ARPA, m24 (MAD) | 450 | 550 | 700 |
| MRR, m24 (MAD) | 27,000 | 79,750 | 210,000 |
| Phase 2 live by | No | m20–24 | m16 |
| Transaction revenue, m24 | 0 | 15,000/mo | 60,000/mo |
| **Verdict** | Model A is a lifestyle business; reconsider | Fundable, on track | Raise properly and accelerate |

**What separates them:** almost entirely quote-to-deal conversion and supplier retention. Not traffic, not build speed.

### 12.4 Break-even

Against a monthly operating cost of ~MAD 25,000 excluding founder pay, break-even is **~50–55 paying suppliers**, reached around **month 15–16 in the conservative case**. Including founder living costs (~MAD 40,000/month total), break-even is **~85 paying suppliers**, around **month 19–20**.

### 12.5 Funding requirement

| Phase | Period | Need (MAD) | Purpose |
|---|---|---|---|
| Phase 0–1 | m1–12 | 420,000 | Build, validate, first 100 suppliers |
| Phase 1b | m12–18 | 500,000 | First hire, growth, sustain to break-even |
| Phase 2 | m12–24 | 1,200,000–2,000,000 | Legal, licensing, escrow build, two hires |
| **Total to m24** | | **~2.1M–2.9M** | ~$210k–290k |

---

## 13. Funding strategy

### 13.1 The sequencing error to avoid

The instinct to "build first, then seek funding" is backwards here. Morocco's current instruments are designed to fund exactly the stage we are at now. Arriving with a finished product asking for scale money means competing against teams asking for build money with a better story about what the funding unlocks — and it means twelve months of unfunded runway from our own pockets in the meantime.

**Apply at prototype stage. It is cheaper and strictly more likely to land.**

### 13.2 Target instruments

`[ASSUMPTION — all program details need verification against current published criteria; terms change]`

| Source | Type | Indicative size | Stage | Notes |
|---|---|---|---|---|
| **Tamwilcom — Startup Venture Building** | Stipend + grant + two loan tiers, **all non-dilutive** | Up to ~MAD 2.7M across four instruments | Ideation → growth | **Launched December 2025; public relaunch April 2026.** MAD 700M / 800 startups is a *forward target*, not a track record. **Primary target — see breakdown below.** |
| **Mohammed VI Investment Fund — Fonds Startups** | Early-stage equity via appointed managers | ~MAD 2.5B across 9 managers | Pre-seed → Series A+ | **9 management companies preselected at Gitex Africa, April 2026.** Equity, so dilution. Better suited to Phase 2 |
| Bank-affiliated SME programs | Loan/grant | Varies | Various | Lower profile, less competition |
| Accelerators (local and regional) | Small equity + program | Small | Pre-seed | Value is network and credibility, not cash |
| Angels | Equity | MAD 200k–1M | Pre-seed | Local B2B/construction angels bring distribution |
| Revenue | — | — | — | The best funding; §12.4 |

**Nearly all require a registered Moroccan entity.** This is why §9.1 puts registration in month 1–2.

#### Startup Venture Building — the four instruments `[VERIFIED — A]`

| Instrument | Amount | Nature |
|---|---|---|
| **Bourse de Vie** | Up to **70% of prior 12 months' average gross salary**, ceiling **MAD 40,000/month per founder**, max **12 months** | Non-dilutive stipend |
| **Bourse d'Incubation** | Up to **MAD 200,000** | Grant — prototyping and validation |
| **Prêt d'Honneur** | Up to **MAD 500,000** | Interest-free, unsecured |
| **Prêt d'Amorçage** | **MAD 500,000 – 2,000,000** | Unsecured — growth and first raise |

**Eligibility** `[VERIFIED — B]`: digital startups constituted **within the last 8 years**, innovative solution with a digital component, **applications go through partner operators rather than to Tamwilcom directly.**

**Operators:** Technopark, CEED Maroc, Flat6Labs, Open Startup International, Renew Capital, 500 Global. Technopark alone is mandated to incubate 240 startups.

**Why this reshapes §12.5.** The Bourse de Vie ceiling is MAD 40,000/month *per founder*; §12.1 budgets MAD 15,000/month for both founders combined. Add the MAD 200,000 incubation grant — aimed exactly at the prototype stage §13.1 argues we should apply from — and **the entire Phase 0–1 requirement of MAD 420,000 may be coverable without equity or debt.** This is the strongest single finding of the 0.2 research pass.

**Two cautions.** The Bourse de Vie is calculated from *prior salary*, so it rewards founders leaving salaried employment; a founder with no recent salaried income may get little from it. **That is a founder-specific fact neither of us can look up — check it against your own situations before building it into a plan.** And we do not know whether the instruments stack.

**The action is a phone call, not more research.** Contact Technopark or CEED and ask: can the four instruments be combined and in what order; does a B2B marketplace qualify as "innovative with a digital component"; what are the current cohort dates; what does the Bourse de Vie require by way of employment history; and does accepting Startup VB financing constrain a later equity raise from a Fonds Startups manager. **The authoritative criteria live at `tamwilstartups.ma`, which blocks automated access — open it manually.**

### 13.3 Application timeline

| When | Action |
|---|---|
| Month 1–2 | Register SARL. Obtain ICE/RC. Confirm current eligibility criteria directly with the program. |
| Month 2–3 | Prepare application: this plan condensed, validation evidence from Phase A interviews, team credentials. |
| Month 3–4 | Submit. Expect 2–4 months to decision `[verify]`. |
| Month 6–8 | Decision. Adjust hiring and Phase 2 timing accordingly. |
| Month 12–15 | Second instrument for Phase 2 (escrow build, legal, licensing). |

### 13.4 What funders will actually ask

Prepare answers before applying, not during:

1. Why has nobody done this? (See §17 — you must know whether someone tried and failed.)
2. What stops Kerix from copying it? (§5.3 — honest answer: nothing, in Phase 1; the licensing burden, in Phase 2.)
3. How do you get the first hundred suppliers? (§7.2, §10.2 — the answer is field work, and it should be specific.)
4. Do you hold the money? (§9.3 — the answer determines which box they file you in.)
5. What are you instrumenting that proves this works? (§10.4, §15.3.)
6. Who is the eventual buyer? (§16.)

### 13.5 What we will not do

- Take strategic investment from a bank or telecom before Phase 2 is proven — it caps the acquirer pool early and at a low price
- Raise on a valuation that requires a Phase 2 outcome to justify, before Phase 2 is de-risked
- Accept funding conditioned on a pivot away from the transaction model to a pure directory

---

## 14. Risk register

### 14.1 Register

| # | Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|---|
| R1 | **Cold start fails** — cannot reach 100 suppliers | Medium | Fatal | Field-first plan (§7.2); free tier; concierge onboarding; measure weekly against §10.2 capacity | Growth |
| R2 | **No demand-side pull** — buyers don't submit RFQs | Medium | Fatal | Validate in Phase A before building; manual routing first; direct outbound | Growth |
| R3 | **Escrow legally impractical** at our size | **Medium-High** ↑ | Severe | **Raised in 0.2.** Confirmed regulated (Arts. 15/16/18); Route B closed; and no framework yet exists for digital escrow — experts are lobbying BAM for a circular. Route A is the only route. Establish partner licence scope in month 1–2 (§9.3) | Product |
| R3b | **Phase 2 blocked by regulation that does not yet exist** | Medium | Severe | **New in 0.2.** Escrow authorisation depends partly on a BAM circular outside our control. Mitigate by executing Phase 1 fast, staying visible to the regulator and fintech community, and treating §15.4's dates as conditional | Product |
| R3c | **Cross-border data transfer authorisation delays launch** | **Low** ↓ | Moderate | **Downgraded in 0.2 after further research.** CNDP's adequacy list (Delib. 236-2015) covers EU/EEA states and Canada — hosting there needs **no separate authorisation**. Risk applies only if we host in an unlisted country (e.g. US), which triggers F118 and ~2 months. **Mitigation: host in Morocco or the EU (§8.1.2)** | Product |
| R4 | **Quote-to-deal conversion too low** — suppliers churn | Medium-High | Severe | Instrument from day one; gate Phase 2 on it; improve matching before scaling supply | Product |
| R5 | **Incumbent copies Phase 1** | Medium | Moderate | Speed to Phase 2; own the transaction data; relationships | Both |
| R5b | **Existing entrants already occupy parts of Phase 1** | **High** | Moderate | **New in 0.2.** Procurement.ma routes RFQs free; BTPro publishes city-level material prices. Our Phase 1 is a better-executed version of things buyers can already do for nothing. Mitigate by making verification visibly real (§7.2) — it is our only Phase 1 differentiator — and by assessing BTPro as a partner rather than only a rival | Growth |
| R6 | **Founder conflict / departure** | Medium | Fatal | Vesting, written agreement, named CEO — §11.3, month 1 | Both |
| R7 | **Funding doesn't land** | Medium | Severe | Apply early at prototype stage; keep burn low enough to survive on revenue | Growth |
| R8 | **Trust default beats us** — buyers keep using their network | Medium-High | Severe | Position as complement, not replacement (§5.2); target out-of-network sourcing specifically | Growth |
| R9 | **Verification fraud** undermines the badge | Medium | Severe | Tiered verification; annual renewal; reference calls; publish what the badge means | Product |
| R10 | **Review manipulation** | Medium | Moderate | Tie reviews to recorded deals only; moderation; right of reply | Product |
| R11 | **Scope creep past 6 months** | High | Moderate | One vertical, one region, one flow; §8.3 as the contract | Product |
| R12 | **Stack decision reopened repeatedly** | Medium | Moderate | **Updated in 0.2:** frontend and hosting are now explicitly ❓ OPEN (§8.1.1, §8.1.2) with the arguments laid out on both sides. **Settle them at the §15.1 gate and record the reasoning.** After that, reopen only against the two stated costs — cross-boundary build cost and §9.2 security surface — not against SEO capability, which §8.1.1 addresses | Both |
| R13 | **Dispute liability** exceeds reserves | Low (Ph.2) | Severe | Published rules; caps in T&Cs; reserve fund; insurance `[verify availability]` | Product |
| R14 | **Currency/macro shock** hits construction demand | Low-Medium | Moderate | Vertical diversification after month 24 | Both |

### 14.2 The three that deserve most of the worry

**R1 and R2 together are the marketplace cold-start problem, and they kill more platforms than every technical risk combined.** They are addressed by field work, not by product quality. Budget founder time accordingly.

**R4 is the quiet one.** A platform can look healthy — suppliers signing up, RFQs flowing — while quotes never become deals. Suppliers churn at month six, LTV collapses, and the model fails despite good top-line metrics. Instrument this from launch.

**R6 is the one nobody plans for.** Fix it in month one with paperwork.

---

## 15. Milestones and decision gates

### 15.1 Phase 0 — Validation (months 1–2)

**Deliverables**
- [ ] 20 structured supplier interviews, written up
- [ ] 10 structured buyer interviews, written up
- [ ] Vertical and region confirmed or changed, with reasoning
- [ ] SARL registered; ICE and RC obtained — **via CRI *guichet unique*, under a week with a complete file (§9.1)**
- [ ] Payments lawyer consulted — **the question is now specific: does a pure orchestration model, where a licensed PSP holds and releases funds on our instruction and we never touch them, fall outside Art. 18 of Law 103-12? (§9.3)**
- [ ] One PSP conversation held — **ask: does your licence permit conditional release on delivery confirmation, what is your maximum hold period, will you support orchestration by a platform our size?**
- [ ] Founder agreement signed: equity, vesting, roles, CEO
- [ ] ~~Competitive post-mortem: has anyone tried this in Morocco?~~ **Partly answered in 0.2 — see §5.1. Remaining question: are BTPro, MABANI, Procurement.ma, BTP Business Market and Business Hub actually operating businesses, or live homepages? Answer via the supplier interviews (Appendix B).**
- [ ] **NEW — Call Technopark / CEED / Flat6Labs about Startup VB** (§13.2). Highest-value call available: can the four instruments stack, do we qualify, what are the cohort dates, what does the Bourse de Vie require by way of salary history
- [ ] **NEW — Visit `tamwilstartups.ma` manually** for authoritative eligibility criteria (blocks automated access)
- [ ] **NEW — CNDP: file the F211 declaration** (free, 24h) and **determine whether Arts. 43–44 cross-border authorisation is needed for offshore hosting** — 2-month lead time, gates §8.1 (§9.2)
- [ ] One-page joint memo: model, vertical, monetization, who does what, equity
- [ ] **Stack decision — two items now explicitly open (§8.1):**
  - [ ] **Frontend:** Next.js only, or WP/Next.js hybrid for editorial? **Settle by answering one question: will either founder personally write and maintain the `/guides/` content?** (§8.1.1)
  - [ ] **Hosting:** managed, or self-hosted VPS? **Requires one founder to explicitly accept the ops burden.** Morocco or EU/adequacy-list carries no CNDP cost; US does (§8.1.2)
  - [ ] Confirm the CNDP adequacy country list against Deliberation 236-2015 itself before committing to a region

**🚦 GATE 0 — proceed only if:**
1. ≥12 of 20 suppliers describe a real problem finding qualified buyers
2. ≥6 of 10 buyers describe a trust or recourse failure, unprompted
3. ≥8 suppliers say they would list on a free verified directory
4. Escrow has a plausible legal route (Route A or B)
5. Both founders have signed the founder agreement

**If gate 0 fails, do not build. Change the vertical, or stop.**

### 15.2 Phase 1 — Build and launch (months 3–8)

- [ ] M3: taxonomy built with supplier input; foundations shipped
- [ ] M4: profiles, admin, verification workflow live internally
- [ ] M5: search and facets; first 25 suppliers onboarded manually
- [ ] M6: programmatic SEO pages live; 40 verified suppliers; **soft launch**
- [ ] M7: RFQ and quote flow live; first RFQ routed (manually is fine)
- [ ] M8: reviews live; 70 verified suppliers; **public launch**

**🚦 GATE 1 (month 8) — proceed to monetization if:** 70+ verified suppliers; 20+ RFQs submitted; ≥50% receiving 3+ quotes; ≥3 confirmed deals attributable to the platform.

### 15.3 Phase 1b — Monetize and prove the loop (months 9–15)

- [ ] M9: paid tiers live; first paying supplier
- [ ] M12: 100 verified, 30 paying, 8,000 organic sessions/month
- [ ] M15: 140 verified, 50 paying, break-even on direct costs

**🚦 GATE 2 (month 15) — THE PHASE 2 GATE. Begin escrow work only if:**
1. **Quote-to-deal conversion ≥15%** — the single most important number
2. ≥50 paying suppliers with <5% monthly churn
3. ≥40 confirmed deals recorded
4. Buyers have explicitly asked for payment protection, unprompted, repeatedly
5. A payment partner has agreed in principle
6. Funding secured or committed for the Phase 2 build

**If gate 2 fails, do not start escrow.** Fix the core loop first. An escrow layer on a marketplace that does not close deals is expensive theatre.

### 15.4 Phase 2 — Referee (months 15–24)

- [ ] M15–18: legal framework, partner integration, dispute rules published
- [ ] M18: escrow live in pilot with 10 trusted suppliers
- [ ] M21: escrow generally available; first dispute resolved under published rules
- [ ] M24: 320 verified, 145 paying, transaction revenue material, second vertical scoped

---

## 16. Exit thesis

### 16.1 The honest version

A five-year exit is a reasonable ambition and a bad plan. The Moroccan acquirer pool for a B2B marketplace is thin. Planning *toward* an exit distorts decisions; building an asset that several different buyers would want does not.

### 16.2 Plausible acquirers and what each buys

| Acquirer type | What they want | What we must instrument now |
|---|---|---|
| **Bank / financial institution** | SME distribution; lending origination data | Transaction volume; verified financial behaviour; creditworthiness signals |
| **Telecom** | SME digital-services bundle | Active SME accounts; engagement; ARPA |
| **Regional/pan-African marketplace** | Morocco market entry | Supplier count; category coverage; geographic depth |
| **Construction-sector incumbent** | Digital channel; procurement control | Buyer relationships; category share |
| **Incumbent directory** | Defensive; the transaction layer they lack | Everything they don't have — transaction records |

**These wants conflict.** A bank cares about credit signals; a marketplace cares about supplier count; a telecom cares about active accounts. **Deciding which asset we are building — even provisionally — changes what we instrument from day one.** That is a conversation for now, not year four. ❓

### 16.3 What actually makes this acquirable

Not traffic. Not listings. Three things:

1. **Transaction volume flowing through us** — proof the loop works, and not reproducible by scraping
2. **A verified supplier network with a maintained trust record** — expensive to rebuild, and the annual re-verification discipline is what makes it credible
3. **Regulatory position** — if we reach Phase 2 with a working escrow arrangement, the licensing and partnership burden is a moat that a competitor must pay for in time, not money

Item 3 is why Phase 2 matters strategically and not just financially. **Model A alone is a business. Model B is an acquirable asset.**

---

## 17. Open questions and research backlog

Ordered by how much they would change this plan.

**Status after the 0.2 desk-research pass. Answered items are struck through with the finding; the rest are unchanged or sharpened.**

### Blocking — answer before building

1. ~~**Has someone already tried a Moroccan B2B escrow or verified-supplier play?**~~ **PARTLY ANSWERED (§5.1).** Verified-supplier and RFQ-routing plays exist and are live — Procurement.ma routes RFQs free; BTPro publishes city-level material prices; MABANI is a construction materials directory. **No one is named as attempting escrow**, and experts confirm no regulatory framework for it exists. *Remaining:* are these operating businesses or live homepages? → supplier interviews.
2. ~~**Is escrow legally practical for a company our size?**~~ **ANSWERED (§9.3) `[VERIFIED — A]`.** It is regulated under Arts. 15/16/18 of Law 103-12; unlicensed activity carries 6mo–3yr imprisonment and MAD 100k–5M fines. Route A (licensed partner) is effectively the only lawful route; Route B is closed. *Remaining for counsel:* **does a pure orchestration model, where we never touch funds, fall outside Art. 18?** That single question determines whether Phase 2 is buildable as designed.
3. **Will any PSP work with us at our scale?** — one conversation, month 1–2. **Sharpened (§9.3):** ask about licence scope for conditional release, maximum hold period, and support for orchestration — not merely willingness.
4. **Do buyers actually experience recourse failure often enough to change behaviour?** (§2.2) — buyer interviews. **Unchanged. This remains the core hypothesis and no desk research can touch it.**
5. **Equity, vesting, CEO** (§11.3) — founders, month 1. **Unchanged. A decision, not a fact.**

### High priority

6. ~~Real market sizing for construction materials (§4.1)~~ **PARTLY ANSWERED `[VERIFIED — A]`.** GDP MAD 1,720.2bn; BTP value added ~MAD 100bn (~6% of GDP); sector growth ~6% in 2025, 4.1% forecast 2026; 1.2M+ employed. *Remaining:* materials-procurement share and SME-B2B share are **not published** — retrieve HCP input-output tables manually, or plan bottom-up as §4.1 recommends.
7. Supplier count and geographic distribution in the target region — **not yet researched; next block**
8. What suppliers currently pay for lead generation, and what a lead is worth to them — **field only.** Kerix's paid pricing is unpublished; **BTPro's is MAD 499/month `[VERIFIED — A]`, a useful anchor (§6.2)**
9. ~~Current Tamwilcom eligibility criteria and application timeline~~ **LARGELY ANSWERED (§13.2) `[VERIFIED — A]`.** Four non-dilutive instruments; company must be <8 years old; apply through partner operators. *Remaining:* whether instruments stack, cohort dates, Bourse de Vie salary-history rules → **phone call to Technopark/CEED**
10. Whether suppliers prefer French or Arabic for a business tool — **field only, do not assume**
11. Whether the launch region should be Casablanca–Settat or where a founder's network is strongest — **a founder decision, not a research question**

### Added by the 0.2 research pass

18. **Does accepting Tamwilcom Startup VB financing constrain a later equity raise** from a Mohammed VI Fonds Startups manager? (§13.2)
19. **Is CNDP Arts. 43–44 authorisation required for our hosting choice**, and does verification's handling of ID documents push us into the F112 authorisation regime? (§9.2) — **2-month lead time, on the critical path**
20. **What is the minimum capital under Circular 20/G/2006** as modified? Secondary sources conflicted; not retrievable online. Ask the lawyer or BAM directly
21. **Is BTPro a competitor or a potential partner?** They are buyer-side, we are supply-side (§5.1)
22. **How does J+1/J+2 settlement affect the escrow product design and supplier cash-flow expectations?** (§9.3)

### Medium priority

12. Construction-materials trade associations and their gatekeepers
13. Sector trade fairs and their calendar
14. Availability and cost of professional/liability insurance for a platform of this type
15. Whether platform dispute decisions can be made contractually binding under Moroccan law
16. Whether a relevant aged domain exists at a sane price — timeboxed to two weeks, non-blocking

---

## 18. Appendices

### Appendix A — Glossary

| Term | Meaning |
|---|---|
| **ICE** | Identifiant Commun de l'Entreprise — Moroccan company identifier |
| **RC** | Registre de Commerce — commercial register number |
| **SARL** | Société à Responsabilité Limitée — Moroccan limited liability company |
| **RFQ** | Request for Quotation |
| **KYB** | Know Your Business — corporate identity verification |
| **PSP** | Payment Service Provider |
| **ARPA** | Average Revenue Per Account |
| **Model A** | Verified discovery and RFQ routing; no funds held |
| **Model B** | Escrow and referee; funds held via licensed partner |

### Appendix B — Interview guides

**Supplier interview (30 min, in person where possible)**
1. How do buyers find you today? Walk me through the last new customer you won.
2. What do you currently pay for visibility or leads? Do you know if it produced a deal?
3. **Are you listed on Kerix, Procurement.ma, BTPro, MABANI, or BTP Business Market? Did any of them ever produce an actual order?** *(Added in 0.2. One question that answers competitor scale, quality, and willingness-to-pay at once — and tells us whether these platforms are real businesses or just live homepages. Kerix's paid pricing is unpublished; this is how we learn it.)*
4. How many enquiries do you get monthly? What fraction are serious?
5. What happens when a buyer doesn't pay? How often?
6. Have you turned down a buyer because you couldn't assess them?
7. What would a genuinely qualified enquiry be worth to you, in dirhams?
8. If a platform verified you and sent only serious buyers, what would you pay per month?
9. **If a buyer paid into a protected account and the money reached you one to two days after delivery was confirmed, would that be better or worse than how you get paid today?** *(Added in 0.2. Moroccan interbank settlement runs at J+1 to J+2, so escrow release carries an unavoidable tail — §9.3. This tests whether that tail is acceptable against the informal credit suppliers extend today.)*
10. What would make you distrust a platform like this?
11. Who else should I talk to?

**Buyer interview (30 min)**
1. Walk me through the last time you sourced from a supplier you hadn't used before.
2. How did you decide they were trustworthy?
3. Has a supplier ever failed you — late, short, wrong quality? What did you do?
4. How do you know you're paying a fair price?
5. How much time does sourcing a new supplier take you?
6. Would you pay a supplier through a platform that held the money until delivery? Why not?
7. What would make you use a platform instead of calling someone you know?
8. Who else should I talk to?

**Rule: do not pitch during these interviews.** Ask, record, shut up. A supplier being polite about your idea is worth nothing; a supplier describing a real loss is worth everything.

### Appendix C — Founder agreement checklist

- [ ] Equity split, with written reasoning
- [ ] Vesting schedule (recommend 4 years, 1-year cliff, both founders)
- [ ] Acceleration on acquisition — single or double trigger
- [ ] Treatment of unvested shares on departure
- [ ] IP assignment to the company
- [ ] Roles and decision rights; named CEO and tie-break authority
- [ ] Time commitment expected of each founder
- [ ] Capital contributions and treatment of founder loans
- [ ] What happens if one founder wants out — buyback at what valuation
- [ ] Non-compete and confidentiality
- [ ] Dispute-resolution mechanism between founders
- [ ] Review date for this agreement

### Appendix D — Document control

| Version | Date | Change | Author |
|---|---|---|---|
| 0.1 | 12 Aug 2026 | Initial draft from pre-meeting brief | — |
| 0.2 | 13 Aug 2026 | Desk-research pass: regulatory (§9), funding (§13), market sizing (§4.1), competitive landscape (§5). Findings, sources and confidence ratings in `RESEARCH-LOG.md`; primary documents in `research-sources/` | — |
| 0.3 | 13 Aug 2026 | §8.1 restructured: frontend and hosting reopened as ❓ DECISION items (§8.1.1, §8.1.2) at a founder's request. CNDP adequacy-list research resolves the offshore-hosting question and downgrades R3c | — |

**What changed in 0.2, in one paragraph.** Escrow's legal position moved from open question to confirmed constraint, and it is stricter than assumed — Route B is closed and the framework for digital escrow does not yet exist, which raises R3 and puts part of the Phase 2 timeline outside our control. Tamwilcom's Startup Venture Building turned out to be four months old rather than an established program, offering non-dilutive instruments that may cover most of Phase 0–1. The competitive landscape gained a construction-specific cluster that v0.1 missed entirely, including one platform already publishing the price data §7.3 called unreplicable and another already routing RFQs for free. Sector sizing gained real HCP figures at the top and honest blanks below them. Two baseline numbers — the USD rate and Kerix's scale — were simply wrong.

**What did not change, and why.** Pricing, unit economics, conversion rates, verification costs, supplier counts, language preference, and every claim in §2.2 remain assumptions. These have no published answers, and filling them with figures borrowed from other markets would have produced a document that reads as more certain while being less true. **The blanks are deliberate.**

**Next review:** after Phase 0 interviews complete. This document should be substantially rewritten at that point — most of the remaining `[ASSUMPTION]` markers become facts or the plan changes.

---

*This is a working document. Its value is in being argued with, revised, and made specific. A business plan that survives contact with twenty supplier interviews unchanged was not a plan; it was a wish.*
