---
name: xmsumi-vibeui-prompts
description: "VibeUI prompt library for rapid UI component generation in vibecoding workflows. 92 battle-tested prompts across 15 categories (auth, pricing, hero, nav, dashboard, etc.). Use when user says: vibeui, vibe ui, generate UI component, landing page section, create a hero/pricing/nav/footer/CTA/testimonial/FAQ/dashboard, UI prompt, vibecoding UI."
---

# VibeUI — Vibecoding UI Prompt Library

Generate production-ready UI components using 92 curated prompts from [VibeUI](https://vibeui.online/).

## How It Works

1. **User describes** what UI section they need (or provides a screenshot)
2. **Match** the right prompt from the library below
3. **Customize** the prompt with user's specific content/brand details
4. **Generate** the component code (HTML/CSS/React/etc.)

## Quick Category Index

| Category | IDs | Count | When to Use |
|----------|-----|-------|-------------|
| Auth Forms | `auth-1` ~ `auth-6` | 6 | Login, signup, registration pages |
| Pricing | `pr-1` ~ `pr-8` | 8 | Pricing pages, plan comparison |
| Features / Bento | `ft-1` ~ `ft-8` | 8 | Feature showcases, product highlights |
| Hero Sections | `hr-1` ~ `hr-8` | 8 | Landing page headers, first impressions |
| CTA Banners | `cta-1` ~ `cta-7` | 7 | Call-to-action sections, conversion blocks |
| Stats Bars | `st-1` ~ `st-7` | 7 | Numbers, metrics, social proof stats |
| Nav Bars | `nv-1` ~ `nv-8` | 8 | Navigation, menus, sidebars |
| Testimonials | `ts-1` ~ `ts-8` | 8 | Customer reviews, social proof |
| Footer | `ft-1f` ~ `ft-5f` | 5 | Page footers |
| FAQ | `fq-1` ~ `fq-5` | 5 | FAQ sections, help pages |
| Dashboards | `ds-1` ~ `ds-6` | 6 | Admin panels, app dashboards |
| Onboarding | `ob-1` ~ `ob-4` | 4 | User onboarding, empty states |
| Blog / Content | `bl-1` ~ `bl-4` | 4 | Blog layouts, content pages |
| Contact | `ct-1` ~ `ct-3` | 3 | Contact forms, support pages |
| Bonus | `bn-1` ~ `bn-5` | 5 | Comparison tables, 404, cookie banners, loading states |

## Workflow

### Step 1: Identify Component Need

User says something like:
- "I need a pricing section" → Go to **Pricing** (`pr-*`)
- "Make me a hero" → Go to **Hero Sections** (`hr-*`)
- "Add a nav bar" → Go to **Nav Bars** (`nv-*`)
- "I need a login page" → Go to **Auth Forms** (`auth-*`)

### Step 2: Present Options

Show the user the available variants in that category with their descriptions. Help them pick the best fit. Example for Hero:

```
Available Hero styles:
1. hr-1: Centered text + screenshot below
2. hr-2: Split layout — text one side, visual the other
3. hr-3: Video/animated background
4. hr-4: Animated gradient mesh background
5. hr-5: Terminal/code-editor visual
6. hr-6: Floating UI elements around heading
7. hr-7: Big bold oversized typography
8. hr-8: Hero with inline email capture form

Which style fits your vision?
```

### Step 3: Customize and Generate

Take the selected prompt template and:

1. **Replace** generic placeholders with user's actual content (company name, product details, colors)
2. **Append** framework preference: "Output as React/Tailwind", "Use vanilla HTML/CSS", etc.
3. **If user provides a screenshot**: keep the default suffix — *"Match the visual style, colors, typography, and overall aesthetic of the UI shown in my screenshot."*
4. **If no screenshot**: replace the suffix with specific design tokens: *"Use [color palette], [font family], [spacing scale], [border radius], [shadow style]."*

### Step 4: Compose Full Pages

Combine multiple prompts for complete pages:

```
Landing Page Recipe:
1. hr-2 (Split hero) → top section
2. nv-1 (Minimal nav) → navigation
3. ft-2 (Bento grid) → features
4. st-1 (Horizontal stats) → social proof numbers
5. ts-3 (Masonry testimonials) → reviews
6. pr-1 (3-tier pricing) → pricing
7. fq-1 (Accordion FAQ) → FAQ
8. cta-1 (Gradient banner) → final CTA
9. ft-1f (Multi-column footer) → footer
```

## Prompt Templates

All 92 prompts share a common structure:

```
Create a [component type] as [layout pattern].
[Specific details about content and structure].
[Style matching instruction].
```

**Default style suffix** (when user provides a screenshot):
> Match the visual style, colors, typography, and overall aesthetic of the UI shown in my screenshot.

**Custom style suffix** (when no screenshot):
> Use [specific design system details: colors, fonts, spacing, border-radius, shadows].

For the complete prompt text of each template, see [prompts-index.md](prompts-index.md).

## Popular Combos

**SaaS Landing Page:**
`nv-6` + `hr-1` + `ft-2` + `st-2` + `pr-2` + `ts-1` + `fq-1` + `cta-1` + `ft-1f`

**Product Launch:**
`nv-5` + `hr-7` + `hr-3` + `ft-3` + `bn-2` + `cta-6` + `ft-3f`

**Dashboard App:**
`nv-4` + `ds-1` + `ds-5` + `ob-1` + `ds-6`

**Mobile App Web:**
`nv-8` + `hr-6` + `ft-7` + `ts-2` + `pr-6` + `cta-3`

## UI Interaction

When the user triggers the skill or asks to browse prompts, display the interactive explorer:

```
show_widget(
  widget_path: "xmsumi-vibeui-prompts/assets/prompt-explorer.html",
  title: "VibeUI Prompt Explorer",
  i_have_seen_guidelines: true
)
```

The widget allows users to:
- Browse all 92 prompts by category
- Search prompts by keyword, ID, or category
- Click a card to view the full prompt text
- Copy prompts to clipboard
- View popular combo recipes
