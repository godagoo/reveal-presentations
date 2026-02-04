---
name: Presentations
description: Generate interactive HTML presentations with Reveal.js. USE WHEN user wants to create pitch decks, slide presentations, or interactive HTML slides.
---

# Presentations Skill

Generate elegant, minimal HTML presentations using Reveal.js with the Autonomee.ai design system - dark background, serif headlines, muted accents.

## Triggers

| User Says | Action |
|-----------|--------|
| "create presentation", "make slides", "pitch deck" | Generate full presentation |
| "presentation about X" | Generate presentation on topic |
| "add slide for X" | Add single slide to existing |
| "preview presentation" | Open in browser |

---

## Output Location

All presentations save to:
```
~/Documents/Presentations/
```

### File Naming
```
{project-name}/
  index.html          # Main presentation file
  assets/             # Images, if any
```

---

## Generation Workflow

### Step 1: Content Analysis

Parse user input to identify:
- **Title** - Main headline
- **Subtitle** - Tagline or description
- **Sections** - Major topics to cover
- **Data points** - Stats, metrics, numbers
- **Features** - Product capabilities
- **Social proof** - Testimonials, awards

### Step 2: Slide Planning

Map content to slide types:

| Content Type | Slide Template |
|--------------|----------------|
| Introduction | Title Slide |
| New section | Section Divider |
| Overview with image | Split Layout |
| Features/benefits | Feature Cards (2x2) |
| Statistics | Metrics Row |
| Comparisons | 3-Column Comparison |
| Problems/challenges | Numbered List |
| Timeline/roadmap | Timeline |
| Pricing | Pricing Table |
| Testimonials | Testimonials |
| Awards/press | Checklist |
| Contact/CTA | CTA Slide |

### Step 3: HTML Assembly

```javascript
// Pseudocode for assembly
const slides = contentSections.map(section => {
  const template = selectTemplate(section.type);
  return populateTemplate(template, section.content);
});

const presentation = baseTemplate
  .replace('{{TITLE}}', title)
  .replace('{{CUSTOM_CSS}}', autonomeeCSS)
  .replace('{{SLIDES}}', slides.join('\n'));
```

### Step 4: Save & Preview

```bash
# Create project folder
mkdir -p ~/Documents/Presentations/{project}/

# Save HTML file
# Open in browser
open ~/Documents/Presentations/{project}/index.html
```

---

## Slide Templates Reference

See `Templates/slides.md` for full HTML templates:

1. **Title/Cover** - Hero slide with gradient
2. **Section Divider** - Transition between sections
3. **Split Layout** - Text + Image side by side
4. **Feature Cards** - 2x2 or 3x3 grid
5. **Metrics** - Big numbers row
6. **Comparison** - 3-column options
7. **Numbered List** - Problems/steps
8. **Timeline** - Roadmap milestones
9. **Pricing** - 3-tier pricing table
10. **Testimonials** - Quote cards
11. **Checklist** - Awards/recognition
12. **CTA** - Closing with contact info

---

## Design System

### Colors (CSS Variables)

| Variable | Hex | Usage |
|----------|-----|-------|
| `--bg-dark` | `#0a0a0a` | Main background |
| `--bg-card` | `#111111` | Card backgrounds |
| `--accent` | `#7b8fa8` | Primary accent (muted steel blue) |
| `--accent-light` | `#9bb0c9` | Light accent |
| `--text-primary` | `#f5f4f0` | Headlines (warm white) |
| `--text-secondary` | `#a8a8a8` | Body text |
| `--text-muted` | `#666666` | Subtle text |
| `--border` | `#2a2a2a` | Borders |

### Typography

- **Headlines:** Playfair Display (serif, italic for h1)
- **Body:** Inter (sans-serif)
- **Code:** JetBrains Mono (monospace)
- **Style:** Light weight (400), elegant, editorial

### Critical CSS Requirements (Reveal.js)

**MUST INCLUDE** to prevent white borders/flicker:

```css
/* These styles are REQUIRED - prevents white background bleed */
html, body {
  background: var(--bg-dark) !important;
  color: var(--text-primary);
  margin: 0;
  height: 100%;
}

.reveal-viewport {
  background: var(--bg-dark) !important;
  background-image: /* grid pattern */ !important;
  background-size: 60px 60px !important;
}
```

---

### Clickable Buttons (CRITICAL)

**Reveal.js blocks ALL click events inside `<div class="reveal">`.**

#### The Solution

**Place clickable elements OUTSIDE `<div class="reveal">` with `position: fixed`.**

The `base.html` template includes a `{{CTA_BUTTONS}}` placeholder for this:

```html
<!-- In base.html - buttons go AFTER the reveal container -->
</div>  <!-- End of .reveal -->

{{CTA_BUTTONS}}
</body>
```

#### Example CTA Buttons

```html
<!-- Top-right persistent buttons (all slides) -->
<div style="position: fixed; top: 20px; right: 20px; display: flex; gap: 12px; z-index: 999999;">
  <a href="https://example.com" target="_blank"
     style="padding: 8px 16px; font-size: 12px; text-decoration: none;
            border: 1px solid #7b8fa8; color: #7b8fa8;
            text-transform: uppercase; letter-spacing: 0.1em;">
    Link 1
  </a>
  <a href="https://example.com" target="_blank"
     style="padding: 8px 16px; font-size: 12px; text-decoration: none;
            border: 1px solid #f5f4f0; color: #f5f4f0;
            text-transform: uppercase; letter-spacing: 0.1em;">
    Link 2
  </a>
</div>
```

---

### Key Style Principles

1. **No gradients** - Solid colors only
2. **No rounded corners** - Sharp edges
3. **Transparent cards** - Border outlines, fill on hover
4. **Outlined buttons** - No filled buttons
5. **Dash markers** - Use `—` instead of dots in lists
6. **Section numbers** - Format as `01 // SECTION NAME`

---

## Customization

### Brand Colors

To customize for a different brand, modify CSS variables:

```css
:root {
  --accent: #YOUR_PRIMARY;
  --accent-light: #YOUR_LIGHT;
  --accent-glow: rgba(YOUR_R, YOUR_G, YOUR_B, 0.15);
}
```

---

## Keyboard Shortcuts (Reveal.js)

| Key | Action |
|-----|--------|
| `Space` / `Arrow` | Next slide |
| `Shift+Space` | Previous slide |
| `F` | Fullscreen |
| `S` | Speaker notes |
| `O` | Overview mode |
| `Esc` | Exit overview |
| `B` | Black screen |

---

## Deployment Options

### Local Preview
```bash
open index.html
```

### GitHub Pages
1. Create GitHub repo
2. Push presentation files
3. Enable GitHub Pages in repo settings
4. Share URL: `https://username.github.io/repo-name/`

### Vercel
```bash
vercel --prod
```

---

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | This documentation |
| `Templates/base.html` | Base HTML structure |
| `Templates/slides.md` | All slide templates |
| `Styles/autonomee.css` | Autonomee.ai theme CSS |
