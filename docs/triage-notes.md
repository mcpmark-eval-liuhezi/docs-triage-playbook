# Documentation Triage Notes

Research notes for this playbook, seeded from real activity in `microsoft/vscode`.

## Research method

1. Searched `microsoft/vscode` for open issues with the `documentation` label.
   - The search for `repo:microsoft/vscode is:open label:documentation` (and several variants: `is:issue label:documentation`, quoted label, and the REST issues API with `labels=documentation`) all returned **0 results** (`total_count: 0`). The `documentation` label exists in other contexts but currently matches **no** open issues in `microsoft/vscode`.
   - As a documented fallback, the selection below instead uses open VS Code issues that mention documentation, ranked by comment count: `repo:microsoft/vscode is:open documentation in:title sort:comments-desc`.
2. Selected the top three by comment count.
3. Checked `microsoft/vscode` tags to timestamp the research (newest tag found is noted below).

## Selected VS Code source issues

The three open VS Code issues with "documentation" in the title, most-commented first:

| # | Title | Comments | Link |
|---|-------|----------|------|
| 149270 | Allow parameter hints and completion documentation to appear in a docked panel instead of floating over the code | 15 | https://github.com/microsoft/vscode/issues/149270 |
| 283163 | @Docs like Cursor to index documentation sites | 10 | https://github.com/microsoft/vscode/issues/283163 |
| 25898 | [html] provide translations of tag documentation | 10 | https://github.com/microsoft/vscode/issues/25898 |

Note on the tie: issues #283163 and #25898 both report 10 comments, tied for fewest among the three. The mirror of #25898 (last-ranked in the ranked search results) was treated as the least-commented item for the follow-up reorg described below.

## Mirror issues in this repo

Issues created in `mcpmark-eval-liuhezi/docs-triage-playbook`:

| Repo issue # | Mirrors source | Title |
|--------------|----------------|-------|
| #2 | vscode #149270 | [vscode #149270] Allow parameter hints and completion documentation to appear in a docked panel instead of floating over the code |
| #3 | vscode #283163 | [vscode #283163] @Docs like Cursor to index documentation sites |
| #4 | vscode #25898 | [vscode #25898] [html] provide translations of tag documentation |

## Final parent / sub-issue structure

- **Issue #1 — "Documentation triage backlog"** (umbrella). Sub-issues:
  - #2 (mirrors vscode #149270)
  - #3 (mirrors vscode #283163)
- **Issue #5 — "Docs triage follow-ups"** (second parent). Sub-issues:
  - #4 (mirrors vscode #25898, the least-commented source issue — moved out of the umbrella during the reorg, so it sits under #5 only, not under both parents)

## Newest VS Code tag

The newest tag found in `microsoft/vscode` (pages of the tag list are returned in descending order) is **`1.103.1`**, which points at commit `e3550cfac4b63ca4eafca7b601f0d2885817fd1f`. The versioned release tags run in descending order (`1.103.1`, `1.103.0`, `1.102.3`, ...), and the first page of the tag list instead lists some older prefixed tags (`vsda-v1.39.1`, `v14`, `v1.19.3`, `v0.45.1`, `translation/2017*`), so `1.103.1` is the newest release tag overall.

This research was stamped with that tag as the reference point.
