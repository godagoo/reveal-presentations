# Reveal Presentations Plugin

Generate elegant, minimal HTML presentations with Reveal.js using the Autonomee.ai design system.

## Features

- **Dark, editorial aesthetic** - Dark backgrounds, serif headlines, muted accents
- **12+ slide templates** - Title, features, metrics, pricing, timeline, testimonials, and more
- **Reveal.js powered** - Keyboard navigation, transitions, fullscreen, overview mode
- **Self-contained** - Single HTML file with embedded styles, works offline
- **Customizable** - CSS variables for easy brand adaptation

## Installation

### Option 1: GitHub Install (Recommended)

```bash
claude /plugin install godago/reveal-presentations
```

### Option 2: Local Install

Clone this repository and install from local path:

```bash
git clone https://github.com/godago/reveal-presentations.git
claude /plugin install ./reveal-presentations
```

## Usage

### Quick Start

```
/presentation AI Productivity Tools for Solopreneurs
```

This generates a complete pitch deck with:
- Title slide
- Problem statement
- Solution overview
- Feature cards
- Metrics/traction
- Timeline/roadmap
- Call to action

### Trigger Phrases

The skill responds to these prompts:

| Say This | Get This |
|----------|----------|
| "create presentation about X" | Full presentation |
| "make slides for X" | Full presentation |
| "pitch deck for X" | Full presentation |
| "add slide for X" | Single slide addition |

### Example Prompts

```
Create a pitch deck for TechStartup:
- AI-powered analytics platform
- $2M ARR, 500+ customers
- Pricing: $29/79/199 per month
- Founded 2023, Series A ready
```

```
Make slides for my workshop on prompt engineering
```

```
Create a presentation about the future of AI agents
```

## Design System

### Colors

| Element | Color |
|---------|-------|
| Background | `#0a0a0a` (near black) |
| Accent | `#7b8fa8` (muted steel blue) |
| Text | `#f5f4f0` (warm white) |
| Muted | `#666666` |
| Borders | `#2a2a2a` |

### Typography

- **Headlines:** Playfair Display (serif, italic)
- **Body:** Inter (sans-serif)
- **Code:** JetBrains Mono

### Style Principles

1. No gradients - solid colors only
2. No rounded corners - sharp edges
3. Transparent cards with border outlines
4. Outlined buttons (no fills)
5. Dash markers instead of bullets
6. Section numbers as "01 // SECTION NAME"

## Slide Templates

| Template | Use For |
|----------|---------|
| **Title** | Opening slide with hero headline |
| **Section Divider** | Transitions between major topics |
| **Split Layout** | Text + image side by side |
| **Feature Cards** | 2x2 or 3x3 feature grid |
| **Metrics** | Big numbers row (stats, KPIs) |
| **Comparison** | 3-column comparison table |
| **Numbered List** | Problems, steps, challenges |
| **Timeline** | Roadmap, milestones |
| **Pricing** | 3-tier pricing table |
| **Testimonials** | Quote cards with avatars |
| **Checklist** | Awards, recognition, features |
| **CTA** | Closing with contact info |
| **Code** | Technical slides with syntax highlighting |
| **Workflow** | Process diagrams |

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` / `Arrow` | Next slide |
| `Shift+Space` | Previous |
| `F` | Fullscreen |
| `O` | Overview mode |
| `S` | Speaker notes |
| `B` | Black screen |
| `Esc` | Exit overview |

## Customization

### Change Brand Colors

Edit the CSS variables in your generated presentation:

```css
:root {
  --accent: #your-brand-color;
  --accent-light: #your-light-variant;
}
```

### Add Persistent CTA Buttons

The template supports fixed buttons that appear on all slides:

```html
<!-- Add outside the .reveal container -->
<div style="position: fixed; top: 20px; right: 20px; z-index: 999999;">
  <a href="https://yoursite.com" target="_blank"
     style="padding: 8px 16px; border: 1px solid #7b8fa8; color: #7b8fa8;">
    Your CTA
  </a>
</div>
```

## Deployment

### GitHub Pages (Free Hosting)

1. Create a GitHub repo for your presentation
2. Push the `index.html` file
3. Enable GitHub Pages in Settings
4. Share: `https://username.github.io/repo-name/`

### Vercel

```bash
vercel --prod
```

### Local

Just open `index.html` in any browser.

## License

MIT License - Use freely, modify, share.

---

Created by [Goda](https://youtube.com/@godago) | [Autonomee.ai](https://autonomee.ai)
