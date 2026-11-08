# Unified Product Design & UX Engineering

**A structured, evidence-led design skill for turning product problems and interface observations into better user experiences.**

Unified Product Design & UX Engineering helps AI agents work like a senior product designer and UX engineer: understand the task, inspect the available evidence, shape the experience, preserve meaningful visual context, and validate what can actually be verified.

It is designed for work that goes beyond generating attractive screens — from UX audits and visual redesigns to design systems, accessibility reviews, responsive behavior, and implementation handoff.

> **Current package:** v1.2.0 · Platform-agnostic Markdown skill · Public GitHub repository

## Why this skill?

AI-generated interfaces can look convincing while missing the user problem, breaking familiar patterns, replacing meaningful assets, or claiming quality that has not been tested.

This skill introduces a repeatable way to:

- Start with user goals and product context, not decoration.
- Separate observations, verified facts, assumptions, and recommendations.
- Understand screenshots and interfaces through structured visual analysis.
- Preserve the relationship between assets and the components they belong to.
- Consider accessibility, responsive behavior, and RTL/LTR as part of the design.
- Validate outcomes against explicit criteria without inventing test results.

## What it can help with

| Area | What the skill supports |
|---|---|
| Product discovery & UX strategy | Problem framing, user goals, constraints, opportunities, and success criteria |
| UX architecture | Information architecture, journeys, task flows, and interaction states |
| Visual intelligence | Screen segmentation, hierarchy analysis, component and asset inventories, confidence labels |
| UI/UX redesign | Evidence-led improvements to layout, typography, content, interactions, and visual consistency |
| Design systems | Foundations, tokens, components, variants, states, and usage guidance |
| Accessibility | Keyboard, focus, semantics, contrast, labels, motion, and WCAG 2.2 AA-oriented reviews |
| Responsive & localization | Viewport-aware layouts, touch behavior, RTL/LTR, and real localized content |
| UX engineering | Design-to-code guidance, implementation review, and handoff |
| Quality validation | Repeatable test cases, evidence levels, scoring, and critical-failure gates |

## Adaptive modes

The skill selects the smallest useful set of modes for the task:

`AUTO` · `DISCOVERY` · `STRATEGY` · `UX_ARCHITECTURE` · `VISUAL_INTELLIGENCE` · `DESIGN` · `REDESIGN` · `DESIGN_SYSTEM` · `BUILD` · `AUDIT` · `ACCESSIBILITY` · `RESPONSIVE` · `QA` · `VALIDATION_LAB`

You do not need to select a mode manually. Describe the work naturally and the skill adapts to the request and the tools available.

## How it works

A typical engagement follows this lightweight cycle:

1. **Understand** — clarify the user task, product objective, audience, and constraints.
2. **Inspect** — review the supplied screen, files, application, code, or design evidence.
3. **Define** — identify the problem, findings, assumptions, and acceptance criteria.
4. **Design** — propose a flow, interface, system, or targeted improvement.
5. **Preserve** — keep correct brand assets and their component/instance relationships.
6. **Validate** — check the result against criteria using available tools and evidence.
7. **Deliver** — explain decisions, artifacts, limitations, and next steps.

Not every request needs every step. The skill avoids heavyweight process when a focused answer is enough.

## Visual intelligence & asset preservation

When you provide a screenshot or design reference, the skill can structure its analysis around:

- Screen regions, hierarchy, visible components, and repeated instances.
- Primary and secondary actions, content density, and interaction clues.
- Images, icons, illustrations, logos, and their apparent component relationships.
- Localization, text expansion, RTL/LTR direction, and responsive clues.
- Accessibility cues and what cannot be verified from pixels alone.

Asset decisions are explicit: **Preserve · Adapt · Replace · Remove · Unknown**.

A screenshot does not prove source filenames, component bindings, keyboard behavior, screen-reader output, or responsive breakpoints. Those require source inspection or runtime testing. The skill labels evidence accordingly rather than presenting an inference as a fact.

## Validation Lab (v1.2.0)

The Validation Lab provides a repeatable way to evaluate skill outputs across comparable tasks.

It includes three baseline case types:

1. Existing interface audit.
2. Asset-preserving redesign.
3. New user-flow design.

The method records the input, environment, evidence, and results; scores defined quality dimensions on a 0–4 scale; and applies **Pass / Revise / Block** gates. Critical failures — such as fabricated evidence, unauthorized changes, or loss of meaningful asset relationships — override a numeric score.

Untested criteria must remain **Not tested**. A score is not a substitute for human review.

## Try it

Use prompts like these with an AI agent that supports custom Markdown skills:

- “Audit this dashboard and rank the usability issues by user impact.”
- “Analyze this screenshot. Map its regions, components, assets, and unknowns.”
- “Redesign this screen while preserving the existing logo, icons, and image-to-card mapping.”
- “Review this Arabic interface for RTL issues and responsive risks.”
- “Create a design-system specification from these existing components.”
- “Run the Validation Lab rubric against these redesign results.”

For implementation tasks, provide the repository or relevant source files and explicitly authorize the changes you want made.

## Installation

This repository contains a platform-agnostic Markdown skill package. Keep the master file and its supporting resources together:

- `SKILL.md`
- `references/`
- `workflows/`
- `templates/`

Copy the package folder into the custom-skills location supported by your agent platform, then invoke it using that platform's skill mechanism. Installation paths and metadata conventions vary by platform; adapt the frontmatter only when required.

See [INSTALLATION.md](INSTALLATION.md) for the short installation note.

## Repository structure

```text
.
├── SKILL.md
├── references/          # Method guides and quality standards
├── workflows/           # Repeatable task workflows
├── templates/           # Reusable working documents
├── INSTALLATION.md
├── CHANGELOG.md
└── package-manifest.json
```

**v1.2.0 package contents:** 1 master skill · 18 references · 10 workflows · 11 templates.

## Principles & limitations

- **Evidence over confidence:** distinguish observed, source-verified, behavior-verified, inferred, and unknown.
- **User outcomes over decoration:** visual polish must serve clarity and task completion.
- **Preserve context:** do not replace meaningful assets or detach them from their intended component or data instance without a reason.
- **Accessibility by default:** use WCAG 2.2 AA as a reference target where appropriate, but never claim conformance without sufficient testing.
- **Respect permissions:** audits are read-only; modifying existing work requires authorization; publishing and destructive actions require explicit approval.
- **Be transparent:** the skill can only use the tools, source, and evidence available in the current environment. It does not guarantee that an agent can execute every workflow.

## Contributing

Suggestions, issue reports, and workflow improvements are welcome. When proposing a change, include the problem it solves, a reproducible example where possible, and the expected behavior or acceptance criteria.

## Versioning & license

See [CHANGELOG.md](CHANGELOG.md) for release notes and [package-manifest.json](package-manifest.json) for package metadata.

The repository is publicly viewable. **No open-source license has been granted yet**; unless a license is added, all rights are reserved. Do not assume permission to redistribute, modify, or use the package commercially.

---

Built as an evolving experiment in combining product design judgment, UX engineering, and AI-assisted workflows.
