# CAIRA Skill PoC

This repository contains a proof-of-concept CAIRA skill definition for coding agents building on the Azure AI platform (including Azure AI Foundry).

The skill is designed to:
- Discover CAIRA reference architectures, modules, and docs dynamically from the upstream repository.
- Recommend architecture options based on user requirements.
- Guide scaffold and code-generation flows across infrastructure, platform, and application layers.

## Prerequisites

If you don't have `bun` or `npx` installed yet, install Bun first (from https://bun.com/docs/installation):

```bash
curl -fsSL https://bun.com/install | bash
```

Then restart your terminal and verify:

```bash
bun --version
```

For Windows install instructions, see: https://bun.com/docs/installation

## Installation

Install the skill from your project's directory so your coding agent can pick it up for that project.

```bash
cd /path/to/your-project
```

Using Bun:

```bash
bunx skills add github.com/PabloZaiden/caira-skill-poc
```

Using NPX:

```bash
npx skills add github.com/PabloZaiden/caira-skill-poc
```

## Repository structure

```text
.
└── caira/
    ├── SKILL.md
    └── references/
        ├── caira-file-mapping.md
        ├── reference-architecture-selection.md
        └── scaffold-modes.md
```

## Key files

- `caira/SKILL.md`: Main skill definition, behavior rules, discovery workflow, and output template.
- `caira/references/caira-file-mapping.md`: Dynamic repository discovery and evidence expectations.
- `caira/references/reference-architecture-selection.md`: Architecture-selection rubric and confirmation gate.
- `caira/references/scaffold-modes.md`: Scaffold mode guidance (`reference` vs `copy`) and safety constraints.

## Notes

- The skill expects network access to GitHub APIs/content endpoints referenced in `caira/SKILL.md`.
- It treats the upstream [microsoft/CAIRA](https://github.com/microsoft/CAIRA) repository as the source of truth.
