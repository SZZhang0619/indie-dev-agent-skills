# System Analysis Writing Rules

## Goal
Produce an implementation-oriented system understanding document that enables:
- Data Model / Schema
- API / Interface Spec
- UI / Component Spec
WITHOUT requiring a separate FRD/NFR.

## Required Style
- Use concise bullets; avoid long prose.
- Prefer explicit lists over vague language.
- Each workflow must be deterministic and testable.

## Mandatory Sections
You MUST include these sections (even if short):
- Purpose
- Scope (In/Out)
- Assumptions & Constraints
- Actors + External Dependencies
- Components (conceptual responsibilities)
- Core Workflows (at least 3 unless the project is extremely small)
- Open Questions
- Next Docs (Derivation Targets)

## Assumptions Handling
- Any unknown that affects implementation must be written as:
  - an Assumption [A-x], or
  - an Open Question [Q-x]
- Never silently invent product policies, pricing, user roles, or legal claims.

## Component Definition Rules
For each component include:
- Responsibility (one sentence)
- Inputs (list)
- Outputs (list)

Avoid:
- internal class/module names
- exact folder structures
Those belong in Repo & Module Guide.

## Workflow Definition Rules
For each workflow WF-x include:
- Trigger
- Preconditions
- Steps (numbered)
- Postconditions
- Failure cases

Failure cases must include:
- at least one user-facing failure
- at least one system/dependency failure (if any dependency exists)

## Terminology Rules
- Introduce a term once in Glossary, then reuse consistently.
- No synonyms for the same concept (pick one term).

## Minimal NFR Policy
Because NFR doc is removed:
- Include only NFR points that directly affect design decisions now.
Examples:
- Offline-first requirements
- Hard performance constraints
- Mandatory encryption / privacy rules

## Output Quality Checks
Before finalizing, ensure:
- Workflows reference glossary terms (consistent naming)
- Components cover all workflows (no orphan workflow)
- Boundaries and ownership are stated clearly enough to derive API + data model
