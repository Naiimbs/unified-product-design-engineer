# Visual asset preservation and component context

## Principle
A redesign must preserve the semantic relationship between a visual asset and the UI component it belongs to. An image or icon is not decoration alone: it can communicate status, category, brand, identity, content, or action.

## Asset inventory
For each affected component, identify component name and instance/record identity; asset type; source (component prop, design library, asset manifest, CMS, file path, URL, or screenshot-only observation); semantic purpose; crop, focal point, aspect ratio, dimensions, color treatment and responsive behavior; and accessibility metadata.

## Decision rules
- **Preserve:** asset is correct, approved, and still serves the same meaning.
- **Adapt:** asset remains correct but needs controlled crop, scale, tint, container, or responsive treatment.
- **Replace:** asset is incorrect, obsolete, low quality, unavailable, or conflicts with approved direction. Select a semantically equivalent and brand-compatible replacement.
- **Remove:** asset is redundant or harms comprehension, and removal is justified.
- **Unknown:** source or meaning cannot be established; request confirmation or retain the current asset until verified.

## Component binding rules
1. Keep each asset associated with its original component and data instance unless the design explicitly changes that relationship.
2. For repeated notifications/cards/list items, do not accidentally share one instance's image across all items. Preserve data-driven per-instance bindings.
3. Shared component changes must be checked across all consumers; local instance changes must not leak globally.
4. Verify assets across component variants, interaction states, responsive breakpoints, and localized versions.
5. Preserve image semantics and accessibility metadata; decorative images should not gain redundant alt text, and meaningful images need useful alternatives.

## Discovery tools
Inspect rendered screens, DOM/component source, props, CSS, design files, asset manifests, CMS records, and approved icon libraries where available. Search only when the existing asset cannot be found or is unsuitable. Generate new imagery only when requested or clearly authorized. Do not invent provenance or use generated imagery to impersonate a real product screenshot, logo, customer image, or functional icon.

## Evidence and limitations
A screenshot can show which asset appears in a component, but usually cannot prove its source path, data binding, or reuse scope. Label screenshot-only conclusions as visual inference. Confirm component bindings from source or design metadata before claiming implementation fidelity.

## Review checklist
- Is the asset semantically correct for the component?
- Is the correct asset associated with the correct item/record?
- Does the asset preserve product and brand identity?
- Are crop, scale, contrast, and focal point intentional?
- Are all relevant states and responsive layouts covered?
- Are alt text and accessible semantics correct?
- Could the change unintentionally affect other instances?
- Is the asset mapping verified, or only visually inferred?
