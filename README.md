# indie-dev-agent-skills

A curated collection of reusable AI agent skills for indie developers — turning experience into repeatable, high-quality workflows.

---

## Why

Indie developers accumulate valuable experience through building, shipping, and maintaining real products —  
but most of that knowledge is lost after each project.

Common problems:
- Hard-won debugging and maintenance experience is not reusable
- Architecture decisions live only in memory or scattered notes
- AI agents produce inconsistent results without structured guidance
- Prompts work once, but fail to scale or transfer

**This repository exists to solve that problem.**

`indie-dev-agent-skills` turns real-world indie development experience into **explicit, structured, reusable skills** that AI agents can reliably execute.

---

## What

This repository is a growing library of **AI agent skills**, each designed to encode:

- Background knowledge and context
- Proven workflows and decision-making logic
- Constraints, edge cases, and quality standards
- Repeatable execution instructions for agents

Each skill is:
- **Modular** — focused on a specific problem or workflow
- **Reusable** — applicable across projects and teams
- **Agent-oriented** — written for execution, not explanation
- **Production-aware** — grounded in real development scenarios

Skills can cover areas such as:
- Project analysis and architecture understanding
- Mobile / web app workflows
- Maintenance, debugging, and refactoring
- DevOps, release, and operational routines
- Product, UX, and indie-specific decision flows

---

## Skill Spec

Each skill follows a consistent structure to ensure reliability and reuse.

### Typical Skill Structure

```md
# Skill Name

## Metadata
- Name
- Description
- Intended usage scenarios
- Required inputs
- Expected outputs

## Background Knowledge
- Domain-specific context
- Assumptions and constraints
- Non-obvious considerations

## Instructions
- Step-by-step execution logic
- Decision points and branching rules
- Quality checks and validation criteria

## References (Optional)
- Docs
- Examples
- Templates
- Scripts
