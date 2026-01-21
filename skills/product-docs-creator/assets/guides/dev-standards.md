---
doc_type: guide
doc_category: development
doc_id: dev-standards
title: Development Standards
version: 0.1
status: draft
---

# Development Standards

## Purpose
This document defines development conventions to ensure consistency,
maintainability, and collaboration quality across the codebase.
It does NOT define system behavior.

## Scope
### Applies To
- Source code
- Git workflow
- Code reviews

### Out of Scope
- System architecture decisions
- Product requirements

## Coding Principles
- Prefer readability over cleverness
- Small, composable functions/modules
- Explicit naming over implicit behavior
- Avoid premature optimization

## Git Commit Conventions
- Commit messages MUST be descriptive
- One logical change per commit

### Commit Message Format

```
<type>: <short summary>
```

(optional body)

**Recommended types**
- feat
- fix
- refactor
- chore
- docs
- test

## Branching Strategy
- `main` / `master`: stable, releasable
- `develop` (if used): integration branch
- `feature/*`: new work
- `fix/*`: bug fixes

## Code Review Guidelines
- Every PR must:
  - Build successfully
  - Pass existing tests
  - Contain a clear description of changes
- Review for:
  - correctness
  - clarity
  - unintended side effects

## Formatting & Linting
- Use automated formatters when available
- Lint errors must be resolved before merge

## Open Questions
- [Q-1] Are there language-specific style guides to enforce?

