# winitapp/.github

## Stack
GitHub Actions, YAML, Markdown templates.

## Structure
- `.github/PULL_REQUEST_TEMPLATE.md` — Standard PR description format
- `.github/ISSUE_TEMPLATE/` — Bug and task templates with frontmatter
- `.github/workflows/pr-review.yml` — AI-powered PR review automation

## Run & test
```bash
# No local runtime; validate YAML syntax
yamllint .github/workflows/pr-review.yml
```

## Conventions
- Skip `claude/*` branches in PR review workflow (reserved for Claude execute loop)
- Always reference closing issue with `Closes #` in PRs
- Include "What/Why/How to test" sections in PR descriptions
- Label new issues with `needs-refinement` by default
- Require `@mention` for owner assignment in issues
- Use appetite sizing (S/M/L) in task tickets
- Call reusable workflows from `winitapp/claude-thedev@main`

## Key files
- `workflows/pr-review.yml` — AI review orchestration
- `PULL_REQUEST_TEMPLATE.md` — Contribution format standard
- `ISSUE_TEMPLATE/bug.md` — Bug report structure
- `ISSUE_TEMPLATE/task.md` — Feature task structure

## Rules
- Never modify `claude/` branch filtering logic without checking claude-thedev repo
- Always preserve `OPENROUTER_API_KEY` and `PROJECT_PAT` secret references
- Never commit console.logs or debug code (enforced by PR checklist)
