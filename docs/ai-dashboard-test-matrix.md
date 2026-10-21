# Dashboard adversarial test matrix

| Scenario | Expected behaviour | Current status |
|---|---|---|
| Empty selected countries | Clear empty message, no invalid indexing | Not run |
| Missing GDP at first year | N/A for growth and explanatory context | Not run |
| Missing GDP at last year | N/A value and no misleading delta | Not run |
| GDP zero in base year | Avoid dividing by zero | Not run |
| Single-year range | Comparison semantics are documented | Not run |
| First and last calendar years | Correct inclusive range | Not run |
| Many selected countries | Charts/legends stay usable | Not run |
| One country selected | Both line chart and metric work | Not run |
| 320px + 200% browser zoom | Labels/controls not clipped | Not run |
| Source CSV missing year column | Helpful data validation error | Not run |

No result is marked PASS until actually run. This is a review checklist, not a claim of completed browser QA.

Method adapted from Emil Kowalski's publicly available MIT-licensed break-ui workflow: https://github.com/emilkowalski/skills
