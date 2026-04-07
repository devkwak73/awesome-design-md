# Design System Inspiration of Tumblbug (텀블벅)

## 1. Visual Theme & Atmosphere

Tumblbug is Korea's largest creative crowdfunding platform, connecting independent creators with their audiences across film, music, art, publishing, design, games, and beyond. The visual identity communicates **creative trust**—it should feel culturally savvy, artisanal-warm, and accessible rather than corporate or clinical.

The design is **editorially minimal**: white canvas, restrained typography, and an unmistakable orange-coral accent that carries all emotional energy. Content (project thumbnails, creator portraits, progress bars) does the visual heavy lifting. UI chrome recedes.

The signature element is the **funding progress bar**—a horizontal fill in brand orange that communicates momentum. It transforms financial data into a visceral sense of collective participation.

**Key Characteristics:**
- Pure white canvas with generous card-based project grid
- Pretendard as the single typeface—modern Korean grotesque, clean at every weight
- Brand Orange (`#FF5A36`) as the sole warm accent: CTAs, progress bars, badges
- Dark-ground approach: near-black `#111111` for text, not pure black
- Rounded cards (`border-radius: 12px`) with subtle shadows—friendly, approachable
- 4-column project grid on desktop; 2-column on tablet; 1-column on mobile
- Project thumbnails carry most visual personality; UI remains neutral
- Trust signals: funding percentage, supporter count, deadline urgency

## 2. Color Palette & Roles

### Primary Brand
- **Tumblbug Orange** (`#FF5A36`): The signature CTA color—후원하기 buttons, progress bar fill, active badges, and notification indicators. Energetic and warm.
- **Orange Hover** (`#E54A28`): Pressed/hover state for interactive orange elements.
- **Orange Light** (`#FFF0ED`): Tinted background for orange-context UI (alerts, tag backgrounds, badge washes).

### Text
- **Primary Text** (`#111111`): Headlines, project titles, creator names, body copy.
- **Secondary Text** (`#555555`): Metadata—category labels, funding amounts, supporter counts.
- **Tertiary Text** (`#999999`): Captions, timestamps, helper text, placeholder labels.
- **Disabled Text** (`#CCCCCC`): Inactive states, greyed-out labels.

### Backgrounds & Surfaces
- **Page Background** (`#FFFFFF`): Pure white—the consistent neutral canvas.
- **Surface Gray** (`#F7F7F7`): Alternate section backgrounds, sidebar fills, input backgrounds.
- **Divider** (`#E8E8E8`): Hairline separators between content rows and card grid sections.
- **Skeleton** (`#EEEEEE`): Loading placeholder fill.

### Semantic
- **Success Green** (`#00C897`): Funding reached / goal met badge.
- **Warning Amber** (`#FFAA00`): Deadline urgency ("마감임박") indicator.
- **Error Red** (`#FF3B30`): Validation errors, refund alerts.
- **Info Blue** (`#2E9CFF`): Informational tooltips and link text in body copy.

### Borders & Shadows
- **Card Border** (`1px solid #E8E8E8`): Subtle definition for project cards.
- **Card Shadow** (`rgba(0,0,0,0.06) 0px 2px 8px`): Gentle elevation for cards on hover.
- **Input Focus** (`2px solid #FF5A36`): Orange ring on focused form elements.

## 3. Typography Rules

### Font Family
- **Pretendard**: The sole typeface. Modern Korean grotesque; superior at all weights for Korean + Latin.
- **Fallback chain**: `-apple-system`, `BlinkMacSystemFont`, `"Segoe UI"`, `sans-serif`
- Loaded via CDN: `https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css`

### Hierarchy

| Role | Size | Weight | Line Height | Notes |
|------|------|--------|-------------|-------|
| Hero Headline | 32px | 700 | 1.3 | Campaign banners, section intros |
| Section Heading | 20px | 700 | 1.4 | Category headers, module titles |
| Project Title | 17px | 600 | 1.45 | Card headline—most read element |
| Creator Name | 14px | 500 | 1.4 | Creator attribution under title |
| Body / Description | 14px | 400 | 1.65 | Project descriptions, rich text |
| Metadata | 13px | 400 | 1.4 | Funding %, D-day, supporter count |
| Caption / Tag | 12px | 500 | 1.3 | Category chips, badge labels |
| Navigation | 14px | 500 | 1.4 | Global nav links |
| CTA Button | 15px | 700 | 1.4 | 후원하기, 프로젝트 올리기 |

### Principles
- **Pretendard only**: No mixing with display or serif fonts—consistency is the brand.
- **Weight for hierarchy**: 700 (headlines), 600 (card titles), 500 (labels), 400 (body).
- **Line-height for Korean**: 1.6–1.7 for paragraph text; Korean characters benefit from generous line spacing.
- **No decorative type**: No letter-spacing, text-transform, or italics in UI (italics only in editorial/campaign contexts).

## 4. Component Stylings

### Project Card

**Standard Card**
- Background: `#FFFFFF`
- Border: `1px solid #E8E8E8`
- Border-radius: `12px`
- Box-shadow: none (border only at rest)
- Hover shadow: `rgba(0,0,0,0.08) 0px 4px 16px`
- Overflow: hidden (image fills top)

**Thumbnail Image**
- Aspect ratio: `4 / 3` (standard) or `1 / 1` (square variant)
- Width: 100%
- Object-fit: cover
- Border-radius: `12px 12px 0 0`

**Card Body (padding: 14px 16px 16px)**
- Category chip: 12px, weight 500, `#999999`, no background
- Project title: 17px, weight 600, `#111111`, 2-line clamp
- Creator name: 13px, weight 400, `#555555`
- Progress bar container: height 4px, background `#EEEEEE`, border-radius `2px`
- Progress bar fill: `#FF5A36`, border-radius `2px`
- Funding % label: 14px, weight 700, `#FF5A36`
- Supporter count: 13px, `#555555` — e.g., "1,234명이 함께해요"
- D-day badge: 12px, weight 700, background `#FFF0ED`, color `#FF5A36`, border-radius `4px`, padding `2px 6px`

### Navigation (GNB)

**Container**
- Height: 56px
- Background: `#FFFFFF`
- Border-bottom: `1px solid #E8E8E8`
- Position: sticky top

**Logo** (text "텀블벅" or 't' mark): Left-aligned, `#111111`

**Category Nav Links**
- Font: 14px, weight 500, `#111111`
- Active: `#FF5A36` with 2px bottom border in orange
- Hover: `#FF5A36`
- Gap between items: 24px

**CTA Buttons (right)**
- "프로젝트 올리기": Primary orange button
- "로그인/회원가입": Ghost button

### Buttons

**Primary (Orange)**
- Background: `#FF5A36`
- Color: `#FFFFFF`
- Font: 15px, weight 700
- Padding: `12px 24px`
- Border-radius: `8px`
- Hover: `#E54A28`
- Active: `#CC3E1E`

**Secondary (Outlined)**
- Background: `#FFFFFF`
- Color: `#111111`
- Border: `1.5px solid #111111`
- Font: 15px, weight 600
- Padding: `12px 24px`
- Border-radius: `8px`
- Hover: Background `#F7F7F7`

**Ghost / Text Button**
- Background: transparent
- Color: `#555555`
- No border
- Hover: Color `#111111`

**후원하기 (Fund) Button**
- Same as Primary but full-width on project detail page
- Background: `#FF5A36`
- Height: 52px
- Border-radius: `10px`
- Font: 16px, weight 700

### Progress Bar (Funding Gauge)

```
Container height: 6px
Background:       #EEEEEE
Fill color:       #FF5A36
Border-radius:    3px
```

### Badge / Tag

**Category Chip**
- Background: `#F7F7F7`
- Color: `#555555`
- Font: 12px, weight 500
- Padding: `4px 10px`
- Border-radius: `100px` (pill)

**D-day Badge**
- Background: `#FFF0ED`
- Color: `#FF5A36`
- Font: 12px, weight 700
- Padding: `3px 8px`
- Border-radius: `4px`

**달성 (Achieved) Badge**
- Background: `#E6FAF4`
- Color: `#00C897`
- Font: 12px, weight 700

**마감임박 (Closing Soon) Badge**
- Background: `#FFF8E6`
- Color: `#FFAA00`
- Font: 12px, weight 700

### Form / Input

**Text Input**
- Background: `#FFFFFF`
- Border: `1.5px solid #E8E8E8`
- Border-radius: `8px`
- Height: 48px
- Padding: `0 16px`
- Font: 14px, weight 400, `#111111`
- Placeholder: `#CCCCCC`
- Focus border: `1.5px solid #FF5A36`

## 5. Layout Principles

### Container System
- **Max-width**: `1200px` centered
- **Side padding**: `24px` (desktop), `16px` (mobile)
- **Breakpoints**: `480px` / `768px` / `1024px` / `1200px`

### Project Grid
- **Desktop (≥1024px)**: 4 columns, gap `20px`
- **Tablet (768–1023px)**: 2 columns, gap `16px`
- **Mobile (<768px)**: 2 columns (small cards) or 1 column (large cards), gap `12px`

### Spacing Scale
- `4px` — micro (icon-to-label gaps)
- `8px` — tight (badge internal, caption stacks)
- `12px` — base inner spacing
- `16px` — card body padding, list item separation
- `24px` — between cards, section-to-section
- `32px` — major section separation
- `48px` — hero sections, page-level breathing

### Whitespace Philosophy
- Content density is moderate—not Naver-dense, not empty-editorial.
- Cards breathe at 20px gap; page margins are 24px.
- Category filter bar provides scannable chunking without heavy visual weight.

## 6. Depth & Elevation

### Shadow System

| Level | Usage | Value |
|-------|-------|-------|
| 0 | Default cards, nav | `1px solid #E8E8E8` (border only) |
| 1 | Hovered cards | `rgba(0,0,0,0.08) 0 4px 16px` |
| 2 | Dropdowns, tooltips | `rgba(0,0,0,0.12) 0 8px 24px` |
| 3 | Modals, drawers | `rgba(0,0,0,0.2) 0 16px 48px` |

### Border Radius Scale
- `4px` — badges, chips (small)
- `8px` — buttons, inputs, small cards
- `12px` — project cards, modals
- `100px` — pill buttons, category tabs

## 7. Do's and Don'ts

### Do's
- Use `#FF5A36` exclusively for primary CTAs and progress bar fills
- Apply `12px` border-radius on project cards—it signals friendliness
- Use Pretendard 700 for titles, 400 for body—weight alone carries hierarchy
- Keep project thumbnails as the visual star; minimize UI chrome
- Show funding momentum (progress bar + % + supporter count) as a unified cluster
- Use `border-bottom: 1px solid #E8E8E8` for GNB separation (no box-shadow)
- Keep button labels action-forward: "후원하기", "프로젝트 올리기", not passive labels

### Don'ts
- Don't use orange as a large-area background—it's accent-only
- Don't mix Pretendard with decorative or serif fonts in UI
- Don't add gradient fills—flat orange and white are the language
- Don't use heavy shadows on cards at rest—the border is enough
- Don't crowd D-day and category chips—prioritize the project title
- Don't use orange for error states—reserve red (`#FF3B30`) for errors
- Don't center-align body text in cards—left-align for Korean readability

## 8. Responsive Behavior

### Breakpoints
- `480px` — Mobile S: 1-column grid, full-width cards, simplified nav
- `768px` — Tablet: 2-column grid, horizontal scroll category filters
- `1024px` — Tablet L: 3-column grid, full nav
- `1200px` — Desktop: 4-column grid, max-width container

### Mobile Adaptations
- 4-column grid → 2-column (small) or 1-column (full-width featured)
- Sticky bottom bar with "후원하기" CTA on project detail pages
- Category nav becomes horizontal scrollable strip
- GNB simplifies to logo + search icon + profile icon
- Touch targets minimum `44px` height

### Collapsing Strategy
- 4-column project grid → 2-column at `1024px`
- 2-column → 1-column at `480px`
- Category filter → horizontal scroll strip at `768px`
- Sidebar (if any) → hidden/drawer at `768px`

## 9. Agent Prompt Guide

### Quick Color Reference
```
Page background:     #FFFFFF
Card surface:        #FFFFFF  (border: 1px solid #E8E8E8)
Surface alt:         #F7F7F7
Primary text:        #111111
Secondary text:      #555555
Tertiary text:       #999999
Brand Orange:        #FF5A36  ← primary CTA / progress fill
Orange hover:        #E54A28
Orange light:        #FFF0ED
Success green:       #00C897
Warning amber:       #FFAA00
Error red:           #FF3B30
Divider:             #E8E8E8
Progress bg:         #EEEEEE
Card hover shadow:   rgba(0,0,0,0.08) 0px 4px 16px
```

### Ready-to-Use Prompts

**Build a Tumblbug-style project card:**
Create a crowdfunding project card with white background, `12px` border-radius, and `1px solid #E8E8E8` border. Stack: full-width `4:3` thumbnail image on top; card body below with 14px padding. Show category chip (12px, `#999999`), project title (17px, weight 600, `#111111`, 2-line clamp), creator name (13px, `#555555`), funding progress bar (6px height, background `#EEEEEE`, fill `#FF5A36`), funding percentage (14px, weight 700, `#FF5A36`), and supporter count (13px, `#555555`). Hover: add `rgba(0,0,0,0.08) 0 4px 16px` shadow. Font: Pretendard.

**Build a Tumblbug-style project grid:**
Design a 4-column responsive project grid (max-width 1200px, 24px side padding). Each cell is a project card. Gap between cards: 20px. Responsive: 3-column at 1024px, 2-column at 768px, 2-column (small) at 480px. Include a section heading (20px, weight 700, `#111111`) and a horizontal category filter bar above the grid. Background: `#FFFFFF`. Font: Pretendard.

**Build a Tumblbug-style navigation:**
Design a sticky navigation bar (height 56px, background white, `border-bottom: 1px solid #E8E8E8`). Left: the "텀블벅" wordmark in `#111111`. Center: horizontal nav links (14px, weight 500) — 홈, 상시판매, 인기, 신규, 공개예정, 마감임박. Active link: `#FF5A36` color with 2px bottom border in `#FF5A36`. Right: ghost "로그인" button and orange "프로젝트 올리기" button (border-radius 8px). Font: Pretendard.

**Build a Tumblbug-style funding CTA block:**
Create a sticky bottom funding bar for a project detail page. Full-width bar (background white, `border-top: 1px solid #E8E8E8`). Left: project thumbnail (40px circle) + title (14px, weight 600). Center: progress (funding %, supporter count). Right: full orange "후원하기" button (height 44px, border-radius 8px, background `#FF5A36`, 15px weight 700 white text). Font: Pretendard.

**Build a Tumblbug-style hero banner:**
Design a full-width hero banner with white or dark background (based on campaign). Featured project: large image (aspect ratio 16:9 or 3:2), overlay text block with project title (28px, weight 700, white), creator name (14px, white 80% opacity), funding % badge (background `#FF5A36`, white text, border-radius 6px). Prev/Next navigation arrows (white circles). Dot pagination indicator.
