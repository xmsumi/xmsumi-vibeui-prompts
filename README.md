# xmsumi-vibeui-prompts

> 92 battle-tested UI component prompts across 15 categories — for rapid vibecoding

**[中文文档](README-CN.md)**

VibeUI - A curated prompt library , designed for AI-assisted coding (Vibecoding) workflows. Generate production-ready UI components — Hero sections, Pricing, Navigation, Dashboards, and more — with screenshot-based style matching and custom design system support.

## Features

- **92 Prompt Templates** — covering Auth Forms, Pricing, Hero, Nav Bars, Dashboards, and 10 more UI categories
- **Screenshot Style Matching** — provide a design screenshot, AI auto-matches colors, typography, spacing, and visual style
- **Custom Design Tokens** — no screenshot? Specify your own color palette, font family, border-radius, shadows
- **Page Combo Recipes** — 4 built-in combos: SaaS Landing Page, Product Launch, Dashboard App, Mobile App Web
- **Interactive Explorer** — built-in HTML browser with category filtering, keyword search, and one-click copy
- **Agent Skill Format** — compatible with Qoder / Claude Code and other AI IDE skill specs, install and use instantly

## Screenshots

### Category Browser

![Category Browser](assets/ScreenShot_1.png)

### Popular Combos

![Popular Combos](assets/ScreenShot_2.png)

## Demo Examples

Real page outputs generated with this Skill:

### SaaS Landing Page

> Combo: `nv-6` + `hr-1` + `ft-2` + `st-2` + `pr-2` + `ts-1` + `fq-1` + `cta-1` + `ft-1f`

[View Source](assets/vibeui-saas-landing.html)

![VibeUI SaaS Landing Page](assets/vibeui-saas-landing.png)

### More Examples

<table>
<tr>
<td width="50%">
<b>AI Product Launch</b><br>
<a href="assets/mada-ai-product-launch.html">View Source</a><br>
<img src="assets/mada-ai-product-launch.png" alt="AI Product Launch" width="100%">
</td>
<td width="50%">
<b>WeChat Multi-Account Dashboard</b><br>
<a href="assets/wechat-multi-account-dashboard.html">View Source</a><br>
<img src="assets/wechat-multi-account-dashboard.png" alt="WeChat Multi-Account Dashboard" width="100%">
</td>
</tr>
</table>

## Categories

| Category | Count | ID Range | Use Cases |
|----------|-------|----------|-----------|
| Auth Forms | 6 | `auth-1` ~ `auth-6` | Login, signup, registration pages |
| Pricing | 8 | `pr-1` ~ `pr-8` | Pricing pages, plan comparison |
| Features / Bento | 8 | `ft-1` ~ `ft-8` | Feature showcases, product highlights |
| Hero Sections | 8 | `hr-1` ~ `hr-8` | Landing page headers, first impressions |
| CTA Banners | 7 | `cta-1` ~ `cta-7` | Call-to-action sections, conversion blocks |
| Stats Bars | 7 | `st-1` ~ `st-7` | Numbers, metrics, social proof stats |
| Nav Bars | 8 | `nv-1` ~ `nv-8` | Navigation, menus, sidebars |
| Testimonials | 8 | `ts-1` ~ `ts-8` | Customer reviews, social proof |
| Footer | 5 | `ft-1f` ~ `ft-5f` | Page footers |
| FAQ | 5 | `fq-1` ~ `fq-5` | FAQ sections, help pages |
| Dashboards | 6 | `ds-1` ~ `ds-6` | Admin panels, app dashboards |
| Onboarding | 4 | `ob-1` ~ `ob-4` | User onboarding, empty states |
| Blog / Content | 4 | `bl-1` ~ `bl-4` | Blog layouts, content pages |
| Contact | 3 | `ct-1` ~ `ct-3` | Contact forms, support pages |
| Bonus | 5 | `bn-1` ~ `bn-5` | Comparison tables, 404, cookie banners, loading states |

## Popular Combos

```
SaaS Landing Page:
nv-6 + hr-1 + ft-2 + st-2 + pr-2 + ts-1 + fq-1 + cta-1 + ft-1f

Product Launch:
nv-5 + hr-7 + hr-3 + ft-3 + bn-2 + cta-6 + ft-3f

Dashboard App:
nv-4 + ds-1 + ds-5 + ob-1 + ds-6

Mobile App Web:
nv-8 + hr-6 + ft-7 + ts-2 + pr-6 + cta-3
```

## Installation

### Qoder (Recommended)

Clone or copy this repo into your project's `.qoder/skills/` directory:

```bash
# Project-level install
git clone https://github.com/xmsumi/xmsumi-vibeui-prompts.git .qoder/skills/xmsumi-vibeui-prompts

# Global install
git clone https://github.com/xmsumi/xmsumi-vibeui-prompts.git ~/.qoder/skills/xmsumi-vibeui-prompts
```

### Claude Code

Place `SKILL.md` into your `.claude/skills/` directory.

### Codex

Clone or copy this repo into your project's `.codex/skills/` directory:

```bash
# Project-level install
git clone https://github.com/xmsumi/xmsumi-vibeui-prompts.git .codex/skills/xmsumi-vibeui-prompts

# Global install
git clone https://github.com/xmsumi/xmsumi-vibeui-prompts.git ~/.codex/skills/xmsumi-vibeui-prompts
```

## Usage

### In AI IDE

After installation, just ask in chat:

```
Build me a SaaS landing page
```

```
I need a pricing section
```

```
Use vibeui to generate a hero with split layout
```

The AI will automatically match the best-fitting template from the library and generate complete component code.

### With Screenshots

1. Prepare a design screenshot
2. Tell the AI which template ID to use (e.g. `hr-2`)
3. AI auto-matches the visual style from your screenshot

### Direct Prompt Usage

Browse all prompts via `prompts-index.md` or `assets/prompt-explorer.html`, copy and use directly:

```
Create a hero section as a split layout — heading, subheading, and CTAs on one side,
and a product mockup or visual on the other.
Use Inter font, #6366f1 primary color, 12px border-radius, soft shadows.
```

### Custom Style Suffix

**With screenshot** (default):
> Match the visual style, colors, typography, and overall aesthetic of the UI shown in my screenshot.

**Without screenshot** (replace with your design tokens):
> Use Inter font, #6366f1 primary, #f8fafc background, 12px border-radius, 0 4px 6px rgba(0,0,0,0.1) shadows.

## Project Structure

```
xmsumi-vibeui-prompts/
├── SKILL.md                                    # Agent Skill main file (workflow + category index)
├── prompts-index.md                            # 92 prompts full reference
├── README.md                                   # English docs (this file)
├── README-CN.md                                # Chinese docs
└── assets/
    ├── prompt-explorer.html                    # Interactive prompt browser
    ├── vibeui-saas-landing.html / .png         # Demo: SaaS Landing Page
    ├── mada-ai-product-launch.html / .png      # Demo: AI Product Launch
    ├── wechat-multi-account-dashboard.html / .png  # Demo: WeChat Dashboard
    ├── ScreenShot_1.png                        # Category browser screenshot
    └── ScreenShot_2.png                        # Popular Combos screenshot
```

## How It Works

All 92 prompts share a unified structure:

```
Create a [component type] as [layout pattern].
[Specific content and structure details].
[Style matching instruction].
```

**Workflow**:

1. **Identify Need** — User describes which UI section they need
2. **Match Template** — Select the best-fitting layout from the category
3. **Customize & Generate** — Replace placeholder content, append framework preference (React/Vue/Tailwind, etc.)
4. **Compose Pages** — Chain multiple templates to build complete pages

## Prompt Explorer

The built-in `assets/prompt-explorer.html` is a standalone interactive page:

- Dark theme with gradient highlights
- 16 category tabs for quick switching
- Keyword search (by ID, name, or description)
- Click cards to view full prompt text
- One-click copy to clipboard
- 4 Popular Combos displayed at the bottom

Open directly in a browser, or embed in AI IDEs via `show_widget`.

## License

MIT

## Author

- Website: [xmsumi.com](https://www.xmsumi.com/)
- GitHub: [github.com/xmsumi](https://github.com/xmsumi)
