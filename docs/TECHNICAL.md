# winitapp/.github

## What it does
Organization-level GitHub configuration providing standardized issue/PR templates and automated AI code review via Claude.

## Stack
| Layer | Technology |
|-------|------------|
| CI/CD | GitHub Actions |
| Templates | Markdown + YAML frontmatter |
| AI Review | OpenRouter API |
| Auth | GitHub Personal Access Tokens |

## Architecture
```
PR opened/synchronized
    │
    ▼
[Filter: not claude/* branch]
    │
    ▼
reusable workflow call ──► winitapp/claude-thedev/.github/workflows/claude-pr-review.yml@main
                              │
                              ▼
                         OpenRouter API (Claude)
```

## Run locally
1. Not applicable — GitHub-native configuration
2. Validate syntax: `yamllint .github/workflows/`
3. Test templates via GitHub web UI preview

## Request flow
1. Developer opens PR against any repo in org
2. `pr-review.yml` triggers on `opened` or `synchronize` events
3. Job filters out branches prefixed with `claude/`
4. Workflow calls external reusable workflow with PR metadata
5. External service uses `OPENROUTER_API_KEY` to generate review comments

## External dependencies
- **winitapp/claude-thedev** — Reusable workflow for AI review logic
- **OpenRouter API** — LLM inference for code review
- **PROJECT_PAT** — GitHub token for cross-repo workflow access
