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

**Navigation:** [← Overview](00-overview.md) · [← 5. Competitive landscape](05-competitive-landscape.md) · [7. Go-to-market strategy →](07-go-to-market.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
