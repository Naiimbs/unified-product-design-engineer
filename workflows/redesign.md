# Workflow: redesign

1. Set the redesign objective, target users, scope, and what must remain unchanged.
2. Inspect the current experience at the available viewports. Record what was actually observed.
3. Map screens to components and instances; identify shared/reused components.
4. Inventory visual assets used by affected components: icons, illustrations, images, logos, avatars, thumbnails, and media. Trace source paths or bindings when source access exists; otherwise label visual inference clearly.
5. For each asset, decide preserve, adapt, replace, remove, or unknown. Preserve semantically correct and brand-approved assets by default.
6. Separate confirmed usability/UI defects from aesthetic preferences and prioritize by user impact.
7. Explore alternatives and trade-offs. Keep each retained or replacement asset bound to the same intended component and correct instance. Check component variants and interaction states.
8. Specify revised flow, hierarchy, layout, typography, spacing, visual states, responsive behavior, and asset mapping.
9. Validate the redesigned component against the original meaning, product brand, accessibility, and user task. Verify asset-to-component mapping after implementation where possible.
10. Deliver rationale, before/after evidence, asset mapping, limitations, and prioritized roadmap.

## Asset preservation acceptance checks
- [ ] Correct existing image/icon is retained in the correct component when still appropriate.
- [ ] No unrelated image or icon has been substituted.
- [ ] Shared component instances and instance-specific assets are distinguished.
- [ ] Relevant default, hover, focus, selected, loading, success, warning, error, disabled, and responsive states are checked where applicable.
- [ ] Alt text, accessible names, decorative semantics, crop, focal point, and contrast are reviewed.
- [ ] Asset source/binding verification is distinguished from visual inference.

If source or asset provenance cannot be inspected, explicitly state that limitation rather than claiming the original asset mapping was confirmed.
