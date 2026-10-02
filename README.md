<div align="center">

<img src="docs/img/social-preview.png" alt="965play: a bilingual gaming and PC storefront on WooCommerce" width="100%">

# 965play

**A bilingual gaming and PC storefront for Kuwait, on WooCommerce.**<br>
Built and documented by [Tarek Okasha](https://github.com/tarekokashha).

[![CI](https://github.com/tarekokashha/965play-storefront/actions/workflows/ci.yml/badge.svg)](https://github.com/tarekokashha/965play-storefront/actions/workflows/ci.yml)
[![Docs: CC BY 4.0](https://img.shields.io/badge/docs-CC%20BY%204.0-lightgrey.svg)](LICENSE)
![WooCommerce](https://img.shields.io/badge/WooCommerce-Woodmart-7f54b3.svg)
![RTL first](https://img.shields.io/badge/RTL-first-c084fc.svg)

[**Live store**](https://965play.com) · [العربية](README.ar.md) · [Documentation](docs/) · [Portfolio](https://tarek-portfolio-phi.vercel.app)

</div>

---

![The live 965play homepage](docs/img/live-home-desktop.png)

<sub>The live store at [965play.com](https://965play.com), captured on 2 October 2026.</sub>

## The project

965play is an Arabic-first store for gaming hardware, accessories, digital cards and consumer technology in Kuwait. I built the storefront, and I have kept working on it since: the checkout, the product pages and the audit that sets what to improve next. It is one of three stores in the 965 collection, alongside [965toys](https://github.com/tarekokashha/965toys-storefront) and [965gym](https://github.com/tarekokashha/965gym-storefront).

This repository documents the work and how it behaves. The store's own code is part of a production site and is not published here.

## At a glance

| | |
|---|---|
| **Role** | Storefront build, checkout engineering, product-page work, audit and roadmap: [Tarek Okasha](https://github.com/tarekokashha) |
| **Live** | [965play.com](https://965play.com) |
| **Stack** | WordPress, WooCommerce, the Woodmart theme with a child theme, TranslatePress, Elementor, Google Site Kit |
| **Languages** | Arabic by default (right to left), English under `/en/` |
| **Catalogue** | Consoles and accessories, PCs and gaming laptops, sixteen kinds of PC component, collectibles and game cards |
| **Account** | Registration, lost-password recovery, Google sign-in, wishlist |

## What I built

### City-aware delivery at checkout
The checkout works out the right delivery price from the customer's city. A normal city sees three standard services. One of Kuwait's six remote areas sees **exactly one** service, at its own final price, with express hidden and disabled, and the check is repeated **on the server** so an order cannot complete with a service that does not match the city. I tested every one of the six areas, and confirmed that the fee lands in the WooCommerce order total (458.700 KWD plus 7.000 KWD for Al-Khiran gives 465.700 KWD). → [Delivery and checkout](docs/delivery-and-checkout.md)

### A pre-sales PC-expert button
On PC product pages only, a green button above add-to-cart opens a WhatsApp conversation with the product's name and link already in the message, so a customer unsure about compatibility can reach a human at the exact moment of hesitation. The original buy buttons are untouched. → [The PC-expert button](docs/pc-expert-button.md)

![The PC-expert button above add-to-cart on a PC product page](docs/img/live-pc-product-expert-button.png)

### An audit that says how sure it is
Every finding is labelled **LIVE** (confirmed), **AUDIT** (to recheck) or **PLAN** (not yet done), and a release gate forbids cache changes, updates, payment or shipping changes and broad redirects without a tested restore point. → [The audit and roadmap](docs/audit-and-roadmap.md)

### A catalogue that scales
A deep PC-components branch and a clear category tree, with Arabic and English throughout. → [Stack and structure](docs/stack-and-structure.md)

## Screens

| Desktop | Mobile |
|---|---|
| ![Desktop home](docs/img/live-home-desktop.png) | ![Mobile home](docs/img/live-home-mobile.png) |

## Documentation

| | |
|---|---|
| [Delivery and checkout](docs/delivery-and-checkout.md) | The rates, the flow, the server-side check and the tests |
| [The PC-expert button](docs/pc-expert-button.md) | What it does, where it appears, and why |
| [The audit and roadmap](docs/audit-and-roadmap.md) | The method, the findings and what shipped |
| [Stack and structure](docs/stack-and-structure.md) | The stack and the catalogue tree |

## What is not in this repository

The store's theme customisation, plugin code, catalogue data, customer data and credentials. They belong to a live business, so this repository documents the work instead of shipping it. The store's phone numbers are not published here either.

## License and credit

- **Documentation** is [CC BY 4.0](LICENSE). Reuse must credit **Tarek Okasha** and link to this repository.
- 965play's name, logo and imagery, and the console, hardware and game brand names in the screenshots, are **not** licensed here. See [NOTICE](NOTICE.md).

Copyright (c) 2026 Tarek Okasha.

## About the author

I am **Tarek Okasha**, a robotics and automation engineer in Cairo who builds systems that run without supervision: six-axis robots, AI automations, and the custom software and brand presences that companies actually operate on. More of my work is in my [portfolio](https://tarek-portfolio-phi.vercel.app) and on [GitHub](https://github.com/tarekokashha).
