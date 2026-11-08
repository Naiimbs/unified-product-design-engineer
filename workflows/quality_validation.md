# Workflow: quality validation

1. Gather acceptance criteria, approved design/source of truth, and resolved defects.
2. Define environment, browser/device, actual viewport dimensions, locale, and test data.
3. Identify relevant functional, visual, responsive, accessibility, asset-continuity, and regression checks.
4. For each check, define reproducible steps and expected result before execution.
5. Run manual and automated checks only with available, authorized tools. Record exact commands, outcomes, and evidence.
6. Retest fixes and likely regressions across affected component instances and states.
7. Classify each criterion as **Pass**, **Fail**, **Blocked**, or **Not tested**. Never mark untested criteria passed.
8. Record evidence level and distinguish screenshot observation from source inspection or executed behavior.
9. Report residual risks, unsupported claims, limitations, and release recommendation.

A screenshot does not prove keyboard behavior, source bindings, screen-reader output, or full WCAG conformance. Automated checks do not prove complete accessibility. Use `references/validation_method.md` when a scored evaluation is requested.
