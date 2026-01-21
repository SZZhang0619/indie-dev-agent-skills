---
name: product-docs-creator
description: An AI agent skill to create lean, implementation-driven product documentation.
---

## Core Principles

- Implementation-first, not presentation-first
- Ask before assuming
- Generate the minimum documentation required to proceed safely
- Make assumptions and uncertainties explicit
- Optimize outputs for:
  - engineers
  - small teams
  - AI agents

---

## Interaction Model

1. Understand project context via Q&A
2. Identify which documents are required (do NOT generate all by default)
3. Confirm scope and assumptions
4. Generate documents incrementally
5. Reuse previously confirmed information as source-of-truth
6. Maintain cross-document consistency

The agent MUST NOT generate full documents without prior confirmation.

---

## Document Classification

### A. Specification Documents

These documents define **system behavior, structure, and constraints**.
They are considered **source-of-truth** and must be internally consistent.

#### 1. System Analysis
- Defines system boundaries, actors, workflows, assumptions, and constraints
- Serves as the root document for derivation

#### 2. Data Model / Schema
- Defines domain entities, fields, relationships, and ownership
- Must be derivable from System Analysis

#### 3. API / Interface Specification
- Defines contracts between system components or external actors
- Includes inputs, outputs, and error behaviors

#### 4. UI / Component Specification
- Defines component responsibilities, states, and interactions
- Focuses on behavior, not visual design

#### 5. Test Plan
- Defines what constitutes correct behavior
- Includes critical paths and failure scenarios

#### 6. Error Handling / Exception Strategy
- Defines error categories, handling responsibilities, and user/system responses

---

### B. Guide Documents

These documents describe **how to implement, organize, deploy, or operate** the system.
They are contextual and may vary by team or project.

#### 7. Repository & Module Guide
- Describes repository structure and module responsibilities
- Maps system components to code organization

#### 8. Development Standards
- Defines commit conventions, branching strategies, and code hygiene rules
- Enforces team-level consistency, not system behavior

#### 9. Environment / CI-CD / Release Guide
- Describes environment setup, build pipelines, and deployment flow
- Operational in nature

#### 10. Release & Store Documentation
- Describes app release processes (e.g., App Store / Play Store)
- Includes compliance and submission notes

---

### C. Meta / Agent Documents

These documents configure **AI behavior and capabilities**.
They are not system specifications.

#### 11. Agent System Prompt
- Defines agent role, behavior constraints, and interaction rules

#### 12. Skill / Tool Definition (Skill.md, Tool specs)
- Defines available skills, tools, and usage contexts
- Enables composable agent workflows

---

## File System Conventions

- Templates MUST be loaded from:
  - `/assets/templates/`
- Writing rules MUST be enforced from:
  - `/references/writing-rules/`
- Global writing constraints MUST be enforced from:
  - `/references/global-rules.md`

The agent MUST follow document-specific rules when generating each file.

Specification templates are organized by enforcement level:

- /specifications/mandatory/
  Documents that MUST exist before implementation proceeds.

- /specifications/optional/
  Documents that are generated conditionally based on system complexity and risk.

The agent MUST enforce these rules based on template location.

---

## Assumptions & Uncertainty Handling

- Any unknown that affects implementation MUST be recorded as:
  - an **Assumption [A-x]**, or
  - an **Open Question [Q-x]**
- The agent MUST NOT silently invent:
  - business policies
  - pricing models
  - legal claims
  - user roles

---

## Output Quality Requirements

Before finalizing any document, the agent MUST ensure:

- Terminology is consistent across documents
- All Specifications can be derived from System Analysis
- No workflow, component, or entity is orphaned
- Guides do not contradict Specifications

---

## Non-Goals

This skill explicitly does NOT aim to:

- Replace PMP, SA, or SD certification documentation
- Generate exhaustive enterprise documentation
- Optimize for presentation or stakeholder persuasion

---

## Intended Use Cases

- Solo developers and small teams
- AI-assisted development workflows
- Project bootstrapping
- Taking over poorly documented projects
- Generating just-enough documentation to proceed safely
