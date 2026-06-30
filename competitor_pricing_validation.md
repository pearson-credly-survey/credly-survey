# Competitor Pricing Validation

## Scope

This note consolidates the competitor pricing signals I could validate from public web sources and the two pricing workbooks already in the workspace. The goal is comparability first, not exact feature parity.

Current assessment scope:
- Personas: Higher Ed & Associations, Product Certification Providers, SMBs, Training Providers, Enterprises
- Market: United States only
- Segment: Scale business only
- Exclusion: high-volume deals should not be forced into standardized pricing

## What looks reliable

| Vendor | Public pricing signal | Model | Confidence | Notes |
| --- | --- | --- | --- | --- |
| Accredible | Launch starts at $45/month on an annual commitment; 50 recipients to get started | Recipient-based | High | Public pricing page explicitly says pricing is by recipients, not credentials, and there are no setup or maintenance fees on listed plans. |
| Certifier | Starter $0, Professional $67/month billed annually, Advanced $339/month | Mostly plan-based / tiered | High | Public pricing is clear and includes onboarding for subscriptions above $200/month. |
| Sertifier | Free $0/year, Pro $250/year, Enterprise custom | Plan-based / annual | High | Public pricing page is explicit; annual plans include two months free. |
| Certopus | Free Starter $0, Professional public pricing surfaced inconsistently, Enterprise custom | Credential-based | Medium | Public signals are usable, but search snippets conflicted on the Professional tier. Treat the exact number as needing one more direct page capture. |
| Virtualbadge.io | Lite $26/month billed yearly, Growth $49/month billed yearly, Plus $75/month billed yearly | Plan-based / credit-based | High | Public pricing is visible and the page uses credits; unused credits do not roll over. |
| Give My Certificate | Public free-plus-paid plans; third-party sources show $12 to $54 and custom enterprise | Plan-based / mixed | Medium | Public page shows free and paid plans but no clean numeric plan table in the fetched page. Third-party pricing directories show ranges only. |
| BadgeCert | Starter $49.95/month up to 200 annual badge issuances; Bronze $99.95, Silver $149.95, Gold $249.95; Enterprise custom | Issuance-based | Medium | Pricing surfaced in search snippets and appears public, but should still be confirmed directly from the vendor page before using in a final benchmark. |
| Instructure / Canvas Credentials | No clear US public list price on vendor pages; third-party and framework references indicate quote-led/per-user contracting | Per-user enterprise contracting | Low | Treat as quote-heavy in US comparisons. One external benchmark signal cites about GBP 2.94 per user/year plus one-time setup fee (regional/public-sector context, not a universal US list price). |
| Credly | No public list pricing | Quote-only | High | Search results and vendor pages indicate pricing is quote-based. Public web sources mention annual costs often around $3,000 to $20,000, but that should be treated as directional only. |

## How the models differ

The main comparison problem is that these vendors do not price the same thing.

Some are recipient-based, some are credential- or credit-based, and some bundle onboarding, support, or integrations differently. That means a raw monthly sticker price is not comparable on its own. For example, a platform that charges by recipients can look cheaper than a credential-based platform at low usage, then flip at higher issuance volume. A quote-only vendor can also look expensive simply because onboarding and support are bundled into the quote.

## Recommended comparable scenario

Use one standard scenario for the chart and one stress test.

Primary scenario:
- 1,000 active recipients per year
- 1 credential per recipient per year
- 1 admin user
- standard badge/certificate issuance workflow
- no custom integration work
- one onboarding event in year 1
- support included where the vendor normally bundles it
- only standardize pricing for the US scale-business range
- keep high-volume enterprise deals as separate quote-driven exceptions

Why this works:
- It is simple enough to compare across recipient-based and credential-based models.
- It is large enough to avoid pure free-plan noise.
- It is still small enough to stay within the realistic SMB / lower mid-market bracket.

Stress test scenario:
- 5,000 active recipients per year
- 1.5 credentials per recipient per year, or 7,500 total credentials for credential-based vendors
- include an integration assumption if the vendor normally monetizes API or setup separately

## How to normalize pricing

For the chart, calculate an effective annual cost and then divide by the standard unit:

- recipient-based vendors: annual platform cost + onboarding + required add-ons, divided by recipients
- credential-based vendors: annual platform cost + onboarding + required add-ons, divided by credentials
- quote-only vendors: use the best validated external estimate, but flag it as low confidence unless the vendor confirms it directly

For Credly, keep onboarding separate in the comparison so the platform does not appear cheaper than it really is at year 1.

## Practical takeaway

The public market splits into three rough bands:
- low-friction self-serve tools below about $75/month
- mid-tier tools around $45 to $339/month with clearer plan structure
- quote-only enterprise platforms where onboarding and support can materially change year-1 cost

That makes a price/value chart useful only if it plots a normalized annual cost for the same scenario and shows confidence alongside the point estimate.

## Suggested next step

Build a small comparison table with columns for vendor, pricing model, public price, onboarding fee, unit basis, normalized annual cost, and confidence. Then plot the vendors against the value score on the x-axis and the normalized annual cost on the y-axis.