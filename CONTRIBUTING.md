# Contributing Guide

Thanks for considering contributing to **Bias Detection Project**!  
We welcome contributions of all sizes — from fixing typos to adding new detection logic.  
This guide explains how you can help and how we work together as a community.

---

## Ways to Contribute
There are many ways to contribute:
- 🐞 **Report bugs**: Open an issue describing what’s broken and how to reproduce it.
- 💡 **Suggest features**: Open a feature request issue to discuss new ideas.
- 📝 **Improve documentation**: Fix typos, add examples, or clarify instructions.
- ⚙️ **Code contributions**: Implement new detection logic, add parsing rules, or improve performance.
- ✅ **Testing**: Write test cases to catch false positives/negatives.

---

## Development Workflow

1. **Fork the repository**  
   Click the “Fork” button on GitHub to create your own copy.

2. **Clone your fork**  
   ```bash
   git clone https://github.com/bravetto/bias-detect
   cd bias-detection

---

## Commit Message Guidelines

Write clear, helpful commit messages so others can understand the change history.

Rules:
- Use the imperative mood in the subject line (e.g., "Add rule for...", not "Added").
- Keep the subject line ≤ 72 characters; capitalize only the first word and proper nouns.
- Add a blank line after the subject, then include a body when helpful: what and why, not how.
- Reference related issues at the end (e.g., "Refs #123" or "Fixes #123").

Recommended (Conventional Commits) prefixes:
- feat: new user-facing feature
- fix: bug fix
- docs: documentation changes only
- refactor: code change that neither fixes a bug nor adds a feature
- perf: performance improvements
- test: adding or updating tests
- chore: build or tooling changes

Examples:
```
feat: add basic bias lexicon matching to detector

Introduce a minimal lexicon-based pass for initial bias flags.
This enables early feedback while we design the ML stage.
Refs #42
```

```
fix: handle null/empty input in detectBias

Return an empty result instead of throwing when text is missing.
Fixes #57
```

---

## Issues (Bugs)

When reporting a bug, please include:
- Summary: a clear one-line description
- Expected vs actual behavior
- Steps to reproduce (numbered, minimal)
- Environment: OS, Node/PNPM versions, browser (if relevant)
- Screenshots or logs if helpful
- Minimal reproduction repository or snippet when possible

Labels we commonly use: `bug`, `help wanted`, `good first issue`, `needs triage`.

---

## Feature Requests and Ideas

Before opening a large proposal, consider starting a discussion to build consensus.

When submitting an idea, include:
- Problem statement: what pain or gap are we addressing?
- Proposed solution: concise outline of what you want to build
- Alternatives considered: brief list and trade-offs
- Scope and impact: what’s in/out, risks, open questions
- Acceptance criteria: bullet list of verifiable outcomes

Small, incremental proposals are preferred over monolithic changes.

---

## Pull Requests

Checklist:
- Keep PRs focused and as small as practical
- Update or add tests where applicable
- Update documentation (README, docs) when behavior changes
- Ensure CI/lint/tests pass locally before requesting review
- Link related issues (e.g., "Fixes #123")

Review tips:
- Provide a brief PR description: context, approach, and trade-offs
- Call out areas where you’d like specific feedback

Thank you for contributing and helping us keep a clear, useful history for commits, ideas, and issues!