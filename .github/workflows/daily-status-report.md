---
on:
  schedule:
    - cron: '0 12 * * *'  # Daily at 12:00 UTC
  workflow_dispatch:  # Allow manual trigger

permissions:
  contents: read
  issues: read
  pull-requests: read

safe-outputs:
  create-issue:
    title-prefix: "[research-note status]"
    labels: [report]

tools:
  github:
---

# Research Note Daily Status Report

Create a daily status report for the research-note repository maintainers.

## What to Include

**Repository Activity:**
- Recent issues (opened, closed, labeled in last 24h)
- Recent pull requests (opened, merged in last 24h)
- Recent releases (if any)
- Code changes: significant commits, file additions

**Health Metrics:**
- Open issues breakdown by label
- Open PRs with age analysis
- Test coverage (if available)
- Last release date

**Progress Tracking:**
- Any TODO/FIXME comments in code (flag for review)
- Documentation gaps (README vs code)
- Potential improvements or refactoring opportunities

**Actionable Items:**
- Issues needing attention (stale, unassigned)
- PRs ready for review
- Bugs or feature requests to prioritize

## Formatting

- Keep it concise (bullet points preferred)
- Link directly to relevant issues/PRs
- Highlight blockers in red (use Markdown)
- Highlight completed items in green
- Use emojis for quick scanning: 🐛 bugs, ✨ features, 📝 docs, 🔧 maintenance

## Audience

This report is for maintainers: Seneca, Marcus, Galen, and anyone contributing to research-note.

## Goal

Help maintainers stay informed about repository health, prioritize work, and identify actionable next steps without having to manually check GitHub.
