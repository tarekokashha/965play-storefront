# The audit and roadmap

How 965play was audited, how the findings were labelled, and what was shipped from them. Audit and roadmap by [Tarek Okasha](https://github.com/tarekokashha), written in **August 2026**.

## Scope

A review of the live storefront, an authenticated review of the WordPress and WooCommerce administration, the audits that had already been supplied, and a light review of the Kuwait market. The goal was stated at the top of the document: **increase completed orders, trust, speed, discoverability and operating reliability without creating unsafe production changes.**

## The method: say how sure you are

Every finding carries one of three evidence labels, and a reader is told how to read them before the first finding:

| Label | Meaning |
|---|---|
| **LIVE** | Confirmed in the current storefront or administration review |
| **AUDIT** | Supported by a supplied audit, and should be rechecked before a production change |
| **PLAN** | A high-value recommendation that is **not yet implemented** |

The document also says plainly which items are done: only the correction that had actually been released is described as completed, and nothing else is to be presented as finished until it ships. That discipline matters when the audience is a business owner deciding what to spend on.

## The release gate

One rule is marked **non-negotiable**:

> Do not activate a cache, update the theme or WooCommerce, change payment or shipping, or create broad redirects until there is a tested restore point or a staging site.

It is not delay. It protects live orders and makes any change reversible. Every P0 item in the roadmap is written against that gate: *back up, change in a controlled order, test the home page, search, product, cart, checkout, payment, emails and mobile, then monitor for errors.*

## What the audit concluded

The verdict was that the store already had a strong gaming identity and a broad catalogue, and that **the bottleneck was not "more design" but commerce reliability and customer confidence.** The headline findings, in the order of their priority:

| Priority | Finding | What happened |
|---|---|---|
| P0 | Shipping was enabled but the active zone had no usable delivery method, which can block a physical order at checkout | Roadmapped. The related checkout delivery work shipped the same day: see [delivery-and-checkout.md](delivery-and-checkout.md) |
| P0 | No page cache was active, so category and product pages were slower than they needed to be on mobile | Roadmapped behind the release gate, with the dynamic WooCommerce routes excluded |
| P0 | Invalid markup had ended up in the theme's custom JavaScript and caused a storefront syntax error | **Fixed**: the invalid code was removed and the syntax error eliminated |
| P0 | A carousel configuration produced a loop warning | Roadmapped: identify the exact carousel, never change every slider globally |
| P0 | A 404 monitor listed 27 URLs that were wasting search value and paid visits | Roadmapped: map each valuable URL to a real replacement, **never mass-redirect to the homepage** |
| P1 | Delivery, warranty, returns, support and reviews were not visible near the purchase action | Partly addressed: delivery clarity by the checkout work, expert help on PC pages by [pc-expert-button.md](pc-expert-button.md) |
| P1 | Search structure was weak: the homepage heading hierarchy, metadata and Open Graph, alt text and Arabic copy | Roadmapped |

## The rules the roadmap held itself to

- **Only publish approved facts.** A trust block near the buy button carries delivery, warranty and returns facts that the business has actually approved.
- **Never fabricate reviews.** Enable verified-purchase reviews and ask for them after purchase.
- **No stock claims the inventory cannot back.** "In stock", "limited stock", "pre-order" and "instant digital delivery" appear only when inventory rules support them.
- **Do not claim volume without data.** Keyword clusters are listed without made-up search volumes, until an SEO tool provides them.
- **One change at a time on production.** Prefer additive changes with a rollback.

## The second document: a growth and SEO audit

A companion audit looked at search and growth, and is organised as an executive assessment, what is already working, confirmed critical issues, an SEO audit with on-page findings and recommended homepage metadata, a keyword and content opportunity map with content clusters to build, a conversion and UX roadmap, a technical, accessibility and security checklist, a competitor benchmark framed as **what to learn, not copy**, and a prioritised action plan for this week, this month and this quarter, with measurement targets.

## What was shipped

| Date | Change |
|---|---|
| 11 August 2026 | The invalid code removed from the theme's custom JavaScript, eliminating the confirmed syntax error |
| 11 August 2026 | City-aware delivery and server-side validation at checkout. See [delivery-and-checkout.md](delivery-and-checkout.md) |
| 11 August 2026 | The pre-sales PC-expert button. See [pc-expert-button.md](pc-expert-button.md) |

## Why publish this

An audit is only useful if it can be acted on and trusted. Labelling evidence, separating done from planned, and stating the release gate in the first screen are how an audit stays honest about what it knows and what it recommends.
