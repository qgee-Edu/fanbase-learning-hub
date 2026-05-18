# Fanbase Support Center: Mintlify Build

A drop-in Mintlify documentation package for the Fanbase Support Center. Three hubs, nine modules, all referenced images mapped to a single image-specifications brief.

## What's in this package

```
fanbase-learning-hub/
├── docs.json                          # Mintlify navigation config (3 tabs, 9 modules)
├── index.mdx                          # Landing page
├── IMAGE_SPECIFICATIONS.md            # Detailed brief for every referenced image
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
    ├── business-center/               # Drop image assets here
    ├── knowledge-center/
    └── creator-academy/
```

## Module status

| Module | Status | Notes |
|---|---|---|
| 1.1 Getting Paid | Converted from draft | All draft VERIFY flags preserved as Mintlify Warning callouts |
| 1.2 Payment Account Setup | Converted from draft | All draft VERIFY flags preserved |
| 1.3 Subscriptions & Pricing | Built from scratch | Replaces the old paywall model. Verify subscription price range with platform team. |
| 2.1 Getting Started | Converted from draft | All draft VERIFY flags preserved |
| 2.2 Fanbase Features | Converted from draft | All draft VERIFY flags preserved. Largest module. |
| 3.1 Monetize Basics | Built from scratch | Builds on 1.1, 1.3, and 2.2 |
| 3.2 Content Strategy | Built from scratch | Sustainable rhythm + Live structure |
| 3.3 Creator Insights & Spotlights | Built from scratch | Spotlight section needs creator sourcing before publishing |

## Style notes baked in

- **No em dashes anywhere** (per your preference). Colons, periods, parentheses only.
- **Mintlify-native components** used throughout: `Steps`, `Cards`, `CardGroup`, `AccordionGroup`, `Tabs`, `Frame`, `Tip`, `Info`, `Warning`, `Note`, `Check`.
- **Every VERIFY flag from the original drafts is preserved** as a Mintlify `<Warning>` callout so the platform team can audit them in place.
- **Every image is referenced by path** and matched to a specification entry in `IMAGE_SPECIFICATIONS.md`. No image is referenced without a spec.

## What to do next

1. **Drop the directory into your Mintlify project root** and run `mintlify dev` to preview.
2. **Resolve VERIFY flags** with the platform team (Justin, Lauren, Isaac, Andy, Amario). All are tagged inline in Warning callouts.
3. **Brief design or capture an illustrator** using `IMAGE_SPECIFICATIONS.md`. Every referenced image has a description and intended type (annotated screenshot vs concept diagram).
4. **Source creators for Module 3.3 Spotlights.** Replace the three placeholder Spotlights with real creator stories.
5. **Confirm the subscription price range** referenced in 1.3 (the two existing drafts cite different ranges).
