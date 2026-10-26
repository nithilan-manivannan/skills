# Skills

**A curated collection of 17 agent skills for OpenCode, spanning design systems, frontend engineering, image generation, and workflow utilities.**

## Overview

This repository is a structured library of `SKILL.md` definitions built to extend the capabilities of AI coding agents operating within OpenCode. Each skill encapsulates a distinct discipline, from taste driven frontend design to image only generation pipelines, giving agents the precision, consistency, and craft that raw prompting cannot reliably deliver on its own.

The goal of the collection is simple: eliminate generic, templated output, and replace it with deliberate, well made results across design, code, and visual generation.

Alongside the skill folders, the repo carries:

- `llms.txt`: a one line, machine readable index for agent discovery. It covers 14 of the 17 skills today; the remaining three (laws-of-ux, web-designer, webcore-analyzer) are described in the tables below.
- `index.html`: a showroom page ("Maison des Skills") that presents the collection as an acquirable volume: porcelain paper, gold accents, and a small catalogue site for browsing the skills locally.
- Supporting assets, references, and scripts inside the skill folders themselves.

## Design and frontend skills

| Skill | What it does |
|---|---|
| **taste-skill** | The default design skill, currently in its second experimental generation. Reads a creative brief, infers the design language, and tunes three dials (Variance, Motion, Density) to ship landing pages, portfolios, and redesigns that avoid a templated look. Includes brief inference, design system mapping, an em dash ban, GSAP code skeletons, and a hard rules preflight check. In active iteration toward v2 stable. |
| **taste-skill-v1** | The original version of taste-skill, preserved for projects that depend on its exact prior behavior. The active default is taste-skill. |
| **gpt-tasteskill** | Elite frontend design and GSAP motion skill aimed at premium, deterministic, anti-slop output, with Awwwards level structure and motion discipline. |
| **image-to-code-skill** | Image first frontend skill: generates premium website design references, analyzes them in depth, then implements matching code. |
| **redesign-skill** | Purpose built for upgrading existing projects through systematic auditing and correction of design problems, without breaking function. |
| **soft-skill** | Cultivates an expensive, soft aesthetic: premium typography, generous whitespace, layered depth, and smooth motion. |
| **minimalist-skill** | Enforces clean editorial interfaces in the spirit of Notion and Linear, with strict monochrome palettes. |
| **brutalist-skill** (beta) | Raw mechanical interfaces: Swiss typography, rigid grids, extreme scale contrast. |
| **stitch-skill** | Google Stitch compatible semantic design rules, producing a DESIGN.md that enforces premium AI driven UI. |
| **design-language** | Applies a named UI design language (glassmorphism, neumorphism, brutalism, Material 3, cyberpunk, Y2K, Bauhaus, and 220 plus more) consistently across a codebase. Tokens first workflow, a large catalog of implementation specs, WCAG contrast checks, Tailwind fragments, starter themes, and a consistency drift audit. Sourced from the claude-artisan repository. |
| **laws-of-ux** | Applies the laws and principles of user experience design as concrete rules for interface work, from Fitts to the Zeigarnik effect. |
| **webcore-analyzer** | Analyzes websites for old web revival aesthetics (webcore, neo Geocities, Y2K) and drives a revival style audit. |
| **web-designer** | Design level web craft guidance: color, typography, patterns, interactive features, and motion playbooks, gated behind an explicit opt in. |

## Image generation skills

| Skill | What it does |
|---|---|
| **imagegen-frontend-web** | Generates premium website design reference imagery, one image per section. Image only, no code output. |
| **imagegen-frontend-mobile** | Generates premium mobile app screen concepts and flows inside framed device mockups. Image only. |
| **brandkit** | Generates brand identity imagery: logo concepts, guidelines boards, identity decks, and mockup art. Image only. |

## Utility skills

| Skill | What it does |
|---|---|
| **output-skill** | Stops an agent from going lazy mid answer: complete code, no placeholder comments, no skipped blocks. |

## Getting started

1. **Clone the repository**

```bash
git clone https://github.com/nithilan-manivannan/skills
```

2. **Pick a skill** from the tables above that matches the job.

3. **Install it for OpenCode** by copying the skill's folder into your OpenCode skills directory, so its `SKILL.md` is discoverable at runtime:

```bash
# for the design language skill, for example
cp -r design-language ~/.config/opencode/skills/design-language
```

4. **Combine skills** where appropriate. Skills are designed to complement one another: pair `design-language` with `output-skill`, or `redesign-skill` with `laws-of-ux`.

The `llms.txt` file gives agents a compact, one line per skill index they can parse directly.

## Repository structure

```
skills/
├── brandkit/
├── brutalist-skill/
├── design-language/
├── gpt-tasteskill/
├── image-to-code-skill/
├── imagegen-frontend-mobile/
├── imagegen-frontend-web/
├── laws-of-ux/
├── minimalist-skill/
├── output-skill/
├── redesign-skill/
├── soft-skill/
├── stitch-skill/
├── taste-skill/
├── taste-skill-v1/
├── web-designer/
├── webcore-analyzer/
├── index.html           # showroom page
└── llms.txt             # agent readable index
```

Each directory is self contained: a `SKILL.md` plus any references, scripts, or assets the skill needs. `design-language` is by far the largest, with a full references tree, scripts, and hundreds of starter themes and implementation specs.

## Contributing

This collection is under active development, most notably with taste-skill progressing toward a stable v2. Suggestions, refinements, and new skill proposals are welcome through issues and pull requests.

## License

Proprietary. All rights reserved by the repository owner.
