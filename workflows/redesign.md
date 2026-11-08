# Workflow: redesign

1. Set redesign objective, target users, scope, success criteria, and what must remain unchanged.
2. Capture baseline at actual available viewports. Record dimensions, environment, locale, and evidence source.
3. Apply Visual Intelligence: segment regions, identify visible components/instances, hierarchy, states, and interaction clues. Label observations, source-verified facts, inferences, and unknowns.
4. Map screens to components and instances; identify shared/reused components.
5. Inventory visual assets used by affected components: icons, illustrations, images, logos, avatars, thumbnails, and media. Trace source paths/bindings when source access exists; otherwise label visual inference clearly.
6. For each asset, decide preserve, adapt, replace, remove, or unknown. Preserve semantically correct and brand-approved assets by default.
7. Separate confirmed usability/UI defects from aesthetic preferences and prioritize by user impact, confidence, and effort.
8. Explore alternatives and trade-offs. Keep each retained/replacement asset bound to the same intended component and correct instance. Check relevant variants and interaction states.
9. Specify revised flow, hierarchy, layout, typography, spacing, visual states, responsive behavior, accessibility, and asset mapping.
10. Validate the redesign against original meaning, product brand, user task, acceptance criteria, and evidence. Verify asset-to-component mapping after implementation where possible.
11. Deliver rationale, before/after evidence, asset mapping, tested/not-tested items, limitations, and prioritized next steps.

## Asset preservation acceptance checks
- [ ] Correct existing image/icon remains in the correct component when still appropriate.
- [ ] No unrelated image or icon has been substituted.
- [ ] Shared component instances and instance-specific assets are distinguished.
- [ ] Relevant states and responsive layouts are checked where applicable.
- [ ] Alt text, accessible names, decorative semantics, crop, focal point, and contrast are reviewed.
- [ ] Asset source/binding verification is distinguished from visual inference.

## Evidence and validation
For substantial redesigns, record the baseline and final viewport, evidence level, and any checks not possible. Use `templates/visual_inventory.md` for the screen/asset inventory. If comparing skill versions or evaluating repeatability, use `workflows/validation_lab.md` and `references/validation_method.md`.

If source or asset provenance cannot be inspected, state that limitation rather than claiming the original asset mapping was confirmed.
