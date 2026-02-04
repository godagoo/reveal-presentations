---
name: presentation
description: Generate an interactive HTML presentation with Reveal.js
arguments:
  - name: topic
    description: The topic or outline for the presentation
    required: true
---

# /presentation Command

Generate an elegant, minimal HTML presentation using Reveal.js with the Autonomee.ai design system.

## Instructions

When the user runs `/presentation [topic]`, follow this workflow:

### 1. Parse the Input

Analyze the topic to identify:
- **Title** - Main headline for the presentation
- **Subtitle** - Tagline or description
- **Sections** - Major topics to cover (aim for 6-10 slides)
- **Data points** - Any stats or metrics mentioned
- **Features** - Product capabilities if relevant
- **Call to action** - What should viewers do?

### 2. Plan the Slide Structure

Map content to these slide types:

| Content Type | Template |
|--------------|----------|
| Introduction | Title Slide |
| New section | Section Divider |
| Overview + visual | Split Layout |
| Features/benefits | Feature Cards (2x2) |
| Statistics | Metrics Row |
| Comparisons | 3-Column Comparison |
| Problems/steps | Numbered List |
| Timeline | Timeline |
| Pricing | Pricing Table |
| Testimonials | Testimonials |
| Awards | Checklist |
| Contact/CTA | CTA Slide |

### 3. Generate the Presentation

1. Read the base template from `skills/presentations/Templates/base.html`
2. Read the CSS from `skills/presentations/Styles/autonomee.css`
3. Read slide templates from `skills/presentations/Templates/slides.md`
4. Assemble the HTML by:
   - Replacing `{{TITLE}}` with the presentation title
   - Replacing `{{CUSTOM_CSS}}` with the autonomee.css content
   - Replacing `{{SLIDES}}` with the generated slide sections
   - Replacing `{{CTA_BUTTONS}}` with any persistent buttons (optional)

### 4. Save and Preview

Save the presentation to the user's preferred location (ask if not specified).

Default: `~/Documents/Presentations/{project-name}/index.html`

Then open it in the browser for preview.

## Design Principles

- **Dark background** (#0a0a0a)
- **Serif headlines** (Playfair Display, italic for h1)
- **Sans-serif body** (Inter)
- **Muted steel blue accent** (#7b8fa8)
- **No gradients** - solid colors only
- **No rounded corners** - sharp edges
- **Transparent cards** - border outlines, fill on hover
- **Outlined buttons** - no filled buttons
- **Dash markers** - use "—" instead of dots in lists

## Example

User: `/presentation AI Productivity Tools for Solopreneurs`

Output: 8-10 slide deck with:
1. Title slide with compelling headline
2. Problem slide (challenges solopreneurs face)
3. Solution overview
4. Feature cards (4 key features)
5. Metrics (impact/results)
6. How it works (workflow)
7. Testimonial or social proof
8. CTA with contact info
