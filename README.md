# indie-dev-agent-skills

A curated collection of reusable AI agent skills for indie developers — turning experience into repeatable, high-quality workflows.

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

## Skill Spec

Each skill follows a consistent structure to ensure reliability and reuse.

### Typical Skill Structure

#### Metadata
- Name
- Description
- Intended usage scenarios
- Required inputs
- Expected outputs

#### Background Knowledge
- Domain-specific context
- Assumptions and constraints
- Non-obvious considerations

#### Instructions
- Step-by-step execution logic
- Decision points and branching rules
- Quality checks and validation criteria

#### References (Optional)
- Docs
- Examples
- Templates
- Scripts

### Design Principles

* Prefer **explicit instructions** over vague prompts
* Optimize for **consistent output quality**
* Encode **experience, not just information**
* Assume the skill will be reused by future agents with no prior context

## Contributing

Contributions are welcome.

This repository values:

* Real-world experience over theoretical completeness
* Clear structure over clever wording
* Practical workflows over generic advice

### How to Contribute

1. Fork the repository
2. Add a new skill following the existing spec
3. Keep skills focused and scoped
4. Submit a pull request with a clear description

### What Makes a Good Skill

* Solves a recurring real problem
* Can be reused across projects
* Encodes decisions, not just steps
* Improves agent reliability and output quality

## License

MIT License