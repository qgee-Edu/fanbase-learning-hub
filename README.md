# Fanbase Support Center: Mintlify Build

A drop-in Mintlify documentation package for the Fanbase Support Center. Three hubs, nine modules, twenty-two branded visuals, and full brand-kit alignment baked in.

## Quick start

```bash
# 1. Replace your Mintlify project root with the contents of this package
# 2. Preview locally
mint dev
# 3. Push to GitHub. Mintlify auto-deploys.
```

## What's in this package

```
fanbase-learning-hub/
├── docs.json                          # Mintlify config: nav, brand colors, fonts, dark mode
├── index.mdx                          # Landing page
├── README.md                          # This file
├── IMAGE_SPECIFICATIONS.md            # Full image inventory
├── business-center/
│   ├── overview.mdx                   # Business Center hub overview
│   ├── getting-paid.mdx               # Module 1.1
│   ├── payment-account-setup.mdx      # Module 1.2
│   └── subscriptions-and-pricing.mdx  # Module 1.3
├── knowledge-center/
│   ├── overview.mdx                   # Knowledge Center hub overview
│   ├── getting-started.mdx            # Module 2.1
│   └── fanbase-features.mdx           # Module 2.2
├── creator-academy/
│   ├── overview.mdx                   # Creator Academy hub overview
│   ├── monetize-basics.mdx            # Module 3.1
│   ├── content-strategy.mdx           # Module 3.2
│   └── creator-insights-and-spotlights.mdx  # Module 3.3
└── images/
    ├── home-hero.svg                  # Landing page hero
    ├── business-center/               # 5 visuals (4 SVG diagrams + 1 real screenshot)
    ├── knowledge-center/              # 7 visuals (3 SVG diagrams + 4 real screenshots)
    └── creator-academy/               # 10 visuals (all SVG diagrams)
```

## Brand alignment

Every choice in `docs.json` pulls from the official Fanbase Asset Creation Guidelines.

| Element | Value | Source |
|---|---|---|
| Primary color | `#9824FF` | Fanbase Violet |
| Dark mode accent | `#FF00D6` | Fanbase Pink |
| Light mode highlight | `#C77DFF` | Light violet derived from primary |
| Dark background | `#0A0118` | Deep tint of the Icon Gradient start `#2B0458` |
| Background decoration | gradient | Adds subtle texture, matches brand mood |
| Default appearance | dark | Matches Fanbase app default |
| Typography | Inter | SF Pro equivalent on Google Fonts |

## Image inventory: 22 visuals across the docs

Every page has at least one visual. The heaviest modules (3.1 Monetize Basics, 2.2 Fanbase Features) carry 4 each.

**SVG diagrams (15)** are designed in-package using the official Fanbase color palette: Icon Gradient (`#2B0458` to `#841AC8` to `#871951`) and Love Gradient (`#FF1BAF` to `#FF3F24` to `#FFA624`), with violet and pink accents. They render crisp at any size, work natively in dark mode, and weigh under 5KB each.

**Real app screenshots (5)** are the in-product UI captures: the Set Subscription Price screen, the Create Something sheet, the Amara Jackson profile, the live broadcast, and the Audio Room.

See `IMAGE_SPECIFICATIONS.md` for the full per-image inventory.

## Module status

| Module | Status | Visuals |
|---|---|---|
| 1.1 Getting Paid | Converted from draft | Cover, 3-ways-to-earn, payment flow |
| 1.2 Payment Account Setup | Converted from draft | None (procedural, uses Steps component) |
| 1.3 Subscriptions & Pricing | Built from scratch | Public-vs-Exclusive, real price selector screenshot |
| 2.1 Getting Started | Converted from draft | Real profile screenshot, real create-menu screenshot |
| 2.2 Fanbase Features | Converted from draft | Real Live broadcast + Audio Room + Public-vs-Exclusive + Love packs |
| 3.1 Monetize Basics | Built from scratch | Three paths + funnel + cross-platform + 30-day plan |
| 3.2 Content Strategy | Built from scratch | Format jobs + weekly rhythm |
| 3.3 Creator Insights & Spotlights | Built from scratch | Audience-to-community + Responsible Influence |

## Style rules baked in

- **No em dashes anywhere.** Colons, periods, parentheses only. Verified by automated check.
- **Mintlify-native components** throughout: `Steps`, `Cards`, `CardGroup`, `AccordionGroup`, `Tabs`, `Frame`, `Tip`, `Info`, `Warning`, `Note`, `Check`.
- **Subscription price range** ($0.99 to $49.99) is consistent across Modules 1.1, 1.3, and 2.2, confirmed against the in-app price selector screenshot.
- **All VERIFY flags** from original drafts are preserved as `<Warning>` callouts so the platform team can audit them in place.
- **Every image is referenced by path** and every referenced path has a real file behind it.

## To deploy

In GitHub Desktop (or whatever you've been using):

1. Open your cloned repo folder
2. Replace the existing files with everything in this package
3. Commit with a message like "Full Fanbase Support Center build with brand visuals"
4. Push

Mintlify auto-deploys within a minute or two.

## What's left to fully polish

In priority order:

1. **Upload logo and favicon SVGs.** Drop them at `images/logo-light.svg`, `images/logo-dark.svg`, and `images/favicon.svg`. The brand kit says the logo is always white; for light mode you'll need a dark/violet version.
2. **Resolve VERIFY flags** with the platform team. All are tagged inline as `<Warning>` callouts. Walk through them with Justin, Lauren, Isaac, Andy, and Amario.
3. **Source creators for Module 3.3 Spotlights.** Three placeholder slots are scaffolded and waiting for real creator stories.
4. **Capture additional real app screenshots** if you want to deepen specific modules (Revenue Dashboard view, Edit Profile screen, Post composer, Flickz editor, FB+ upload). The SVG diagrams currently fill those slots conceptually.
