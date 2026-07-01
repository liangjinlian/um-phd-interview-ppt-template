---
name: um-phd-interview-ppt-template
description: 'University of Macau (中国澳门大学) PhD interview presentation template, exported from WPS Office as a frame-based HTML deck (22 slides). This skill should be used when the user asks to create, generate, or customize a PhD interview / academic defense / research proposal presentation in the UM visual style, or when the user references the "UM 澳门大学 PhD 面试模板" / "学院 logo 版" template. It provides the complete original HTML export as a referenceable asset plus an extracted design system (colors, typography, slide structure) so new presentations can be produced matching the established look.'
agent_created: true
---

# UM PhD Interview PPT Template

## Overview

A reusable presentation template originating from a University of Macau
(中国澳门大学) PhD interview deck. The original was built in WPS Office and
exported as a frame-based HTML presentation (22 slides, 16:9). This skill
bundles the full original export as a visual reference and documents the
extracted design system so new PhD interview / academic presentations can be
produced that match the established UM look.

## When to Use

Trigger this skill when the user requests any of the following:

- Create a PhD interview presentation in the UM Macau style.
- Generate an academic defense / research proposal deck using the "学院 logo 版"
  template.
- Customize or fill in the existing UM PhD interview template.
- Reference the UM visual identity (deep-navy + gold) for a new slide deck.

## Asset Layout

The complete original WPS HTML export lives under `assets/template/`:

```
assets/template/
├── index.html              # Entry point — open this to preview the deck
└── template-files/         # 253 supporting files
    ├── frame.htm           # Frameset: outline (left) + slide (right) + nav (bottom)
    ├── slide0001.htm ... slide0022.htm   # 22 individual slides
    ├── outline.htm         # Navigation outline
    ├── master03/04/05.htm + .xml + _stylesheet.css   # Slide masters
    ├── pres.xml            # Presentation manifest
    ├── script.js           # Navigation logic
    ├── image001.jpeg ...   # All images (campus photo, UM logo, charts, icons)
    └── buttons.gif, *.wmf, *.mso   # UI sprites & legacy vector assets
```

To preview the original deck, open `assets/template/index.html` in a browser.
Modern browsers render the non-frame fallback; for the full framed view use
Internet Explorer / Edge legacy mode or open `template-files/frame.htm`
directly.

## Design System

The full extracted design system (color palette, typography, slide-by-slide
structure, layout patterns) is documented in `references/design-system.md`.
Load that reference before generating new slides to ensure visual consistency.

Key tokens at a glance:

| Token | Value | Usage |
|-------|-------|-------|
| Primary navy | `#002C55` / `#003A65` / `#031E41` | Brand backgrounds, titles, sidebars |
| Accent gold | `#FFD546` | Highlights, divider bars, emphasis |
| Body text | `#000000` / `#404040` | Primary / secondary text |
| Light surfaces | `#FFFFFF` / `#F2F2F2` / `#E7E6E6` | Content backgrounds, cards |
| Display font | Futura Md BT | Slide titles, section headers |
| Body font (EN) | Calibri | English body text |
| Body font (CN) | OPPOSans M / 思源黑体 CN Regular | Chinese body text |

## Workflow

### 1. Preview the original template

Open `assets/template/index.html` (or `template-files/frame.htm`) in a browser
to study the existing layout, color usage, and slide sequencing before
generating new content.

### 2. Load the design reference

Read `references/design-system.md` for the complete color palette, typography
scale, per-slide structure map (22 slides), and reusable layout patterns
(title slide, section divider, content+sidebar, project cards, timeline,
data-analysis grid, thank-you slide).

### 3. Generate a new presentation

Produce a single self-contained HTML file (or a set of slides) that reproduces
the UM look:

- Use the 16:9 aspect ratio (960×540 internal coordinate space, same as the
  original `p:slide coordsize="960,540"`).
- Apply the primary navy as the dominant background or sidebar color, with
  gold accents for dividers and highlights.
- Use Futura Md BT / Calibri for English; fall back to OPPOSans or 思源黑体
  for Chinese (include system-font fallbacks since these may not be installed
  everywhere).
- Follow the 22-slide narrative structure from the design reference, adapting
  section count to the user's content.
- Place the UM logo (available as `template-files/image003.png`) in the
  title-slide corner when appropriate.

### 4. Fill in placeholder content

The original template uses placeholder text (`[Your Name]`, `Click here to
enter a brief introduction`, `PROJECT NAME`, etc.). Replace every placeholder
with the user's actual content. Common fields:

- Title slide: presentation title, presenter name, instructor/advisor, date.
- Profile slide: full name, nationality, current status, core research
  interests.
- Education / Awards / Skills / Research Experience / Research Proposal /
  Why PhD / Thank You sections.

### 5. Deliver

Output the final presentation as an HTML file the user can open in a browser,
or as individual slide HTML files. If the user needs a `.pptx` instead,
generate the HTML first then advise importing into PowerPoint/WPS, or use a
python-pptx workflow to rebuild the deck programmatically.
