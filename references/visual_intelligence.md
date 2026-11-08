# Visual intelligence: screen understanding and asset mapping

## Goal
Convert rendered visual input into a structured, uncertainty-aware model of the interface. Visual interpretation is not equivalent to source-code understanding.

## Inspection sequence
1. **Orient:** identify product/page, user task, platform, viewport, language/direction, and capture conditions.
2. **Segment:** divide the screen into regions, components, repeated instances, overlays, and navigation.
3. **Read hierarchy:** identify primary action, headings, content groups, status, emphasis, density, alignment, and visual flow.
4. **Inventory components:** record visible name/role, boundaries, parent/child relationships, variants, states, and repeated instances. Use neutral IDs when exact component names are unknown.
5. **Inventory assets:** record icon/image/illustration/logo/avatar, visible meaning, owning component and instance, dimensions/crop/focal point, and likely source. Mark source and binding as unknown unless inspected.
6. **Inspect interaction clues:** distinguish visible affordances from verified behavior. Test only with authorized tools and safe read-only actions.
7. **Check content and localization:** labels, truncation, long text, mixed-direction content, number/date formatting, and text expansion.
8. **Check responsive evidence:** compare actual captures at recorded dimensions. Never infer responsive behavior from a single screenshot.
9. **Synthesize:** produce a screen map, component/asset map, issues, assumptions, and confidence.
10. **Recommend:** connect each proposed change to a user need, observed issue, or explicitly labeled hypothesis.

## Confidence labels
- **Observed:** directly visible in supplied or captured screen.
- **Source-verified:** confirmed from code, design metadata, DOM, props, or asset manifest.
- **Behavior-verified:** action or state was executed and observed.
- **Inferred:** plausible interpretation from appearance, not confirmed.
- **Unknown:** insufficient evidence.

## Output schema
| Region / component ID | Visible role | Instance | Asset | State | Evidence | Confidence |
|---|---|---|---|---|---|---|

Also provide:
- viewport and capture details;
- primary user task and visual hierarchy;
- interaction assumptions vs verified behavior;
- responsive and localization observations;
- accessibility cues and checks not possible from pixels;
- prioritized opportunities and unresolved questions.

## Limitations
A screenshot alone cannot reliably prove DOM semantics, component boundaries, asset filenames, data bindings, keyboard behavior, screen-reader output, hidden states, responsive breakpoints, or actual interaction. State these limits explicitly. Do not infer source structure from visual similarity.
