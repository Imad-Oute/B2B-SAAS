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

**Navigation:** [← Overview](00-overview.md) · [← 7. Go-to-market strategy](07-go-to-market.md) · [9. Regulatory and legal →](09-regulatory-and-legal.md)

*Section of the Moroccan B2B Trade Platform business plan. The canonical single-file version is [`../BUSINESS-PLAN.md`](../BUSINESS-PLAN.md) (v0.3); research findings and sources are in [`../RESEARCH-LOG.md`](../RESEARCH-LOG.md).*
