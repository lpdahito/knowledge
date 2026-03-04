# Common Wireframe Layout Patterns

Reference these patterns when building wireframes. Adapt to the project context.

---

## Landing / Marketing Page
```
┌─────────────────────────────────────┐
│  NAV: Logo | Links | CTA            │
├─────────────────────────────────────┤
│  HERO: Headline + Sub + CTA | Image │
├─────────────────────────────────────┤
│  SOCIAL PROOF: Logos / Testimonial  │
├─────────────────────────────────────┤
│  FEATURES: 3-col icon + text grid   │
├─────────────────────────────────────┤
│  CTA BANNER: Headline + Button      │
├─────────────────────────────────────┤
│  FOOTER: Links | Legal | Social     │
└─────────────────────────────────────┘
```

---

## Dashboard
```
┌──────────┬──────────────────────────┐
│          │  TOP BAR: Search | User  │
│  SIDEBAR │──────────────────────────┤
│  Nav     │  STAT CARDS (row)        │
│  Items   │──────────────────────────┤
│          │  MAIN CHART / TABLE      │
│          │──────────────────────────┤
│          │  SECONDARY CONTENT       │
└──────────┴──────────────────────────┘
```

---

## Auth (Login / Sign Up)
```
┌───────────────┬─────────────────────┐
│               │                     │
│  Brand /      │  Form               │
│  Illustration │  [Email field]      │
│               │  [Password field]   │
│               │  [Submit button]    │
│               │  Alt action link    │
│               │                     │
└───────────────┴─────────────────────┘
```
Mobile: single column, form below brand mark.

---

## Settings / Profile
```
┌──────────────────────────────────────┐
│  PAGE TITLE + Breadcrumb             │
├──────────┬───────────────────────────┤
│  SECTION │  FORM FIELDS              │
│  NAV     │  Label: [Input]           │
│          │  Label: [Input]           │
│  General │  Label: [Toggle]          │
│  Account │                           │
│  Billing │  [Save] [Cancel]          │
│  …       │                           │
└──────────┴───────────────────────────┘
```

---

## Feed / List View
```
┌─────────────────────────────────────┐
│  NAV                                │
├─────────────────────────────────────┤
│  FILTERS / SEARCH BAR               │
├─────────────────────────────────────┤
│  ┌─────────────────────────────┐    │
│  │ [Thumb] Title       Action  │    │
│  │         Meta / Description  │    │
│  └─────────────────────────────┘    │
│  ┌─────────────────────────────┐    │
│  │ [Thumb] Title       Action  │    │
│  └─────────────────────────────┘    │
│  … (repeat)                         │
├─────────────────────────────────────┤
│  PAGINATION / LOAD MORE             │
└─────────────────────────────────────┘
```

---

## Detail / Article Page
```
┌─────────────────────────────────────┐
│  NAV                                │
├──────────────────────┬──────────────┤
│  MAIN CONTENT        │  SIDEBAR     │
│  [Hero Image]        │  Author info │
│  Title               │  Related     │
│  Byline / Date       │  items       │
│  Body text…          │              │
│                      │  [Ad / CTA]  │
│  [Comments section]  │              │
└──────────────────────┴──────────────┘
```
Mobile: sidebar moves below main content.

---

## Onboarding / Wizard
```
┌─────────────────────────────────────┐
│  Logo              Step 2 of 4 ●●○○ │
├─────────────────────────────────────┤
│                                     │
│       [Illustration / Icon]         │
│                                     │
│       Step Title                    │
│       Supporting description text   │
│                                     │
│       [Input or choice UI]          │
│                                     │
├─────────────────────────────────────┤
│  [Back]                    [Next →] │
└─────────────────────────────────────┘
```

---

## Mobile Bottom-Nav App
```
┌─────────────────┐
│ Page Title   ⋮  │  ← Top bar
├─────────────────┤
│                 │
│  Main Content   │
│  Area           │
│                 │
│                 │
├─────────────────┤
│ 🏠  🔍  ➕  🔔  👤 │  ← Bottom nav
└─────────────────┘
```

---

## Empty State
```
┌─────────────────────────────────────┐
│  NAV / HEADER                       │
├─────────────────────────────────────┤
│                                     │
│          [Illustration]             │
│                                     │
│        Nothing here yet             │
│    Supporting explanation text      │
│                                     │
│          [Primary CTA]              │
│                                     │
└─────────────────────────────────────┘
```
