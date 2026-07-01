# UM PhD Interview PPT Template (WorkBuddy Skill)

A reusable **WorkBuddy Skill** built from a University of Macau (中国澳门大学)
PhD interview presentation template, originally exported from WPS Office as a
frame-based HTML deck (22 slides, 16:9).

## What's Inside

```
um-phd-interview-ppt-template/
├── SKILL.md                          # Skill entry point — metadata + usage workflow
├── README.md                         # This file
├── .gitignore
├── references/
│   └── design-system.md              # Extracted design system (colors, fonts, slide map)
└── assets/
    └── template/                     # Complete original WPS HTML export
        ├── index.html                # Entry point — open in browser to preview
        └── template-files/           # 253 supporting files (slides, images, masters, CSS)
```

## Design System at a Glance

| Token | Value | Usage |
|-------|-------|-------|
| Primary navy | `#002C55` / `#003A65` / `#031E41` | Brand backgrounds, titles, sidebars |
| Accent gold | `#FFD546` | Highlights, divider bars, emphasis |
| Display font | Futura Md BT | Slide titles, section headers |
| Body font (EN) | Calibri | English body text |
| Body font (CN) | OPPOSans M / 思源黑体 CN | Chinese body text |

Full details in [`references/design-system.md`](references/design-system.md).

## Slide Structure (22 slides)

1. Title slide (campus photo + navy sidebar)
2. Outline
3. Personal profile
4. Honors & awards
5. Practical skills (icon grid)
6. Section divider — Research Experience
7. Project cards
8. Timeline / flow
9–15. Research deep-dives & data analysis
16. Section divider — Research Proposal / Why PhD
17–21. Proposal & motivation
22. Thank you

## How to Use

### As a WorkBuddy Skill

Copy (or symlink) this directory to `~/.workbuddy/skills/um-phd-interview-ppt-template/`.
WorkBuddy will auto-discover it. The skill triggers when you ask WorkBuddy to
create or customize a PhD interview / academic presentation in the UM style.

### Preview the Original Deck

Open `assets/template/index.html` in a browser. For the full framed navigation
view, open `assets/template/template-files/frame.htm` directly.

### Build a New Presentation

Ask WorkBuddy something like:

> "用 UM 澳门大学 PhD 面试模板帮我做一份博士面试演示文稿，主题是 [你的研究方向]"

WorkBuddy will load this skill, reference the design system, and generate a
new HTML presentation matching the UM visual identity.

## License

This template is provided for personal/academic use. The University of Macau
name and logo are trademarks of their respective owners and are included here
only as part of the original presentation template.
