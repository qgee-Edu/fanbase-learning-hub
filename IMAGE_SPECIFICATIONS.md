# Fanbase Support Center: Image Inventory

A complete map of every image in the package. 22 images total: 15 brand-aligned SVG diagrams designed in-package, 5 real app screenshots, and 2 logo placeholder slots.

All SVGs use the official Fanbase color palette:

- **Icon Gradient:** `#2B0458` → `#841AC8` → `#871951`
- **Love Gradient:** `#FF1BAF` → `#FF3F24` → `#FFA624`
- **Fanbase Violet:** `#9824FF` (primary accent)
- **Fanbase Pink:** `#FF00D6` (dark-mode accent)
- **White:** `#FFFFFF` (all text)

## Global

| Path | Type | Status | Description |
|---|---|---|---|
| `/images/home-hero.svg` | SVG hero | ✅ Done | Landing page hero with the lightning bolt centerpiece and three hub cards |
| `/images/favicon.svg` | Brand asset | Placeholder | Use the App Store icon from the brand kit (violet square with white lightning bolt F) |
| `/images/logo-light.svg` | Brand asset | Placeholder | Logo for light mode (needs a dark/violet version of the Fanbase wordmark) |
| `/images/logo-dark.svg` | Brand asset | Placeholder | Logo for dark mode (use the white wordmark from the brand kit) |

## Business Center (5 images)

| Path | Type | Status | Used in |
|---|---|---|---|
| `/images/business-center/hub-hero.svg` | SVG hero | ✅ Done | Business Center overview page |
| `/images/business-center/1-1-three-ways-to-earn.svg` | SVG diagram | ✅ Done | Module 1.1 Lesson 1 |
| `/images/business-center/1-1-payment-flow.svg` | SVG diagram | ✅ Done | Module 1.1 Lesson 2 |
| `/images/business-center/1-3-public-vs-exclusive.svg` | SVG diagram | ✅ Done | Module 1.3 Lesson 1 |
| `/images/business-center/1-3-price-selector.png` | Real screenshot | ✅ Done | Module 1.3 Lesson 3 |

## Knowledge Center (7 images)

| Path | Type | Status | Used in |
|---|---|---|---|
| `/images/knowledge-center/hub-hero.svg` | SVG hero | ✅ Done | Knowledge Center overview page |
| `/images/knowledge-center/2-1-cover.png` | Real screenshot | ✅ Done | Module 2.1 cover (Amara Jackson profile) |
| `/images/knowledge-center/2-1-create-menu.png` | Real screenshot | ✅ Done | Module 2.1 Lesson 2 (Create something sheet) |
| `/images/knowledge-center/2-2-live-setup.png` | Real screenshot | ✅ Done | Module 2.2 Section 1.4 (Live broadcast) |
| `/images/knowledge-center/2-2-audio-room.png` | Real screenshot | ✅ Done | Module 2.2 Section 1.5 (Audio Room) |
| `/images/knowledge-center/2-2-public-vs-exclusive.svg` | SVG diagram | ✅ Done | Module 2.2 Section 2 |
| `/images/knowledge-center/2-2-love-packs.svg` | SVG diagram | ✅ Done | Module 2.2 Section 3.1 |

## Creator Academy (9 images)

| Path | Type | Status | Used in |
|---|---|---|---|
| `/images/creator-academy/hub-hero.svg` | SVG hero | ✅ Done | Creator Academy overview page |
| `/images/creator-academy/3-1-three-paths.svg` | SVG diagram | ✅ Done | Module 3.1 Lesson 1 |
| `/images/creator-academy/3-1-conversion-funnel.svg` | SVG diagram | ✅ Done | Module 3.1 Lesson 2 |
| `/images/creator-academy/3-1-cross-platform-flow.svg` | SVG diagram | ✅ Done | Module 3.1 Lesson 3 |
| `/images/creator-academy/3-1-30-day-plan.svg` | SVG diagram | ✅ Done | Module 3.1 Lesson 4 |
| `/images/creator-academy/3-2-format-jobs.svg` | SVG diagram | ✅ Done | Module 3.2 Lesson 1 |
| `/images/creator-academy/3-2-weekly-rhythm.svg` | SVG diagram | ✅ Done | Module 3.2 Lesson 2 |
| `/images/creator-academy/3-3-audience-to-community.svg` | SVG diagram | ✅ Done | Module 3.3 Lesson 1 |
| `/images/creator-academy/3-3-responsible-influence.svg` | SVG diagram | ✅ Done | Module 3.3 Lesson 2 |

## What's not yet visualized (optional follow-up)

The following modules would benefit from additional visuals but currently work fine without them:

- **Module 1.1:** Real Revenue Dashboard screenshot would deepen Lesson 3
- **Module 1.2:** Profile-to-Settings flow screenshots would help the procedural Steps
- **Module 2.1:** A bottom-nav annotation graphic + an Edit Profile flow graphic
- **Module 2.2:** Real Post composer, Flickz editor, FB+ upload screenshots (currently all flagged for capture in `<Warning>` callouts)
- **Module 3.2:** A daily Story sequence visual and Live broadcast structure visual

If any of these become priorities, the SVG files can be designed and dropped into the matching folder, then the `<Frame>` block restored in the relevant `.mdx`.

## Production notes

- **All SVGs are designed dark-first.** They look correct in dark mode (the default) and also render fine in light mode because they use opaque or bright fills throughout.
- **SVG dimensions:** Heroes are 1200×600 or 1200×400, diagrams are 1200×400 or 1200×500.
- **File sizes:** Every SVG is under 5KB. The full image folder is under 250KB total.
- **Real screenshots** are PNG, sized for retina display, from the actual Fanbase 1.5 build.
- **Fonts in SVGs** specify Inter as the family, with sans-serif fallback. This matches the `docs.json` typography setting so SVG text matches surrounding page text.
