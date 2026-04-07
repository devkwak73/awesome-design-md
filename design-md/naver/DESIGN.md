# Design System Inspiration of Naver

## 1. Visual Theme & Atmosphere

Naver's homepage is Korea's most-visited portal — a masterclass in information density done with quiet restraint. The interface manages to surface an enormous breadth of content (news, search, shopping, weather, stocks, mail) without ever feeling chaotic. The secret is disciplined whitespace, a near-monochromatic base palette, and one powerful accent: Naver Green (`#03C75A`).

The design philosophy is **functional warmth**. Unlike the cold precision of enterprise SaaS or the cinematic drama of tech brands, Naver feels like a trusted daily companion. The backgrounds are pure white or an almost imperceptibly light gray (`#f9fafb`), and every card is defined by an ultra-thin ring shadow (`rgba(0,0,0,0.1) 0px 0px 0px 1px`) rather than a visible border — creating a soft, paper-like sense of layering.

Typography is anchored to Korean system fonts: **Malgun Gothic** on Windows, **Apple SD Gothic Neo** on macOS, falling back to `sans-serif`. Font sizes cluster tight around 13–15px for dense information modules, with the single exception of the hero search input (21px) — a deliberate signal that search is the product's primary purpose. Line heights are generous (1.4–1.5), optimized for comfortable Korean text scanning.

The signature move is the **search bar**: a fully pill-shaped container (`border-radius: 33px`) in pure white with no visible border, hovering above a clean page. It's understated yet unmistakably Naver.

**Key Characteristics:**
- Pure white canvas with subtle `#f9fafb` secondary surfaces
- Naver Green (`#03C75A`) as the sole brand accent — used sparingly but with full confidence
- Ultra-thin ring shadow system replacing visible borders on all card components
- System Korean fonts (Malgun Gothic / Apple SD Gothic Neo) for authentic Korean readability
- 1280px fixed-width container, centered, with `30px` side margins
- Dense information architecture held together by consistent 8px/16px spacing rhythm
- Pill-shaped search bar as the single most prominent UI element
- Conservative, trust-first color usage — no gradients, no dramatic shadows

## 2. Color Palette & Roles

### Primary Brand
- **Naver Green** (`#03C75A`): The unmistakable Naver signature. Used for the search button, primary CTAs, active states, and brand moments. Vibrant yet friendly — neither aggressive nor pastel.
- **Naver Green Dark** (`#03AA5A`): Hover state for green elements. Slightly deeper, maintains full saturation.
- **Naver Green Darker** (`#03A94D`): Active/pressed state. The darkest green in the system.

### Text
- **Primary Text** (`#2E2E2E`): The workhorse — almost-black with a slight warmth. Used for headlines, body copy, and most interactive labels.
- **Secondary Text** (`#737373`): Metadata, dates, secondary labels. A warm mid-gray.
- **Tertiary Text** (`#8C8C8C`): De-emphasized captions, counters, footnotes.
- **Strong Emphasis** (`#1C1C1C`): Near-black for maximum-contrast headings.

### Backgrounds & Surfaces
- **Page Background** (`#FFFFFF`): Pure white — the primary canvas for all content.
- **Secondary Background** (`#F9FAFB`): A near-invisible cool tint used for alternate sections, hover states, and sub-surfaces. So subtle it reads as white at a glance.
- **Tertiary Background** (`#F0F0F0`): Chips, tags, disabled states.

### Interactive & Semantic
- **Link Blue** (`#0C43B7`): Informational links, especially news headlines and search result titles. A rich, saturated blue that reads as "clickable" without being garish.
- **Secondary Blue** (`#406CDC`): Softer blue for secondary interactive elements and info states.
- **Alert Red** (`#F4361E`): Error states, breaking news badges, critical notifications.
- **Live Badge** (`#E31C1C`): "LIVE" indicators and urgent notification badges.

### Borders & Dividers
- **Ring Shadow** (`rgba(0,0,0,0.1) 0px 0px 0px 1px`): The primary "border" system — a spread-only box-shadow creates a soft, inset-feeling edge with no actual border declaration.
- **Depth Shadow** (`rgba(0,0,0,0.04) 0px 1px 2px`): Paired with ring shadow for elevated cards.
- **Divider** (`#E4E4E4`): Section dividers and rule lines.

## 3. Typography Rules

### Font Family
- **Primary (Korean)**: `"Malgun Gothic"`, `"맑은 고딕"` → Windows Korean
- **Primary (macOS)**: `"Apple SD Gothic Neo"` → macOS Korean
- **Fallback chain**: `-apple-system`, `"system-ui"`, `helvetica`, `sans-serif`
- **Display**: Same stack — Naver does not load custom webfonts for performance reasons

### Hierarchy

| Role | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|--------|-------------|----------------|-------|
| Search Input | 21px (1.31rem) | 400 | 1.4 | normal | The largest text on the page — intentional |
| Section Heading | 15px (0.94rem) | 700 | 1.4 | normal | Module titles, news category labels |
| Card Headline | 14.7px (0.92rem) | 700 | 1.4 | normal | News titles, article headlines |
| Body / Link | 14px (0.875rem) | 400–500 | 1.5 | normal | General content, list items |
| Sub-heading | 13.65px (0.85rem) | 500 | 1.45 | normal | Secondary card headers |
| Caption | 12.6px (0.79rem) | 400 | 1.4 | normal | Timestamps, source labels |
| Micro | 11.55px (0.72rem) | 400 | 1.4 | normal | Legal text, counters |
| Navigation | 13px (0.81rem) | 500 | 1.4 | normal | Global nav links |
| CTA Button | 14px (0.875rem) | 700 | 1.4 | normal | Search button, primary actions |

### Principles
- **Dense but readable**: Naver packs more information per viewport than nearly any major portal, yet remains legible through generous line-heights (1.4–1.5) and clean Korean system fonts.
- **Size restraint**: Font sizes barely deviate from 13–15px across the entire page. The only exception is the search input (21px). This creates a homogeneous, scan-friendly information layer.
- **Weight for hierarchy**: Since sizes are constrained, font-weight does most of the hierarchy work. `700` for headlines, `500` for interactive elements, `400` for body.
- **No custom webfonts**: Naver uses the system Korean font stack exclusively, which loads instantly and renders with OS-native quality. This is a deliberate performance and accessibility choice.
- **No decorative typography**: No italics, no letter-spacing, no text-transform except in rare UI labels. Information first.

## 4. Component Stylings

### Search Bar

**Container**
- Background: `#FFFFFF`
- Border-radius: `33px` (full pill)
- Border: none
- Box-shadow: `rgba(0,0,0,0.1) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 4px`
- Height: `58px`
- Max-width: `590px`

**Input Field**
- Font-size: `21px`
- Font-weight: `400`
- Color: `#000000`
- Padding: `17px 20px`
- Border: none
- Background: transparent

**Search Button**
- Background: `#03C75A`
- Color: `#FFFFFF`
- Border-radius: `0 33px 33px 0`
- Width: `80px`
- Height: `100%`
- Icon: magnifying glass SVG
- Hover: `#03AA5A`

### Cards

**Standard Content Card**
- Background: `#FFFFFF`
- Border: none
- Box-shadow: `rgba(0,0,0,0.1) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 1px 2px`
- Border-radius: `8px`
- Padding: `16px`
- Hover: `box-shadow: rgba(0,0,0,0.15) 0px 0px 0px 1px, rgba(0,0,0,0.08) 0px 4px 8px`

**News Card**
- Layout: thumbnail left + text right, OR headline-only
- Headline: 14.7px, weight 700, color `#2E2E2E`
- Source/date: 12.6px, weight 400, color `#8C8C8C`
- Hover: headline color shifts to `#03C75A` or underline appears

**Shopping Card**
- Image: `border-radius: 8px`, fills card width
- Price: weight 700, color `#2E2E2E`
- Discount: weight 700, color `#F4361E`
- Rating: `#03C75A` stars

### Navigation

**Global Nav (GNB)**
- Background: transparent (inherits page white)
- Height: ~48px
- Logo: Naver green wordmark
- Links: 13px, weight 500, color `#2E2E2E`
- Active: color `#03C75A`, bottom border `2px solid #03C75A`
- Hover: color `#03C75A`

**Service Shortcuts**
- Icon size: 32px
- Label: 11–12px, weight 500, color `#2E2E2E`
- Grid: flex wrap, 8 icons per row
- Hover: background `#F9FAFB` behind icon

### Buttons

**Primary (Green)**
- Background: `#03C75A`
- Color: `#FFFFFF`
- Font: 14px, weight 700
- Padding: `10px 20px`
- Border-radius: `8px`
- Hover: `#03AA5A`
- Active: `#03A94D`

**Secondary**
- Background: `#F9FAFB`
- Color: `#2E2E2E`
- Border: `1px solid #E4E4E4`
- Font: 14px, weight 500
- Border-radius: `8px`
- Hover: background `#F0F0F0`

**Text Button / Link Button**
- Background: transparent
- Color: `#0C43B7` or `#2E2E2E`
- No border
- Hover: underline
- Often used for "더보기 ›" (more) links

### Badge / Tag
- Background: `#F0F0F0`
- Color: `#2E2E2E`
- Font: 11–12px, weight 500
- Padding: `2px 7px`
- Border-radius: `4px`
- Special: `#03C75A` background for active/featured tags

## 5. Layout Principles

### Container System
- **Max-width**: `1280px` centered
- **Side margin**: `30px` (desktop)
- **Mobile breakpoint**: `768px`
- **Tablet**: `1024px`

### Spacing Scale
- `4px` — micro gaps (between icon and label)
- `8px` — tight spacing (intra-component)
- `12px` — default inner padding
- `16px` — card padding, section spacing
- `24px` — between major modules
- `32px` — section-level separation

### Grid
- **Main content**: variable-width flex, ~880px
- **Sidebar**: ~300px fixed, right-aligned
- **Gap**: `24px` between main + sidebar
- **Card grids**: 3–4 column, `gap: 8–12px`

### Whitespace Philosophy
- Dense by intent: Naver maximizes visible content without scrolling
- Cards touch (separated by gap, not margin) — efficient use of space
- No "hero" sections — content starts immediately below the search bar
- Breathability comes from white backgrounds and ring shadows, not spacing

## 6. Depth & Elevation

### Shadow System
Naver uses a ring-shadow-based depth system (not traditional drop shadows):

| Level | Usage | Shadow Value |
|-------|-------|-------------|
| 0 (flat) | Inline elements, nav | none |
| 1 (card) | Standard content cards | `rgba(0,0,0,0.1) 0 0 0 1px, rgba(0,0,0,0.04) 0 1px 2px` |
| 2 (elevated) | Hover state, search bar | `rgba(0,0,0,0.1) 0 0 0 1px, rgba(0,0,0,0.08) 0 4px 8px` |
| 3 (overlay) | Dropdowns, tooltips | `rgba(0,0,0,0.15) 0 4px 16px, rgba(0,0,0,0.1) 0 0 0 1px` |
| 4 (modal) | Dialogs, panels | `rgba(0,0,0,0.2) 0 8px 32px` |

### Border Radius Scale
- `4px` — chips, badges, small tags
- `8px` — buttons, cards, inputs
- `12px` — larger cards, modals
- `16px` — bottom corners of expanded panels
- `33px` — search bar, pill buttons

## 7. Do's and Don'ts

### Do's
- **Do** use `#03C75A` as the single brand accent — place it on the search button and primary CTAs
- **Do** use ring shadows (`box-shadow: rgba(0,0,0,0.1) 0 0 0 1px`) instead of visible borders for cards
- **Do** keep font sizes in the 13–15px range for dense modules; reserve 21px for search only
- **Do** use `Malgun Gothic` / `Apple SD Gothic Neo` for all Korean text rendering
- **Do** use 8px and 16px as your primary spacing rhythm
- **Do** show density — Naver modules are information-rich, not spacious
- **Do** use `#0C43B7` for informational links (news headlines, search results)
- **Do** keep backgrounds white or near-white (`#F9FAFB`) — no colored section backgrounds

### Don'ts
- **Don't** use Naver Green as a background color for large areas — it's an accent only
- **Don't** use custom display fonts — the Korean system font stack is intentional
- **Don't** add gradients — Naver's surfaces are always flat
- **Don't** use heavy drop shadows — the ring shadow system defines depth
- **Don't** increase font sizes dramatically for "impact" — density is the design
- **Don't** use rounded corners above 12px on content cards (search bar is the exception)
- **Don't** add decorative elements (patterns, textures, illustrations) — pure UI only
- **Don't** use colors other than green, blue (`#0C43B7`), and red (`#F4361E`) as accents

## 8. Responsive Behavior

### Breakpoints
- `480px` — Mobile S: Single column, search bar full-width
- `768px` — Tablet: 2-column news grid, sidebar collapsed
- `1024px` — Tablet L: 3-column grid, narrow sidebar
- `1280px` — Desktop: Full layout, 880px main + 300px sidebar

### Mobile Adaptations
- Search bar becomes full-width, `border-radius: 12px` (less pill-like)
- Service shortcuts: 4 icons per row (vs 8 on desktop)
- News cards: single column, horizontal thumbnail layout
- Sidebar content (weather, stocks) moves to horizontal scrollable strips
- Font sizes remain constant — Korean mobile readability requires no scaling
- Touch targets minimum `44px` height

### Collapsing Strategy
- Sidebar collapses first at `1024px`
- 3-column card grids become 2-column at `768px`
- 2-column grids become single-column at `480px`
- Navigation abbreviates to logo + search + hamburger on mobile

## 9. Agent Prompt Guide

### Quick Color Reference
```
Page background:     #FFFFFF
Secondary surface:   #F9FAFB
Primary text:        #2E2E2E
Secondary text:      #737373
Naver Green:         #03C75A  ← brand accent
Green hover:         #03AA5A
Link blue:           #0C43B7
Alert red:           #F4361E
Divider:             #E4E4E4
Card shadow:         rgba(0,0,0,0.1) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 1px 2px
```

### Ready-to-Use Prompts

**Build a Naver-style portal homepage:**
> "Build a Korean portal homepage using DESIGN.md. White background, Naver Green (#03C75A) accent. Large pill-shaped search bar (border-radius: 33px) centered at top. Below: news cards with ring shadows (box-shadow: rgba(0,0,0,0.1) 0px 0px 0px 1px), service icon grid, and a right sidebar for widgets. Font stack: Malgun Gothic, Apple SD Gothic Neo, system-ui."

**Build a Naver-style news card:**
> "Create a news card following DESIGN.md. White background, ring shadow (rgba(0,0,0,0.1) 0 0 0 1px), border-radius 8px, 16px padding. Thumbnail left, headline (14.7px, weight 700, #2E2E2E) + source label (12.6px, #8C8C8C) right. Headline turns #03C75A on hover."

**Build a Naver-style search component:**
> "Build the Naver search bar from DESIGN.md. Full-width pill container (border-radius: 33px, box-shadow: rgba(0,0,0,0.1) 0 0 0 1px). Input: 21px, white background. Green (#03C75A) search button on the right with magnifying glass icon."

**Build a Naver-style navigation:**
> "Create a Naver-style GNB using DESIGN.md. White/transparent background, 48px height. Logo left, nav links center (13px, weight 500, #2E2E2E). Active link: #03C75A with 2px bottom border. All links hover to #03C75A."
