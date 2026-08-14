# Research Log — verification of BUSINESS-PLAN.md assumptions

**Started:** 13 August 2026
**Purpose:** Replace `[ASSUMPTION — verify]` markers in BUSINESS-PLAN.md with sourced facts, or confirm they cannot be desk-verified and must go to the field.

## Confidence ratings used below

| Rating | Meaning |
|---|---|
| **A — Primary** | Official text: statute, regulator page, program owner's own site. Quotable. |
| **B — Corroborated secondary** | Two or more independent secondary sources agreeing. Usable, flag the source. |
| **C — Single secondary** | One secondary source. A lead for a professional, not a fact. |
| **D — Unresolvable by desk research** | Requires interview, lawyer, or direct contact with the institution. |

**Rule applied throughout:** nothing below rating B goes into BUSINESS-PLAN.md as prose. C and D stay marked as assumptions.

---

## BLOCK 1 — REGULATORY

### 1.1 Can we hold third-party funds? (§9.3, §17 blocking Q2) — **RATING A**

**Answer: No, not without a licence. And the plan's Route B fallback is more legally fragile than §9.3 assumes.**

Source: Law 103-12 on credit institutions, promulgated by Dahir 1-14-193 of 24 December 2014, as amended by Law 44-20 (2020) and Law 50-20 (2021). Full text saved to `research-sources/loi-103-12-full-text.txt`.

**Article 15** — payment institutions (`établissements de paiement`) are those offering one or more of the payment services in Article 16.

**Article 16** defines payment services to include:
> « l'exécution d'opérations de paiement par tout moyen de communication à distance, à condition que l'opérateur agisse uniquement en qualité d'intermédiaire entre le payeur et le fournisseur de biens et services »

This is **precisely** the Model B escrow flow: a platform acting as intermediary between payer and goods supplier, executing payment remotely. Escrow as described in §3.2 is a regulated payment service, not an adjacent activity.

**Article 18** — the monopoly provision:
> « il est interdit à toute personne non agréée en qualité d'établissement de crédit ou d'établissement de paiement d'effectuer, à titre de profession habituelle, les opérations visées aux articles premier et 16 »

Performing Article 16 operations *as a habitual profession* without a licence is prohibited. A platform doing this as its business model is the definition of `à titre de profession habituelle`.

**Article 183** — penalty for breach of Article 18:
> imprisonment of **6 months to 3 years** and a fine of **MAD 100,000 to 5,000,000**, or one of the two.

**Article 184** — the court may additionally order closure of the establishment and publication of the judgment at the convicted party's expense.

**Article 17** — the safeguarding regime, relevant to how a licensed partner must handle the money:
> Funds in payment accounts must be deposited in a *global, separate and individualised* account at a credit institution authorised to receive demand deposits. They must be distinctly identified and ring-fenced (`cantonnés`) in the payment institution's accounts. The balance cannot be seized by the payment institution's own creditors, and in liquidation those funds go to the payment-account holders.

Article 17 is genuinely good news for the *product*: client funds are legally protected from the platform's own insolvency. It is the basis for an honest trust claim to buyers — but only via a licensed partner.

**Article 34(2)** — payment institutions must be constituted as a `société anonyme` (SA) or `société à responsabilité limitée` (SARL). So the SARL form in §9.1 does not itself bar licensing.

**Article 36** — minimum capital is set by circular of the Wali of Bank Al-Maghrib per category, not in the law itself.

#### What this changes in the plan

- §9.3 Route C ("own licence") is correctly dismissed, and now for a documented reason.
- **§9.3 Route B is the problem.** The plan describes it as "funds in a segregated account, possibly under a notary or lawyer" and calls it a "manual fallback for the first deals." Read against Article 18, routing customer payments through our own segregated account as a routine part of the business model is very likely the prohibited activity, regardless of manual operation or low volume. The exemptions listed in Article 18 (commercial credit to one's own contractors, intra-group treasury, salary advances, vouchers for goods sold *by the issuer*) do not cover third-party escrow. A notary/lawyer client account is a genuinely different structure — notaries operate under their own professional regime — but that means **the notary is the escrow agent, not us**, which is a per-deal legal service, not a scalable platform feature.
- **Route A is not merely the recommended route; it is close to the only lawful one at our size.** This strengthens §1.5 risk 2 and §14.1 R3.
- The §9.5 legal budget line "Payments/escrow consultation, MAD 15,000–40,000" is now clearly necessary rather than precautionary.

#### Still `[ASSUMPTION]` — needs the lawyer (RATING D)

- Whether a **payment-orchestration** model (we never touch funds; the licensed PSP holds and releases on our API instruction) falls outside Article 18 entirely. This is the actual architecture question and it is a legal judgement, not a research finding.
- Whether the notary/lawyer escrow route can be structured to be repeatable without us performing an Article 16 operation.
- Minimum capital under Circular 20/G/2006 as modified — the circular text was not retrievable; secondary sources gave conflicting figures (MAD 3M vs MAD 5M), so **both are excluded from the plan**.
- Whether an agent/distributor arrangement under a licensed PSP's licence is available to a company our size.

**Governing circulars to name in the lawyer meeting** (from Bank Al-Maghrib's licensing page, RATING A):
- **Circular 7/W/2016** (modified by 2/W/2022 and 2/W/2024) — modalities of exercising payment services
- **Circular 6/W/2016** (amended by 1/W/2022) — conditions of application of Article 22
- **Circular 20/G/2006** (modified by 1/G/11 and 8/W/16) — minimum capital
- **Circular 5/W/2015** — documents required for a licensing application

### 1.2 Data protection / CNDP (§9.2) — **RATING A**

Source: CNDP official formalities page.

- Prior **declaration** (`déclaration préalable`) is required for processing not excluded or exempted. Form **F211**. Receipt issued within **24 hours**. **Free.**
- Prior **authorisation** (`autorisation préalable`), form **F112**, is required for sensitive categories — including **national ID numbers** and **file interconnections**. Processing time **2 months**, extendable once.
- **Transfers of data abroad require specific authorisation under Articles 43–44** of Law 09-08.

#### What this changes in the plan

- §9.2 said registration "may be required" — it is required, it is free, and it takes 24 hours. This is a month-1 admin task, not a legal project. Remove the uncertainty.
- **New finding not in the plan at all: Articles 43–44.** §8.1 specifies "Vercel or equivalent" hosting, which means personal data on infrastructure outside Morocco. That is a cross-border transfer requiring CNDP authorisation — a **2-month** process, not 24 hours. This needs to be started early or the hosting decision needs revisiting. It is a genuine dependency between §8.1 and §9.2 that the plan does not currently connect.
- Verification documents may include ID numbers → likely pushes parts of the verification workflow into the **F112 authorisation** regime, not simple declaration. Confirm with counsel.

### 1.3 SARL formation (§9.1) — **RATING B**

Multiple company-formation sources agree:

- **No minimum capital** since Law 24-10 amending Law 5-96. A SARL can be formed with symbolic capital (1 MAD).
- **Cost: MAD 4,500–16,000** excluding share capital. Components cited: OMPIC negative certificate MAD 230; statutes drafting MAD 3,000–6,000; RC registration MAD 350; legal publication MAD 900–1,600; accountant fees MAD 3,000–8,000.
- Registration duties are **exempt** for company-formation instruments.
- **Timeline: 7–15 working days** via a professional; 15–30 days DIY; under a week via the CRI single window with a complete file.
- The **CRI guichet unique** triggers RC registration, tax registration and CNSS affiliation from one form.

**Plan said MAD 5,000–15,000 — essentially correct.** Widen slightly to 4,500–16,000 and add the timeline, which the plan omits. Note these are *company-formation-provider* sources (rating B, commercially motivated); treat the upper end as realistic.

---

## BLOCK 2 — FUNDING

### 2.1 Tamwilcom Startup Venture Building (§13.2) — **RATING A/B, and the plan is materially out of date**

Source: Tamwilcom official site (A) + Wamda, Médias24, Le Desk, TelQuel (B).

**The plan mischaracterises this program's status.** §13.2 describes "Reported ~MAD 700M across ~800 startups over three years" as though it were an established track record. In fact:

- **Officially launched December 2025**, with a further public launch event **13 April 2026**.
- MAD 700M / 800 startups over three years is the program's **forward target**, not its history.
- It is therefore **four months old**. This is much better for you than the plan assumes: you are early to a new instrument rather than late to a crowded one.

**The four instruments, with amounts (RATING A — Tamwilcom's own site, corroborated by press):**

| Instrument | Amount | Nature |
|---|---|---|
| **Bourse de Vie** (living allowance) | Up to **70% of prior 12 months' average gross salary**, ceiling **MAD 40,000/month per founder**, max **12 months** | Non-dilutive stipend |
| **Bourse d'Incubation** | Up to **MAD 200,000** | Grant — prototyping and validation |
| **Prêt d'Honneur** | Up to **MAD 500,000** | Interest-free, unsecured loan — market entry |
| **Prêt d'Amorçage** (seed) | **MAD 500,000 – 2,000,000** | Unsecured loan — growth / first raise |

All described as **non-dilutive**.

**Eligibility (RATING B — needs direct confirmation):**
- Digital startups constituted **within the last 8 years**
- Innovative solution with a **digital component**
- Applications go **through partner operators**, not directly to Tamwilcom

**Operators:** Technopark, CEED Maroc, Flat6Labs, Open Startup International, Renew Capital, 500 Global. Technopark alone is mandated to incubate **240 startups**.

#### What this changes in the plan

This is the single largest correction in this block. §1.4 asks for "~MAD 420,000 (~$41,600) total, of which ~MAD 180,000 is founder living costs."

**The Bourse de Vie alone could cover the entire founder-living-cost line, and likely more.** The plan budgets MAD 15,000/month for two founders combined (§12.1). The Bourse de Vie ceiling is MAD 40,000/month *per founder*. Even at a modest prior salary, 70% of it for 12 months plausibly exceeds the plan's entire personal-burn assumption.

Combined with the Bourse d'Incubation (MAD 200,000, non-dilutive, aimed exactly at the prototype stage §13.1 argues for), **the Phase 0–1 funding requirement of MAD 420,000 may be almost entirely coverable by non-dilutive instruments** — no equity, no bank debt.

**Consequences for the plan:**
- §13.3's timeline (register month 1–2, apply month 3–4, decision month 6–8) is sound and should be *accelerated*. The route is through an operator, so the real first action is contacting Technopark/CEED/Flat6Labs, not preparing a Tamwilcom file.
- **The 8-year-age criterion means registering the SARL early does not disqualify you** — it makes you eligible. This removes the tension §9.1 flags between "no company until funding" and "funding requires a company."
- §12.5's total-to-m24 of MAD 2.1–2.9M should be re-derived after confirming what stacking of instruments is permitted — a question for the operator.
- The Bourse de Vie's salary-history basis is a real constraint worth noting: it rewards founders leaving salaried employment. If either founder has no recent salaried income, that instrument may be worth little to them. **This is a founder-specific question neither of us can answer from here.**

#### Still `[ASSUMPTION]` — needs a direct call (RATING D)

- Whether all four instruments can be **stacked**, and in what sequence
- Whether a B2B marketplace qualifies as "innovative with a digital component" — almost certainly yes, but the operator decides
- Application windows and cohort dates (official portal `tamwilstartups.ma` blocked automated access; **visit it manually**)
- Exact Bourse de Vie eligibility: employment-history requirements, treatment of self-employed or previously unsalaried founders
- Whether taking a Prêt d'Honneur affects later eligibility for the Prêt d'Amorçage

**Action: this is a phone call to Technopark, not more research.** It is the highest-value call in the plan right now and it is not currently a numbered task in §15.1.

### 2.2 Fonds Mohammed VI pour l'Investissement (§13.2) — **RATING B, plan understates specificity**

Sources: FM6I structure page, Médias24, La Vie Éco, Agence Ecofin, EcoActu.

**Two distinct tracks, and the plan conflates them:**

**Sectoral/thematic funds:** **14 management companies** engaged (9 Moroccan incl. CDG Invest Management, BMCE Capital Investments; 5 international incl. AfricInvest, Mediterranea Capital Partners). Cumulative target **≥ MAD 20 billion**. FM6I contributes **up to 33%** of each fund's size. These target established companies' equity strengthening — **not us**.

**Fonds Startups:** **9 management companies preselected at Gitex Africa Morocco 2026 (April 2026)**. Cumulative target **~MAD 2.5 billion**, funded by the Ministry, FM6I, CDG, and third-party local/foreign investors. Explicitly covers **pre-seed → seed → Series A and beyond**.

FM6I overall: MAD 120 billion investment volume targeted over 2023–2026.

#### What this changes in the plan

- §13.2's "~MAD 2.5B pool / managers shortlisted" is **correct but stale on timing** — the shortlist happened in April 2026, four months ago. These funds are standing up *now*.
- The pre-seed coverage matters: the plan assumed FM6I was for a later stage. It is not — but it is **equity**, and §13.5 explicitly rules out raising on a valuation requiring a Phase 2 outcome. **Tamwilcom's non-dilutive instruments remain strictly better for Phase 0–1.** FM6I becomes relevant at Phase 2, which is exactly the sequencing §13.3 already proposes.
- **Do not apply to both in parallel for the same round.** Establish with Tamwilcom's operator whether accepting Startup VB financing constrains later equity raises.

#### Still `[ASSUMPTION]` (RATING D)

- Which 9 managers, their sector mandates, and whether any target B2B/marketplace
- Whether the Fonds Startups are yet deployable or still in formation
- Minimum cheque sizes

---

## BLOCK 4 — MARKET SIZING (§4.1)

### 4.1 Morocco GDP and BTP sector — **RATING A**

Sources: HCP *Budget Économique Prévisionnel 2026* (saved to `research-sources/`), HCP national accounts, FNBTP federation deck.

| Metric | Value | Year | Source |
|---|---|---|---|
| GDP at current prices | **MAD 1,720.2 billion** | 2025 | HCP (vs 1,614.6bn in 2024) |
| GDP growth | **4.9%** | 2025 | HCP (4.4% in 2024) |
| BTP value added | **~MAD 100 billion** (approaching) | 2025 | Médias24 citing HCP |
| BTP share of GDP | **~6%** | 2025 | FNBTP |
| BTP employment | **1.2 million+** | — | FNBTP |
| BTP growth | **~6%** (2025), **4.1%** forecast (2026) | HCP BEP 2026 |
| BTP share of gross fixed capital formation | **55%** | 2021 | FNBTP |

**FNBTP value-added time series, current prices, MAD millions** (from federation deck):
2014: 58,406 → 2015: 60,284 → 64,818 → 67,510 → 66,138 → 66,687 → 64,229 → 67,183 → **72,741**

Note the discrepancy: FNBTP's series tops out ~MAD 72.7bn while 2025 reporting says "approaching MAD 100bn." The FNBTP deck is from 2024 and its series ends earlier. Both are directionally consistent with strong recent growth; **use ~MAD 100bn for 2025 with the caveat, or cite the FNBTP series with its year attached.** Do not blend them.

**A direct quote from HCP worth using** (BEP 2026, on 2025 BTP performance):
> « en liaison notamment avec l'accélération des projets d'infrastructures stratégiques, et ce **malgré les coûts élevés des matériaux de construction** et la persistance de la pénurie de main-d'œuvre qualifiée »

The national statistics agency names **high construction-materials costs** as a sector headwind. This is independent, citable support for §4.4's "rising input-cost volatility increases the value of price transparency" — previously an unsourced trend claim. **This is the single most useful sentence found for the funding narrative.**

Growth drivers named across sources: strategic infrastructure, CAN 2025, World Cup 2030, and the direct housing-aid programme.

#### What this changes in the plan

§4.1's top-down table can now be partly filled:

| Input | Value | Status |
|---|---|---|
| Morocco construction sector annual output (value added) | **~MAD 100bn (2025)** | **VERIFIED — A** |
| Share that is materials procurement | ___% | **STILL UNKNOWN** |
| Share transacted B2B between SMEs | ___% | **STILL UNKNOWN** |

**The two remaining unknowns are the ones that actually determine market size, and neither is published.** Value added ≠ materials spend — value added excludes intermediate consumption, which is precisely where materials sit. Deriving materials procurement from a value-added figure is not arithmetic you can do honestly without an input-output table.

**Recommendation: keep §4.1's top-down table explicitly incomplete.** It is more defensible in front of a funder to say "sector value added is MAD ~100bn per HCP; we have not found published data on materials procurement share, and our plan is built bottom-up" than to publish a derived TAM resting on two invented percentages. §4.1 already says the bottom-up number is the one to plan against — that judgement is now better supported, not worse.

**Next step if you want the top-down number:** HCP publishes input-output tables (*tableaux entrées-sorties*) in the full national accounts report. That would give materials' intermediate consumption in construction properly. It was not retrievable in this session — the data sits behind download links. Worth one manual visit to `hcp.ma/Comptes-nationaux_r338.html`.

---

## BLOCK 5 — COMPETITIVE LANDSCAPE (§5.1) — **the plan has a significant gap**

### 5.1 Direct competitors the plan does not list — **RATING B**

§5.1's table lists Kerix, Telecontact, Procurement.ma, Maroc Business, WhatsApp/brokers, and Alibaba. **Research surfaced a cluster of construction-specific and B2B platforms absent from the plan entirely.**

| Player | What it actually is | Overlap with our plan |
|---|---|---|
| **BTPro** (`btpro.ma`) | Construction project-management SaaS for Moroccan pros. **Live material prices for cement, steel, sand, concrete by city**, with variation alerts and history. Moroccan-compliant invoicing (ICE, 20% VAT). Order tracking quote→delivery. | **HIGH — see below** |
| **MABANI** (`mabani.ma`) | Materials directory (*matériauthèque*) for architects/prescribers. 1,600+ products, 60 categories. Sells **brand visibility** to manufacturers. | Medium — incumbent model, construction-specific |
| **BTP Business Market** | Integrated buying group (*centrale d'achat*) with **own factories**. Sells at "factory prices" via order pooling. Claims 100+ sites supplied, ~20% cost reduction. | Medium — competes for the same buyer, different model |
| **Batimis** | Free Moroccan platform to buy/sell/rent BTP **equipment** | Low — equipment not materials |
| **Business Hub** (`businesshub.ma`) | "L'infrastructure B2B Marocaine" — verified opportunities, business groups | Unknown — site blocked |
| **Evollume**, **Solidaire Market**, **B2B Maroc**, **b2bconnect.ma** | General B2B marketplaces | Low–medium |

### 5.2 BTPro is the finding that matters — **RATING A on pricing**

**BTPro's published pricing:**

| Tier | Price | Includes |
|---|---|---|
| Starter | **Free** | 1 project, 5 orders/month, 1 user |
| Pro | **MAD 499/month** | Unlimited projects/orders, team up to 5 |
| Enterprise | Custom | — |

**Why this is significant:**

1. **Price anchor.** Our proposed Verified tier is **MAD 400/month** (§6.2). BTPro sits at MAD 499 for a buyer-side tool. Our pricing hypothesis is no longer unanchored — there is a live Moroccan construction-tech product at a comparable price point, which is *supportive* evidence that MAD 400–900 is not absurd. It also means suppliers may already be paying for construction software.

2. **They already ship the `/prix/` feature.** §7.3 says the price-benchmark tree "is the one incumbents cannot replicate, because it requires real quote data," and §3.4 says "Kerix can publish listings. It cannot publish 'average lead time for cement in Casablanca, from 340 real quotes.'" **BTPro publishes live cement/steel/sand/concrete prices by city today.** That claim in the plan is now false as written. Their data provenance is unknown (possibly scraped, surveyed, or supplier-reported rather than quote-derived) — but the *page* exists, and a funder or competitor will find it.

3. **Free tier with usage caps → paid conversion** is the same mechanic §6.2 describes as our conversion design. Not novel.

4. **They are buyer-side, we are supply-side.** BTPro manages the contractor's projects and orders. We route RFQs to verified suppliers. That is a real distinction and possibly a **partnership** rather than a war — but it is not the empty field §5.1 implies.

### 5.3 Procurement.ma is mischaracterised in the plan — **RATING B**

§5.1 lists it as "Tender aggregation — public tenders only; not private B2B."

**It self-describes as "N°1 de la mise en relation B2B au Maroc" and "La 1ère plateforme B2B du Maroc."** Its actual model:
- Buyer publishes a purchase request (*free*)
- **AI notifies relevant suppliers**
- Parties discuss directly
- "Conclude **without intermediaries or commissions**"
- Supplier directory spans transport, IT, security, training, audiovisual, maintenance; **BTP & Construction appears as a sector** (construction services; materials coverage unclear)
- Directory runs to **21 pages** of listings; exact count not published

**This is RFQ routing — the core Phase 1 loop in §3.2 — already live in Morocco, for free.**

Their explicit "sans intermédiaire ni commission" positioning is the *opposite* of our thesis, and that is the strategic opening: they route requests and step away; we verify, record outcomes, and eventually carry consequence. But §5.1's "public tenders only" is wrong and must be corrected before this document goes near a funder who will spend ninety seconds on their homepage.

#### What this changes in the plan

- **§5.1's table needs rebuilding.** Adding BTPro, MABANI, BTP Business Market, and reclassifying Procurement.ma.
- **§5.3 "Why we can win" needs revisiting.** The innovator's-dilemma argument was aimed at directories monetising visibility. It does not apply to BTPro (SaaS subscription, no visibility revenue to cannibalise) or to Procurement.ma (free routing, no revenue model visible to protect).
- **§17 blocking question 1 — "has someone already tried this?" — is now partly answered: yes, adjacent attempts exist and are live.** None appear to do verified-identity + transaction record + escrow together, which is still the gap. But "nobody has tried this" is no longer a defensible statement.
- **§3.4 and §7.3's price-data moat claim must be softened.** Ours would be quote-derived and therefore better, but we cannot claim incumbents *cannot* publish price pages when one already does.

#### Still `[ASSUMPTION]` (RATING D)

- BTPro's scale, funding, launch date, and where its price data comes from (dashboard mock showed "34 active suppliers" — mock data, not a scale claim)
- Procurement.ma's actual supplier count, monetisation, and materials depth
- Whether any of these have failed, pivoted, or are dormant — **a live homepage is not a live business**
- Whether Business Hub does verification (site blocked)

**Field task: these are five phone calls.** Ask a supplier in Phase A interviews: "Are you listed on any of these? Did it produce anything?" That answers scale, quality, and willingness-to-pay in one question. **Add the platform names to the Appendix B supplier guide.**

### 5.4 Escrow: nobody has built it, and the reason is regulatory — **RATING B, high strategic value**

Source: Le Matin interviewing compliance expert Houda Khouny and economist Taib Aisse.

Key findings:

- **"Aucun texte spécifique ne régit l'Escrow numérique transactionnel"** — no specific regulation governs digital transactional escrow in Morocco (economist Taib Aisse).
- Bank Al-Maghrib's existing directives **already authorise licensed institutions to collect funds via cantonment mechanisms for payment operations** — described as "déjà une base compatible avec un mécanisme de blocage temporaire des fonds." This aligns with Article 17 found in Block 1.
- Experts are **calling for** BAM to issue a dedicated circular authorising payment institutions to act as escrow agents in e-commerce, and for CMI to build a **conditional-payment API**.
- Open questions flagged by the experts themselves: **escrow agent liability, client-fund cantonment procedures, and maximum blocking periods.**
- **Infrastructure obstacle:** SIMT settlement runs at **J+1 to J+2**, described as incompatible with immediate conditional-payment response.
- **No company is named as attempting escrow in Morocco.**

#### What this changes in the plan

This substantially sharpens §9.3 and §1.5 risk 2:

1. **The moat thesis is confirmed and strengthened.** §16.3 argues the regulatory position is the real barrier. Independent experts publicly state the framework does not yet exist. **If we reach Phase 2 with a working arrangement, the barrier is exactly as high as §16.3 hopes.**

2. **But the timeline risk is worse than §15.4 assumes.** §15.4 schedules escrow live in pilot at **month 18** and generally available at **month 21**. If it requires a BAM circular that does not exist yet, that is not a schedule we control. §14.1 R3 rates escrow-impracticality as "Medium" likelihood — **on this evidence it should be raised.**

3. **A licensed partner already operating under Article 17 cantonment is the only near-term route**, reinforcing Block 1's conclusion. The partner's own licence scope becomes the binding constraint — which is exactly what the month-1–2 PSP conversation in §15.1 must establish. **Sharpen that task: not "will you work with us" but "does your licence permit conditional release on delivery confirmation, and what is your maximum hold period?"**

4. **J+1/J+2 settlement is a product-design input nobody has costed.** If funds take two days to settle, "released on confirmed delivery" has a two-day tail. That affects supplier cash-flow expectations — and supplier cash flow is precisely why they extend informal credit today (§2.1). Worth raising in supplier interviews.

5. **Strategic optionality:** if a circular is genuinely being lobbied for, being a credible, registered, operating Moroccan platform *when it lands* is valuable. That argues for Phase 1 execution speed and for visibility with the regulator and fintech community — not for waiting.

---

---

## BLOCK 6 — CNDP CROSS-BORDER TRANSFER (follow-up for §8.1 hosting) — **RATING A**

Triggered by a founder asking whether a **European VPS** is permissible instead of a Moroccan one. **Answer: yes, very likely, and this downgrades R3c.**

Source: CNDP's own transfer pages, plus secondary reporting of the deliberation.

**The mechanism** `[A — CNDP's own pages]`:

- Art. 43 of Law 09-08 permits transfer only to a state ensuring an adequate level of protection.
- The **adequacy list** is established by **Deliberation 236-2015 (18 Dec 2015)**, amending **Deliberation 465-2013 (6 Sep 2013)**.
- **Transfers to listed countries require no separate authorisation** — they proceed under the existing F211 declaration (or F112 authorisation) already covering the underlying processing.
- **Transfers to unlisted countries require Form F118 authorisation**, decided within **2 months, extendable once**, justified by explicit consent, necessity, an international agreement, or sufficient safeguards (standard contractual clauses / binding corporate rules).
- Prerequisite in all cases: the underlying processing must already be declared or authorised.

**The country list** `[B — secondary reporting of Art. 1 of the deliberation]`:
Germany, Austria, Bulgaria, **Canada**, Cyprus, Denmark, Spain, Estonia, Finland, **France**, Greece, Hungary, **Ireland**, Iceland, Italy, Latvia, Liechtenstein, "and others." EU states are generally treated as adequate given the GDPR.

**Note the rating split.** The *mechanism* is A — it comes from CNDP's own pages. The *country roster* is B — it comes from secondary reporting of a 2015 deliberation that may have been amended. **The plan reflects this split.** Confirm against the deliberation itself (CNDP publishes it for download; +212 537 57 11 24).

**Effect on the plan:**
- §9.2's "⚠️ NEW DEPENDENCY, 2 months on the critical path" is **substantially wrong as first written** and has been corrected. It applies only to unlisted destinations — notably the **US**, which is where the default "Vercel or equivalent" assumption would likely have put the data.
- **R3c downgraded from Medium to Low.**
- The §8.1 hosting question is no longer regulatory-forced. **Morocco and EU are both clean; the US is the expensive option.**
- This is a good example of why the confidence ratings matter: the first pass found Arts. 43–44 and correctly flagged a dependency, but stopping there would have left a scary and misleading item on the critical path.

---

## Corrections to fold in — BLOCK 2 additions

| § | Current text | Correction | Rating |
|---|---|---|---|
| §4.1 | Construction output "MAD ___" | **GDP MAD 1,720.2bn (2025); BTP VA ~MAD 100bn, ~6% of GDP, 1.2M+ employed** | A |
| §4.1 | materials share, B2B SME share | **Still unknown — keep blank, do not derive** | — |
| §4.4 | "rising input-cost volatility" (unsourced) | **HCP BEP 2026 names high materials costs as a 2025 headwind — quotable** | A |
| §5.1 | 6-player table | **Add BTPro, MABANI, BTP Business Market, Batimis, Business Hub** | B |
| §5.1 | Procurement.ma "public tenders only" | **Wrong — free private B2B RFQ routing with AI supplier matching** | B |
| §3.4, §7.3 | Incumbents cannot publish price data | **BTPro publishes live prices by city today — soften claim** | A |
| §6.2 | MAD 400/900 pricing unanchored | **BTPro Pro tier = MAD 499/mo — real market anchor** | A |
| §13.2 | FM6I "managers shortlisted" | **9 startup-fund managers preselected April 2026; ~MAD 2.5bn; pre-seed→Series A** | B |
| §9.3 | Escrow feasibility unknown | **No specific text governs digital escrow; experts lobbying BAM for a circular; Art. 17 cantonment is the compatible base** | B |
| §14.1 R3 | Likelihood "Medium" | **Raise — depends on regulation that does not yet exist** | B |
| §15.4 | Escrow pilot m18, GA m21 | **Not a timeline we control. Flag dependency.** | B |

## New tasks from this block

6. **Add competitor names to Appendix B supplier interview**: "Are you on BTPro / MABANI / Procurement.ma / Kerix? Did it produce a deal?" — answers scale, quality and willingness-to-pay at once
7. **Manually retrieve HCP input-output tables** for materials procurement share (`hcp.ma/Comptes-nationaux_r338.html`)
8. **Reframe the PSP conversation**: ask whether their licence permits conditional release on delivery confirmation, and their maximum hold period
9. **Cost the J+1/J+2 settlement tail** into the Phase 2 product design and raise it in supplier interviews
10. **Assess BTPro as a potential partner, not only a competitor** — they are buyer-side, we are supply-side

## Sources — Block 2

- [HCP — Budget Économique Prévisionnel 2026](https://www.hcp.ma/file/246629/) — saved locally
- [HCP — Situation économique nationale en 2025](https://www.hcp.ma/Situation-economique-nationale-en-2025_a4317.html)
- [HCP — Comptes nationaux](https://www.hcp.ma/Comptes-nationaux_r338.html)
- [FNBTP — Le Secteur du BTP au Maroc](https://fnbtp.ma/wp-content/uploads/2024/06/C1-4-Kabbaj.pdf) — saved locally
- [Médias24 — PIB nominal marocain 2025](https://medias24.com/2026/06/25/le-pib-nominal-marocain-frole-les-190-milliards-de-dollars-en-2025-1708289/)
- [Médias24 — BTP marocain, un marché qui a changé d'échelle](https://medias24.com/2025/11/23/btp-marocain-un-marche-qui-a-change-dechelle-sous-leffet-des-investissements-publics-et-prives-1582113/)
- [Médias24 — Neuf sociétés de gestion préselectionnées, fonds de 2,5 MMDH](https://medias24.com/2026/04/10/startups-neuf-societes-de-gestion-preselectionnees-pour-piloter-des-fonds-de-25-mmdh-1657717)
- [FM6I — Structure](https://www.fm6i.ma/fr/structure)
- [Agence Ecofin — FM6I engage 14 gestionnaires](https://www.agenceecofin.com/actualites/1507-130088-maroc-le-fonds-mohammed-vi-pour-l-investissement-engage-14-gestionnaires-de-fonds-sectoriels)
- [Le Matin — E-commerce : le Maroc peut-il créer son propre «PayPal» ?](https://lematin.ma/societe/e-commerce-le-maroc-peut-il-creer-son-propre-paypal/346218)
- [BTPro](https://btpro.ma/) · [MABANI](https://mabani.ma/) · [BTP Business Market](https://btpbusinessmarket.com/) · [Procurement.ma](https://procurement.ma/) · [Procurement.ma suppliers](https://procurement.ma/fournisseurs) · [Batimis](https://batimis.com/fr/) · [Tachrone](https://tachrone.ma/)

---

## BLOCK 3 — BASELINE NUMBERS

### 3.1 USD/MAD exchange rate (§ "How to read this document") — **RATING B, and the plan is wrong**

- **Plan states:** 1 USD ≈ 10.1 MAD
- **Actual, 13 August 2026:** 1 USD ≈ **9.30 MAD** (Wise mid-market 9.304; exchange-rates.org 9.3002 — two independent sources agreeing)
- 2026 range so far: ~9.13–9.34; 2026 average ~9.16

**The plan overstates MAD/USD by ~8.6%**, meaning every USD figure in the document is understated. Corrections:

| Plan figure | Plan's USD | Corrected USD |
|---|---|---|
| MAD 420,000 (§1.4) | $41,600 | **~$45,200** |
| MAD ~400,000 (§12.1) | $39,600 | **~$43,000** |
| MAD 2.1M–2.9M (§12.5) | $210k–290k | **~$226k–312k** |

Low materiality internally — you operate in MAD — but §7.4 and §13 target funders, and a document with a stale FX rate in its conventions section invites doubt about everything else. Fix it, and consider dropping USD conversions entirely except where a funder needs them.

### 3.2 Kerix scale (§5.1) — **RATING C, and the plan overstates it ~5×**

- **Plan states:** "~150k listings `[verify]`"
- **Found:** "over **30,000** Moroccan companies"; platform claims **500,000+ monthly visitors** across Kerix and satellite sites
- Basic listing and consultation are described as **free**; premium/pack pricing is **not published**

Rating C — this comes from directory-aggregator and third-party pages, not Kerix's own about page (their site blocked automated access). But 30k and 150k are far enough apart that the plan's figure should not stand.

**What this changes:** a 30,000-company *general* directory is a much smaller and shallower incumbent than a 150,000-listing one. The construction-materials subset of 30k national listings may be in the low hundreds — which makes §4.1's bottom-up supplier count (the plan proposes counting from Kerix) both more tractable and possibly thin as a sole source. It also makes §5.3's "decade of domain authority" a smaller moat than assumed.

**Still needed (RATING D):** Kerix's actual paid pricing. Not published — §18 Appendix B question 2 ("what do you currently pay for visibility?") is the way to get it. **This is a field question, not a research question.**

---

## Summary of corrections to fold into BUSINESS-PLAN.md

| § | Current text | Correction | Rating |
|---|---|---|---|
| Header | 1 USD ≈ 10.1 MAD | **9.30** | B |
| §5.1 | Kerix ~150k listings | **~30,000 companies**; 500k monthly visitors | C |
| §9.1 | Registration MAD 5,000–15,000 | **4,500–16,000**, no minimum capital, 7–15 working days via CRI | B |
| §9.2 | CNDP registration "may be required" | **Required**, form F211, free, 24h receipt | A |
| §9.2 | *(absent)* | **NEW: Arts 43–44 — offshore hosting needs separate authorisation, ~2 months** | A |
| §9.3 | Escrow "regulated `[verify]`" | **Confirmed: Arts 15/16/18; penalty Art 183 = 6mo–3yr + MAD 100k–5M** | A |
| §9.3 | Route B as manual fallback | **Likely still caught by Art 18 if we hold funds. Reframe.** | A |
| §13.2 | Tamwilcom "reported ~700M/800 startups" | **Launched Dec 2025; 700M/800 is a forward target. Four instruments with specific amounts.** | A |
| §13.2 | *(absent)* | **NEW: Bourse de Vie up to MAD 40k/month/founder for 12 months** | A |
| §1.4 | ~MAD 420,000 needed | **Potentially largely covered by non-dilutive Tamwilcom instruments** | A |

## New tasks this research generated (not currently in §15.1)

1. **Call Technopark / CEED / Flat6Labs** about Startup VB eligibility and stacking — highest-value call available right now
2. **Visit `tamwilstartups.ma` manually** — blocked to automated access, holds the authoritative criteria
3. **Add CNDP Art 43–44 cross-border authorisation to the critical path** — 2-month lead time, gates the §8.1 hosting choice
4. **Reframe the §9.3 Route B question for the lawyer**: not "can we hold funds in a segregated account" but "can we orchestrate a licensed PSP without performing an Art. 16 operation ourselves"
5. **Retrieve Circular 20/G/2006** for current minimum capital — not retrievable online, ask the lawyer or BAM directly

---

## Sources

- [Law 103-12 full text (Bank Al-Maghrib)](https://www.bkam.ma/en/content/download/757666/8545663/loi%20bancaire%20fr%2022.pdf) — saved locally
- [Bank Al-Maghrib — Conditions d'exercice (Agrément)](https://www.bkam.ma/Trouvez-l-information-concernant/Reglementation/Activite-des-etablissements-de-credit-et-assimiles/Conditions-d-exercice-agrement)
- [Bank Al-Maghrib — Legal framework of payment systems](https://www.bkam.ma/en/Find-information-about/Regulation/Legal-framework-of-payment-systems-and-means)
- [CNDP — Formalités](https://www.cndp.ma/formalites/)
- [Tamwilcom](https://www.tamwilcom.ma/)
- [Tamwilcom Startups portal](https://www.tamwilstartups.ma/) — blocked to automated access, visit manually
- [Wamda — Tamwilcom launches $69M venture-building programme](https://www.wamda.com/2026/04/tamwilcom-launches-69m-venture-building-programme-support-800-moroccan-startups)
- [Médias24 — Lancement officiel de l'offre Startup Venture Building](https://medias24.com/2025/12/18/lancement-officiel-de-loffre-startup-venture-building-1598956/)
- [Le Desk — Startup Venture Building, programme à 700 MDH](https://ledesk.ma/2026/04/07/startup-venture-building-avec-son-programme-a-700-mdh-tamwilcom-structure-le-parcours-pour-les-startups/)
- [Wise — USD/MAD](https://wise.com/gb/currency-converter/usd-to-mad-rate)
- [exchange-rates.org — USD/MAD 2026](https://www.exchange-rates.org/exchange-rate-history/usd-mad-2026)
- [Kerix](https://www.kerix.net/en/)
- SARL formation costs: [Upsilon Consulting](https://www.upsilon-consulting.com/en/llc-creation-cost-morocco-2026/), [Nexora](https://nexora-expertise.ma/articles/creer-sarl-maroc-2026-guide-complet-etapes-cout-capital-ompic-dgi), [LegalPlus](https://legalplus.ma/creation-sarl-maroc/)
