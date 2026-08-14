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

**Navigation:** [← Overview](00-overview.md) · [← 4. Market analysis](04-market-analysis.md) · [6. Business model and pricing →](06-business-model-and-pricing.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
