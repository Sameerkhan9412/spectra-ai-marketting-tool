# Product requirements (draft for approval)
## 1. Purpose and scope
One internal workspace for Spectra Technologies, three source websites, four official social identities (one per platform), organic and paid marketing. ZIU drives product sales, SpectraCloud drives service enquiries/subscriptions, Spectra India drives enterprise enquiries. These goals are proposed; verify product data and actual conversion paths. No separate public identities. A content piece is distinct from its platform-specific publication; 14 pieces can yield up to 56 publications, not a guarantee. Videos initially use templates with verified assets; 30 seconds is a planning default. Allow 12 image posts and 2 videos per monthly calendar, configurable; track actual generation attempts separately from accepted pieces.
## 2. Actors and authorization
Admin: manage members, settings, source connections, social accounts, provider budgets, kill switches. Marketing manager: plan content, prepare campaigns and request approvals. Editor: create/modify drafts, never launch ads. Approver: approve exact content or ad revision; ad financial authority is a separate explicit permission. Analyst: read reports; export authorized data. All roles scoped to organization. Deny by default; no self-approval for paid campaigns unless an explicitly approved exception. Re-authenticate for sensitive connection/spend operations. Service workers use scoped identities and policy checks.
## 3. Requirements and acceptance criteria
| ID | Priority | Requirement / observable acceptance |
|---|---|---|
| SRC-01 | Must | Configure the three approved sources; run manual/scheduled read-only sync; show last successful sync, record counts, failures and changes. |
| SRC-02 | Must | Prefer read API/feed/webhooks; fallback sitemap/crawler. Never assume the websites have these APIs. Same external ID/version is idempotent. |
| SRC-03 | Must | Normalize product/service records with source URL, SKU/ID, title, availability, price/currency if valid, specifications, category, provenance, updated time and marketing permission. Duplicate matches require review if ambiguous. |
| SRC-04 | Must | New or changed product creates marketing opportunity, not immediate external publication. Out-of-stock/stale/removed facts block affected claims. |
| KB-01 | Must | Search approved public/marketing knowledge only; evidence records link exact claims to source version. Confidential documents excluded by default. |
| BR-01 | Must | Upload approved logos, palettes, fonts, real product assets and licenses. One parent brand; optional authorized secondary labels. |
| PLAN-01 | Must | Monthly plan honors quotas, source priorities, recent promotion, business goals, event triggers and calendar conflicts; manual override audited. |
| GEN-01 | Must | Generate platform-specific copy, CTA, hashtags, accessibility alt text, evidence and destination URL. Never invent specs, testimonials, offers or price. |
| GEN-02 | Must | Produce branded image from real product assets plus templates/background; preview aspect ratios and validate safe zones. |
| GEN-03 | Must | Render 2 template videos with editable script, storyboard, subtitles, licensed audio and approved product imagery; premium video optional. |
| REV-01 | Must | Draft/review/reject/approve exact immutable revision; edits invalidate prior approval; compare changes and show source evidence. |
| SOC-01 | Must | Connect one company account per platform using authorized OAuth/official APIs; verify identity, scopes, health and expiry. |
| PUB-01 | Must | Schedule UTC with IST display, platform-specific validation and eligibility; preview; cancel before dispatch; track each destination independently. |
| PUB-02 | Must | No duplicate publishing on retries; reconcile uncertain outcomes before retrying; expose provider IDs and errors. |
| PUB-03 | Should | Opt-in organic autopilot for approved categories, exact policy/time/budget/account bounds; sensitive claims always reviewed; pause switch. |
| ADS-01 | Must | Connect company Meta ad account and verified Page/Instagram identity; select eligible existing post or new creative. |
| ADS-02 | Must | Draft campaign/ad set/ad, objective, allowed audience, placement, destination, schedule, budget, currency and creative; validate provider compatibility. |
| ADS-03 | Must | Create paused remote objects only after authorization; activate only with explicit approval bound to exact config and spend; track review/rejection/delivery. |
| ADS-04 | Must | Lifetime and monthly spend caps, reservations, budget reconciliation, pause and emergency stop; increases require fresh approval. |
| ADS-05 | Should | Recommend boosting using organic metrics and compare against baseline; recommend changes, never automatically increase spend in pilot. |
| ANA-01 | Must | Track posts, reach, impressions, engagement, clicks, spend, CPC/CPL/CPA/ROAS where supported. Missing metrics show unavailable, not zero. |
| ANA-02 | Should | UTM conventions and website conversion setup; purchases, service subscriptions and inquiries tracked separately, attribution limitations shown. |
| COST-01 | Must | Record usage per generation attempt, provider/model, asset, job, currency and estimate vs actual; reserve budgets atomically. |
| OPS-01 | Must | Audit approvals, sync, user changes, token updates, external requests and pause events; notify failures without secrets. |
| SaaS-01 | Future | Tenant isolation, onboarding, entitlements, billing, quotas, agency roles and provider review; no billing in internal pilot. |
## 4. Business rules
- Use approved deep links; no claim of clickable Instagram caption URLs. Provide platform-appropriate calls to action and permitted link surfaces.
- Initial illustrative allocation 5 ZIU, 4 SpectraCloud, 3 Spectra India images; rotate videos; manager may override. No fixed priority assumed.
- Price, inventory, offer expiry and licensed assets revalidated shortly before publishing; reject stale facts per configured freshness. Do not publish placeholder content.
- Ads and organic content have distinct approvals and budgets. Meta review may delay or reject ads. Daily budgets are not hard daily spending limits. Use lifetime/account controls where eligible and disclose lag/overshoot risk.
- Pause local scheduling immediately; remote pause confirmation is separate. Published content is not automatically erased. No guarantee of stop on provider outage.
## 5. Nonfunctional and outcomes
Propose measurable p95 dashboard/API latency, ingestion freshness, scheduler lateness, uptime, recovery, cost and concurrency targets after baseline. Security, accessibility, evidence coverage for factual claims, zero unauthorized spend and duplicate prevention are release gates. Measure human editing time, approved-content ratio, cost per accepted asset and downstream outcomes; no guaranteed marketing performance.
## 6. Exclusions and decisions
No public signup, subscriptions, payments, competitor scraping bypasses, automated DMs/comments, checkout changes, or live ad autopilot in pilot. Confirm actual company account ownership, access scopes, brand kit, CMS/API integrations, privacy consent, objectives, money limits, ad account currency, domain, hosting, team roles, expected load, retention and recovery targets before corresponding work. All provider availability/prices must be verified before implementation.
