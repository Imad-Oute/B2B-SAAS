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

#### 7.1.1 Two sequencing errors worth naming explicitly

**Added in 0.4 because both are natural instincts and both are expensive.**

**Error 1 — treating Phase A as sales.** The temptation is to cold-call a list and sign suppliers up before anything is built. Phase A conversations are **interviews, not pitches**, and the distinction is not pedantry. Appendix B ends with the rule: *"do not pitch during these interviews. Ask, record, shut up."* A supplier who is polite about the idea tells us nothing; a supplier describing a real loss tells us everything. Gate 0 requires ≥6 of 10 buyers to describe a recourse failure **unprompted** — a criterion that a pitch call structurally cannot satisfy, because once you have described the product you have contaminated every answer that follows.

Phase A still builds the list. It just builds it by listening, and it returns something a sales call never would: **the words suppliers actually use for their own categories**, which §8.2 identifies as the hardest part of the build and the thing every SEO URL and RFQ route depends on.

**Error 2 — "onboard suppliers before we build."** You cannot onboard anyone onto nothing. What Phase B does instead is **concierge onboarding**: we build the supplier's profile *for* them from materials they already have — their catalogue, their letterhead, their existing listing. Nobody fills in a form. That still requires the product to exist at a basic level. The honest sequence is **interview → build → hand-recruit onto a free tier**, with recruitment overlapping the back half of the build, not preceding it.

What *can* legitimately happen before launch is a **waiting list**: at the end of a Phase A interview, "we're building this, can I come back to you when there's something to show?" That is a warm re-contact list, and it is the single highest-converting input to Phase B. It is not the same as onboarding.

### 7.1.2 The three channels, and why there are three rather than two

**Restructured in 0.4.** The natural reading of this plan is that there are two acquisition channels: cold outreach to build supply, and SEO to bring demand. **That model has a hole in it that maps exactly onto R4, the risk §14.2 calls "the quiet one."**

Both cold outreach and field sales are **supply-side**. SEO, once it works, is mostly **demand-side**. But SEO takes 6–12 months to produce meaningful traffic, and §12.2 projects no paying supplier until month 9. So the two-channel model leaves months ~6–12 with suppliers onboarded, verified, waiting — **and almost no buyer demand reaching them.**

That is precisely how R4 kills the business: suppliers churn at month six because the leads never came, LTV collapses below 2:1, and the dashboard looks healthy right until it doesn't. **A third channel exists specifically to bridge that gap.**

| | Channel | Target | Active | Purpose |
|---|---|---|---|---|
| **CH1** | Supplier outbound — field visits, phone, associations, fairs | Suppliers | m1–8, then tapering | Solve cold start. Get to 100 verified |
| **CH2** | **Buyer outbound — direct to contractors** | **Buyers** | **m6–14** | **The bridge. Manufacture demand while SEO matures** |
| **CH3** | SEO and organic content | Both, mostly buyers | m9+, compounding | The long-run engine. Where CAC drops |

**CH2 is not optional and it is not a smaller version of CH1.** It exists because the marketplace has to be liquid *before* the growth engine works, and the only way to make it liquid in months 6–12 is for a founder to personally generate demand. §7.1 Phase C already says this — "direct outbound to buyers, manual RFQ routing, a founder can be the routing engine for the first fifty requests" — but it is easy to read past. It is stated here as a channel with its own owner, targets and budget so it cannot be quietly dropped.

**The sequencing:**

```
m1-2    m3-6      m6-8       m8-12        m12-14      m14+
CH1 ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░  tapers as inbound takes over
CH2               ░░░░████████████████████████░░░  the bridge — heaviest m8-12
CH3                     ░░░░░░████████████████████  compounds, never stops
                              ↑
                    first organic RFQs ~m9-10
                    meaningful traffic ~m12
```

**The handoff test.** CH2 has done its job when inbound RFQs from CH3 exceed founder-generated RFQs from CH2 for three consecutive months. Until that happens, CH2 stays funded and staffed. **Do not taper CH2 on a calendar date — taper it on that metric.**

Detailed playbooks for all three channels, including scripts, list-building method, sequences and weekly targets, are in **[19 — Acquisition playbook](19-acquisition-playbook.md)**.

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

### 7.3 Buyer acquisition — outbound first, SEO second

**Restructured in 0.4.** v0.3 treated buyer acquisition as an SEO section with outbound mentioned in a closing line. That ordering is backwards for the first year: **SEO cannot deliver buyers when we need them most.** This subsection now covers CH2 (buyer outbound) first, then CH3 (SEO), in the order they actually matter.

#### 7.3.1 CH2 — Buyer outbound, the bridge channel (months 6–14)

**Why this exists:** between soft launch (~m6) and meaningful organic traffic (~m12) there is a six-month window where we have supply and no demand. Every week a verified supplier sits on the platform without receiving an enquiry is a week closer to churn. **This channel manufactures the demand that keeps early suppliers alive.**

**Who we target:** SME contractors and construction firms, 5–50 employees (§4.2) — large enough to have real procurement volume, small enough to lack a formal procurement department or framework agreements with incumbent suppliers.

**The asymmetry that makes this work:** we are not asking buyers to adopt software. We are asking them to describe one thing they need to buy, which we then route by hand. **The buyer's cost of trying us is one phone call or one email, and the output is competing quotes they did not have to chase.** That is a materially easier sell than any supplier-side pitch, and it is why manual routing (§7.1 Phase C) is a feature rather than a stopgap.

**Sources for the buyer list:**
1. **Suppliers we have already onboarded** — the most underrated source in the plan. Ask every onboarded supplier: *"which buyers do you wish would find you?"* They know the market, and a warm mention converts far better than a cold approach.
2. Public tender databases and awarded-contract records — firms winning public works are actively buying materials
3. Construction and real-estate developer listings, project announcements in sector press
4. Trade associations and sector bodies `[ASSUMPTION — identify the relevant bodies]`
5. LinkedIn for procurement and *achats* roles at mid-size firms
6. Physical proximity — active sites in the launch region are visible from the road

**What we ask for:** not a signup. **One real RFQ.** The conversion event for CH2 is a buyer telling us what they need, which a founder then routes manually to matching verified suppliers.

**Manual routing is deliberate, not a limitation.** The first fifty routings are how the matching logic gets designed (§7.1 Phase C) — which categories actually cluster, what a "region" means in practice for delivery, how buyers describe specs versus how suppliers describe stock. **Automating before walking that path builds the wrong matcher.** §8.4 principle 1 applies exactly here.

**Targets:** see the [acquisition playbook](19-acquisition-playbook.md). Headline: **80 RFQs/month by m12** (§10.4), of which the majority in m6–10 will be CH2-generated rather than organic.

#### 7.3.2 CH3 — The SEO engine (months 9+)

SEO is the primary **long-run** channel and the reason CAC eventually drops. The argument from the brief holds: French-language B2B search intent is high, paid acquisition is expensive relative to deal size, and incumbent traffic proves the demand.

**What it cannot do is rescue year one.** Programmatic pages need supply to be populated before they are worth indexing, domain authority accrues slowly, and we start with none (§5.3). Plan for first organic RFQs around m9–10 and meaningful volume around m12 — which is exactly why CH2 exists.

**Programmatic page architecture:**

```
/fournisseurs/{secteur}/{ville}                    e.g. /fournisseurs/ciment/casablanca
/fournisseurs/{secteur}/{ville}/{sous-categorie}
/entreprise/{slug}                                  verified supplier profile
/guides/{topic}                                     editorial, buyer-education
/prix/{materiau}/{region}                           price benchmark pages — Phase 2+
```

The `/prix/` tree is the one incumbents cannot replicate, because it requires real quote data. It should be built as soon as we have statistically meaningful volume, and it is a good reason to instrument quote data properly from day one.

**Content that is not programmatic:** buyer-education guides — how to verify a supplier, what a materials contract should specify, how to structure staged payment. This content ranks, builds trust, and pre-sells the referee proposition. **It also does double duty as CH2 collateral:** a genuinely useful guide is a legitimate reason to contact a buyer cold, and a far better opener than a product pitch.

**The two channels feed each other.** Every CH2 conversation reveals the language buyers actually search in, which improves CH3's targeting. Every CH3 page gives CH2 something credible to point at. **Treat them as one buyer-acquisition programme with two time horizons, not as competing budgets.**

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

**Navigation:** [← Overview](00-overview.md) · [← 6. Business model and pricing](06-business-model-and-pricing.md) · [8. Product and technology plan →](08-product-and-technology.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
