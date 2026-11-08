# Validation method and scoring rubric

## Evidence levels
- **E0 — No evidence:** unsupported claim or no artifact.
- **E1 — Visual indication:** screenshot or rendered output; source behavior/binding not confirmed.
- **E2 — Reproducible observation:** repeatable steps and captured behavior in a stated environment.
- **E3 — Source-backed:** relevant code, design metadata, token, component prop, or configuration inspected.
- **E4 — Executed verification:** test, assistive-technology check, browser interaction, or measurement actually executed and recorded.

Evidence level is claim-specific. A screenshot may be E1 for asset provenance but E2 for visible layout at the captured viewport.

## Scoring scale
Score each dimension from 0 to 4:
- **0 — Missing / harmful:** absent, incorrect, or creates a serious issue.
- **1 — Weak:** major gaps; little usable evidence.
- **2 — Partial:** some useful work, but important gaps remain.
- **3 — Good:** meets the stated requirement with adequate evidence.
- **4 — Strong:** complete, coherent, and verified beyond the minimum requirement.

## Core dimensions
1. **Task and user alignment:** user goal, context, task coverage, and business constraints.
2. **UX quality:** flow clarity, cognitive load, feedback, error/recovery, and consistency.
3. **Visual quality:** hierarchy, typography, spacing, contrast, content, and brand fit.
4. **Asset continuity:** correct asset-to-component and instance mapping, semantic integrity, and justified changes.
5. **Accessibility:** semantics, names, keyboard/focus, contrast, target size, motion, and relevant assistive technology checks.
6. **Responsive behavior:** actual viewport coverage, reflow, overflow, touch behavior, and responsive asset treatment.
7. **Implementation quality:** fit with existing architecture, component reuse, maintainability, and scope control. Mark Not applicable for non-build cases.
8. **Evidence integrity:** distinction between observed, inferred, assumed, proposed, and tested; no fabricated claims.
9. **Handoff clarity:** actionable specifications, acceptance criteria, limitations, and next steps.

## Weighted score
For comparable runs, use the relevant dimensions only and publish weights before scoring. Suggested default weights:
- Task alignment 15%
- UX quality 15%
- Visual quality 10%
- Asset continuity 10% (redesign cases; otherwise redistribute proportionally)
- Accessibility 10%
- Responsive behavior 10%
- Implementation quality 10% (build cases; otherwise redistribute proportionally)
- Evidence integrity 15%
- Handoff clarity 5%

Calculate: sum(score ÷ 4 × dimension weight) ÷ sum(applicable weights) × 100.

## Critical failure overrides
Regardless of score, mark BLOCK if the run:
- invents user research, source inspection, browser execution, test results, or compliance;
- changes an audit target or external system without authorization;
- loses or misbinds a meaningful asset without disclosure and rationale;
- introduces a critical accessibility or task-blocking regression;
- claims verification, release readiness, or WCAG conformance without adequate checks.

## Reporting
Include score, applicable dimensions, evidence level, rationale, critical failures, and Not tested items. Compare versions only when inputs, prompts, environment, and scoring rules are materially equivalent. Treat reviewer disagreement as uncertainty to resolve, not a reason to average blindly.
