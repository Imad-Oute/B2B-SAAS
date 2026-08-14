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

**Navigation:** [← Overview](00-overview.md) · [← 13. Funding strategy](13-funding-strategy.md) · [15. Milestones and decision gates →](15-milestones-and-gates.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
