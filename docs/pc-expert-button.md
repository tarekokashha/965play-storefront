# The pre-sales PC-expert button

A one-tap path from a PC product page to a human expert on WhatsApp, shown only where it earns its place. Designed and built by [Tarek Okasha](https://github.com/tarekokashha) on the live store on **11 August 2026**.

![A custom gaming PC product page on the live store. A green button reading "Contact an expert now, for help with the build and compatibility" sits above the add-to-cart button.](img/live-pc-product-expert-button.png)

*The live store, captured on 2 October 2026. The green button sits above add to cart.*

## Why it exists

Someone buying a PC build or a high-value machine often needs reassurance about compatibility or specifications **before** they press "add to cart". A form or an email is too slow for that moment, and a vague "contact us" link in the footer is invisible. The button puts a human a single tap away at the exact point of hesitation, in the channel most customers in Kuwait already use.

## What it does

A green button, **"تواصل مع خبير الآن"** (*Contact an expert now*), with the line **"للمساعدة في التجميعة والتوافق"** (*for help with the build and compatibility*), sits directly above the add-to-cart button on the product page.

When tapped it:

- opens a WhatsApp conversation in a **new window**;
- carries the **current product's name** automatically;
- carries the **product's own link** automatically.

The message that arrives has this shape, so the expert knows what the customer is looking at without asking:

```text
مرحبًا 965Play، أحتاج مساعدة من خبير بخصوص: <product name>
<product link>
```

## Where it appears

| Rule | Detail |
|---|---|
| **Only PC products** | It appears on products in the **PCs** category (أجهزة كمبيوتر) and nowhere else |
| **Verified absent elsewhere** | It was checked that it does not appear on a product outside that category |
| **Additive** | The original add-to-cart and buy-now buttons are untouched. The expert button is a separate addition above them |
| **Responsive** | It works on a phone |
| **Accessible** | It has a clear focus state for keyboard users |

On the live store the button carries the class `pc-expert-whatsapp`, and the link is a standard WhatsApp click-to-chat URL with the message pre-filled and URL-encoded.

## Design notes

- **Scoped by category, not by price.** A category is a rule a store owner already understands and controls, and it avoids showing a "talk to an expert" button on a cable.
- **Additive, never replacing.** A button that removes the normal path would cost sales it was meant to create.
- **Context in the message.** A message that already contains the product name and link saves a round trip, and lets the expert answer in the first reply.

## For the team

When a message arrives it already carries the product name and link, so the expert can reply with a few short questions about the intended use, the budget and the resolution needed before suggesting an alternative.

## What it deliberately does not do

It does not change any price, payment setting or WhatsApp notification configuration. See [delivery-and-checkout.md](delivery-and-checkout.md) for the full list of what was and was not touched.

## What to measure

The value of the button depends on how quickly the expert replies. Two things worth tracking, both recommended and not yet implemented: clicks on the button (a GA4 event), and sales that begin in the WhatsApp conversation.
