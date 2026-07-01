# UM PhD Interview Template — Design System

Extracted from the original WPS Office HTML export (22 slides, 16:9).
Use this reference when generating new presentations that must match the
University of Macau (中国澳门大学) PhD interview visual style.

## 1. Color Palette

Colors are ordered by frequency of use in the original deck.

### Brand / Structural Colors

| Role | Hex | Notes |
|------|-----|-------|
| Primary navy | `#002C55` | Title-slide sidebar, key shape fills |
| Deep navy | `#003A65` | Section dividers, header bars (most used brand tone) |
| Darkest navy | `#031E41` | Footer bars, dark panels |
| Royal blue | `#002060` | Alternate dark backgrounds |
| Mid blue | `#003D7C` | Secondary structural elements |
| Accent gold | `#FFD546` | Divider lines, highlight bars, emphasis text backgrounds |
| Link blue | `#267BB4` / `#4874CB` | Hyperlinks, chart series |

### Text & Neutral Colors

| Role | Hex | Notes |
|------|-----|-------|
| Primary text | `#000000` | Body copy on light backgrounds |
| Secondary text | `#404040` | Captions, supporting text |
| White | `#FFFFFF` | Text on dark backgrounds, primary canvas |
| Light gray | `#F2F2F2` | Card backgrounds, alt rows |
| Mid light gray | `#E7E6E6` | Subtle separators, panel fills |
| Light blue tint | `#DAE3F5` | Info boxes, table headers |
| Soft pink | `#ECCDD5` | Occasional accent (charts) |

## 2. Typography

### Font Stack

| Role | Font | Fallback |
|------|------|----------|
| Display / Titles | Futura Md BT | `"Trebuchet MS", Verdana, sans-serif` |
| Body (English) | Calibri | `"Segoe UI", Arial, sans-serif` |
| Body (Chinese) | OPPOSans M | `"Microsoft YaHei", "PingFang SC", sans-serif` |
| Headings (Chinese) | OPPOSans H / 思源黑体 CN Bold | `"Microsoft YaHei", sans-serif` |
| Serif accent (CN) | 思源宋体 CN Heavy | `"SimSun", serif` |
| Monospace/legacy | Arial | system default |

> Note: Futura Md BT, OPPOSans, and 思源黑体 are not universally installed.
> Always provide the fallback chain above when generating new HTML.

### Type Scale (relative to 16px base)

| Size | Usage |
|------|-------|
| 244% | Largest display (cover numbers) |
| 200% | Title-slide main title |
| 178% | Section divider titles |
| 156% | Slide titles |
| 133% | Sub-headings |
| 111% | Emphasized body / lead text |
| 100% | Standard body |
| 89% | Default body (most common) |
| 58% | Fine print / footers |

## 3. Slide Canvas

- **Aspect ratio:** 16:9
- **Internal coordinate space:** 960 × 540 (PowerPoint/WPS points)
- **Display size:** 534 × 300 px (scaled in browser via `_RSW()`)
- **Background:** white by default; dark navy for section dividers and the
  title slide sidebar

## 4. Slide Structure Map (22 slides)

| # | Slide | Type | Key Content |
|---|-------|------|-------------|
| 1 | Title | Cover | "PRESENTATION TITLE GOES HERE" + Presenter / Instructor / Date; campus photo right, navy sidebar left, UM logo top-left |
| 2 | Outline | Agenda | Education Background · Research Experience · Research Interests & Why PhD |
| 3 | Personal Profile | Content+photo | Full Name / Nationality · Current status · Core Research Interests |
| 4 | Honors & Awards | List/cards | National Scholarship, competition prizes (two-column repeat) |
| 5 | Practical Skills | Icon grid | Lab equipment, coding (Python/R), GIS software, experiments |
| 6 | Section Divider | Divider | "Research Experience" on navy background |
| 7 | Project Cards | 3-card grid | PROJECT NAME + brief introduction placeholders |
| 8 | Timeline / Flow | Timeline | FLOW → TIME horizontal sequence |
| 9 | Data Analysis | Content | Methodology + brief introduction blocks |
| 10 | Content | Text+visual | Brief introduction with supporting visual |
| 11–15 | Research detail | Mixed | Project deep-dives, results, figures |
| 16 | Section Divider | Divider | Research Proposal / Why PhD transition |
| 17–21 | Proposal & Motivation | Content | Research plan, motivation, future plans |
| 22 | Thank You | Closing | Closing slide with UM branding |

## 5. Reusable Layout Patterns

### Pattern A — Title Slide (slide 1)
- Left ~53%: navy polygon sidebar with white title text + gold divider bar.
- Right ~47%: full-bleed campus photograph.
- Top-left corner: UM logo overlay.
- Bottom-left: presenter / instructor / date in Calibri, gold accent bar
  behind the presenter line.

### Pattern B — Section Divider (slides 6, 16)
- Full navy background (`#003A65` or `#031E41`).
- Large white display title centered or left-aligned.
- Optional gold horizontal rule beneath the title.

### Pattern C — Content + Sidebar
- Thin navy vertical strip on the left edge (brand reinforcement).
- White content area with title in navy, body in black/gray.
- Gold accent line under the slide title.

### Pattern D — Card Grid (slide 7)
- 3 equal cards with navy header strip + white body.
- Each card: project name (bold) + 2–3 lines of description.
- Subtle gray border or shadow separating cards.

### Pattern E — Timeline (slide 8)
- Horizontal flow with circular/numbered nodes.
- Gold connecting line; navy node fills with white numbers.
- Labels above (FLOW) and below (TIME) the axis.

### Pattern F — Icon Skills Grid (slide 5)
- 2×2 or 2×3 grid of skill tiles.
- Each tile: icon + label + one-line description.
- Light gray tile backgrounds (`#F2F2F2`) with navy text.

### Pattern G — Thank You (slide 22)
- Navy full-bleed background.
- Large "THANK YOU" in Futura Md BT, white.
- UM logo + contact info in the lower corner.

## 6. Key Asset Files

| File | Description |
|------|-------------|
| `template-files/image003.png` | UM (University of Macau) logo — place on title & closing slides |
| `template-files/image001.jpeg` | Campus photograph — title slide right side |
| `template-files/image002.png` | Decorative polygon overlay (title slide) |
| `template-files/buttons.gif` | Navigation sprite (prev/next/notes/fullscreen) |
| `template-files/master05_stylesheet.css` | Primary master stylesheet — reference for exact CSS |

## 7. Generation Checklist

When producing a new presentation, verify:

- [ ] 16:9 canvas with 960×540 coordinate space.
- [ ] Primary navy (`#002C55`–`#031E41` range) dominates structural elements.
- [ ] Gold (`#FFD546`) used sparingly for dividers and emphasis only.
- [ ] Futura Md BT for titles (with sans-serif fallback); Calibri for body.
- [ ] Chinese text uses OPPOSans / 思源黑体 with Microsoft YaHei fallback.
- [ ] UM logo present on title and closing slides.
- [ ] All placeholder text (`[Your Name]`, `Click here to enter...`) replaced.
- [ ] Narrative follows: Title → Outline → Profile → Education → Awards →
      Skills → Research Experience → Projects → Data Analysis → Proposal →
      Why PhD → Thank You.
