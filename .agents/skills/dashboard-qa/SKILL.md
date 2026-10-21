---
name: dashboard-qa
description: Audit Streamlit dashboard changes against real data semantics, missing values and interaction edge cases.
---

# Streamlit Dashboard QA

Use for changes to GDP charts, selectors, KPIs, data transforms, presentation and interactions.

## Audit procedure
1. Read the actual CSV header, country list, year coverage and number units.
2. Check missing and zero source values. Render unknown as N/A, never invented zero or NaN.
3. Confirm selected country and year exist before indexing a row.
4. Independently recompute at least one worked example; guard zero denominators.
5. Show a useful empty state when no country is selected.
6. Preserve raw data and report source freshness clearly.

## Worst-case fixtures
- Zero, one, and many selected countries.
- Missing GDP at start or end year, zero GDP, negative or unusually large values.
- One-year ranges, absent year column, missing source file.
- Long labels, 1,000+ rows if relevant, locale numbers and 320px viewport.
- Browser 200% zoom, keyboard use, focus order, dark mode.

## Design checks
- Clear hierarchy and number units; tabular numeric alignment; no clipped labels.
- No gratuitous animation on high-frequency inputs; respect reduced-motion.
- Prefer the project's Streamlit stack over new libraries unless justified.

## Review output
| Severity | Observed issue | Proposed fix | Evidence / test |
|---|---|---|---|

Use explicit verdicts: VERIFIED BY RUNNING; PROPOSED ONLY; BLOCKED. Do not claim a browser test has passed unless it has been performed. No production merge without review.

Inspired by the prototype and break-ui methods from https://github.com/emilkowalski/skills (MIT). Original adapted text.
