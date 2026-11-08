# Workflow: validation lab

## Purpose
Prove that the skill produces useful, accurate, reproducible work before adding more capabilities. Use a small, repeatable test set and record evidence rather than relying on subjective impressions.

## Test protocol
1. **Freeze the input:** record the exact prompt, source URL/files, user-provided constraints, target platform, available tools, and starting commit/version.
2. **Choose the mode:** audit, redesign, or design-from-scratch. Do not mix evaluation criteria between modes.
3. **Capture baseline:** record viewport dimensions, browser/environment when available, screenshots, existing component/asset relationships, and known limitations. If source inspection is unavailable, label observations screenshot-only.
4. **Run the skill:** use the same prompt and inputs for each candidate version. Do not quietly add guidance to one run.
5. **Collect outputs:** preserve findings, design decisions, generated artifacts, code changes, test logs, and screenshots. Separate observed facts from inferred claims.
6. **Score independently:** use the rubric in `references/validation_method.md`. Score each dimension 0–4 and attach evidence.
7. **Check critical failures:** fabricated evidence, unsafe modification, broken asset/component mapping, inaccessible critical interaction, or false test/compliance claims are blockers regardless of total score.
8. **Compare:** report score changes, regressions, unresolved gaps, and confidence. Do not claim improvement without comparable runs.
9. **Decide:** pass, revise, or block. Record the decision and exact next action.

## Minimum validation suite
- **Case A — Existing UI audit:** inspect a real screen/flow; produce evidence-based findings, severity, confidence, and reproducible steps. Audit remains read-only.
- **Case B — Asset-preserving redesign:** redesign a notification/alert/card containing an existing image or icon. Verify that the correct asset remains attached to the same component and data instance, unless a justified replacement is explicitly documented.
- **Case C — New flow design:** create a new task flow and representative screens from a brief. Evaluate task coverage, states, accessibility, responsiveness, and implementation clarity.

## Required result record
For every run, capture: test ID; skill version and commit; date; prompt/input references; environment and viewport; available tools; output artifacts; per-dimension scores; critical failures; evidence links; reviewer; decision; and follow-up issue.

## Decision gates
- **PASS:** no critical failure; evidence is sufficient; all mandatory dimensions score at least 3; total score is at least 80%.
- **REVISE:** no safety/integrity blocker, but one or more mandatory dimensions score below 3 or total is 60–79%.
- **BLOCK:** any critical failure, fabricated evidence, unauthorized modification, false validation claim, or total below 60%.

A score is not a substitute for reviewer judgment. Explain every score with evidence. Mark unavailable checks as Not tested; never convert missing evidence into a pass.
