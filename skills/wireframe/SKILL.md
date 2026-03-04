---
name: wireframe
description: Guide the user through wireframing an app UI/UX. Asks about the project, the page to wireframe, and which tool to use based on available MCP servers and tools.
user-invocable: true
argument-hint: "[page-name]"
---

# Wireframing Assistant

You are helping the user create a wireframe. Follow these steps in order:

## Step 1 — Choose a Tool

Ask the user which tool they'd like to use. Present only the options that are relevant based on what's available:

- **Paper** — use if the `paper` MCP server is connected (check for `mcp__paper__*` tools)
- **Figma** — use if the `figma` MCP server is connected
- **Pencil** — if the user prefers Pencil (pencil.dev), note they'll need to work in Pencil directly
- **Hand-drawn / pencil & paper** — for lo-fi sketching; you'll provide a textual wireframe outline instead
- **ASCII wireframe** — output a structured ASCII wireframe in the chat

If $ARGUMENTS is provided, it may indicate the page name — skip asking about the page in Step 2 and use $ARGUMENTS as the page name.

## Step 2 — Understand the Project

Ask the user:
1. **What is the project?** (app name, product type, target users)
2. **What page or screen are you wireframing?** (e.g. Login, Dashboard, Onboarding step 2) — skip if provided via $ARGUMENTS
3. **What is the primary goal of this page?** (what should the user accomplish or understand?)
4. **Any constraints?** (mobile/tablet/desktop, specific components required, content to include)

## Step 3 — Wireframe

> **Important:** Wireframes consist of graphic elements only — shapes, labels, placeholder text, and layout blocks. Do **not** generate any code (HTML, CSS, JS, etc.) unless the user has explicitly chosen to wireframe directly for a web browser, in which case lightweight HTML/CSS is acceptable as an inevitable medium.

Based on the tool selected and the project context:

### If Paper (MCP available):
- Call `mcp__paper__get_basic_info` to check the current canvas
- Create a new artboard at the appropriate device size (mobile: 390×844, tablet: 768×1024, desktop: 1440×900)
- Build a low-fidelity wireframe using grayscale colors only (#FFFFFF, #F5F5F5, #E0E0E0, #BDBDBD, #757575, #212121)
- Use placeholder text ("Page Title", "Body copy here", "Button") and gray rectangles for images
- Label each section clearly (Nav, Hero, Content, Footer, etc.)
- Focus on layout and information hierarchy — no decorative styling

### If Figma (MCP available):
- Guide the user to create a frame at the appropriate size
- Provide a structured layout description they can build in Figma

### If ASCII wireframe:
Output a structured ASCII wireframe like this example format:
 
```
┌─────────────────────────────────────┐
│  NAVIGATION BAR                     │
│  [Logo]          [Link] [Link] [CTA]│
├─────────────────────────────────────┤
│                                     │
│  HERO SECTION                       │
│  ┌─────────────────┐ ┌───────────┐  │
│  │  Headline text  │ │  [Image]  │  │
│  │  Subheadline    │ │           │  │
│  │  [CTA Button]   │ └───────────┘  │
│  └─────────────────┘                │
├─────────────────────────────────────┤
│  CONTENT SECTION                    │
│  ┌────────┐ ┌────────┐ ┌────────┐  │
│  │ Card 1 │ │ Card 2 │ │ Card 3 │  │
│  └────────┘ └────────┘ └────────┘  │
├─────────────────────────────────────┤
│  FOOTER                             │
└─────────────────────────────────────┘
```

### If hand-drawn / pencil & paper:
Provide a written layout brief the user can sketch from:
- List each section in order (top to bottom)
- Describe what goes in each section
- Note approximate proportions and priority

## Step 3b — Propose Layouts (if no layout specified)

If the user has not described how the page should look, generate **3 distinct layout options** before building anything. Each option should have:
- A short name (e.g. "Centered Focus", "Split Screen", "Card Grid")
- A 2–3 sentence description of the structure and why it suits the page's goal
- An ASCII sketch showing the rough layout

Present all 3 options and ask the user to choose one (or describe their own) before proceeding to Step 3.

## Step 4 — Iterate

After presenting the wireframe, ask:
- "Does this layout match your vision?"
- "Would you like to adjust any sections, add pages, or explore an alternative layout?"

Be ready to revise or wireframe additional pages/states (e.g. empty state, error state, logged-in vs. guest).
