# UI/UX specification
## Design principles
One Spectra workspace, no brand switch between three sources; source filter is informational. Approved company logo/colors pending; prototype neutral palette, consistent tokens, readable typography, minimal animation. Desktop-first operational density while supporting mobile width 360px; accessibility WCAG 2.2 AA target, keyboard/focus, text equivalents, reduced motion, semantic tables and form errors. No invented live metrics; mark sample data and unavailable values.
## Navigation and screens
| Screen | Main content / interactions |
|---|---|
| Dashboard | Monthly target 12/2, approved/scheduled/published counts, failed jobs, source sync health, spend vs approved caps, alerts; distinct organic/paid cards; source/time filters |
| Sources | Three source cards, read-only connector type, URL, sync now, frequency, change history, last success, errors and review queue |
| Catalog & knowledge | Product/service search, source/category/status filters, version comparison, verified fields, evidence links, public approval flag, duplicate merge review |
| Brand assets | Logo, palette, fonts, licenses, templates, media library, expiry and upload validation |
| Strategy | Monthly plan, quotas, source allocation, objectives, priorities and reasons, drag/reorder alternative keyboard controls |
| Content studio | Generation brief, evidence and claims panel, per-platform tabs, CTA/deep link, image preview, edit/regenerate, cost estimate, history and draft state |
| Video studio | Storyboard, script, scenes, voice/subtitles, rights, aspect ratio, render progress, preview and export |
| Calendar | Month/week/list, IST display, source and platform filters, slot conflicts, revision status, schedule/reschedule/cancel, accessibility-friendly list |
| Approvals | Side-by-side revision, claims, brand warnings, audience/budget, approver, reject reason, exact version approval, expiry/revocation |
| Social accounts | Four platform cards, verified identity, scopes/capabilities, expiry and health, connect/reconnect/disconnect; no token display |
| Publishing history | Per-platform intents, remote IDs/links, retryable vs terminal/unknown status, reconciliation controls, timestamps and sanitized failure reason |
| Meta Ads | Campaign list, boost existing eligible post or create new creative, objective, audience, placements, schedule, budget, forecast only if provider-backed, approval, review state, pause and remote confirmation |
| Analytics | Organic vs paid, source/campaign filters, metrics with date/window/currency/freshness, unavailable data explanation, export |
| Costs | AI attempts and actual cost vs estimates, generation quota, ad spend ledger and reservations, warnings and caps |
| Settings & audit | Members/RBAC, model/alias settings, automation policies, timezone, source frequency, flags, budgets, kill switches, append-only activity history |
## Key journeys
New content: source sync → select approved item → generate → check evidence/preview → edit → submit review → approve exact revision → schedule → publish → inspect status. Editing approved content makes a new draft and surfaces schedule conflict; never silently publish unapproved changes.
Boost: choose published post → eligibility check → campaign wizard (objective, destination, audience, placement, date, budget, preview) → review with explicit total and currency → approver confirms → create paused remote objects → activate authorized config → display review and delivery separately. Pause button confirms remote state rather than optimistic success. Missing permission gives reconnect or help, not a fake success.
Autopilot: disabled by default. Configure approved categories, platforms, monthly counts, time window, budget, owner and expiry; show manual exception rules and stop button. Paid automation remains recommendation-only in pilot.
## Required states and interaction
Every screen has loading, empty, error, unauthorized, disabled, stale and success cases. Jobs show queued/running/failed/unknown, cancellation availability, bounded retry and reconciliation. No irreversible action on page load. Show confirmation for live publishing, ads activation, budget increases, account unlink, destructive action; explain effect and approval scope. Never show raw provider stack traces or tokens. Mobile review/approval works without horizontal-only workflows; tables may use labeled scroll or responsive cards. Test 360px, tablet and desktop and actual browser screenshots during phase 3; color contrast and screen-reader testing. Provide design tokens, reusable components and approved wireframes before implementation.
