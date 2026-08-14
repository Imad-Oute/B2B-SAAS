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

**Navigation:** [← Overview](00-overview.md) · [← 8. Product and technology plan](08-product-and-technology.md) · [10. Operations →](10-operations.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
