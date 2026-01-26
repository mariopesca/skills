# Read the Docs Skills

This project provides Agent Skills for interacting with Read the Docs APIs and services.
Each skill is a small, self-contained package that teaches a model how to perform a
specialized workflow.

> Warning: Most of the content in this repository is AI-generated and may contain mistakes. Review carefully before use.

## What is a skill?

A skill is a folder that includes:

- `SKILL.md` with instructions and examples
- Optional scripts, references, or assets for the workflow

Skills are discovered automatically by compatible agents. When a user request matches
a skill description, the agent loads the relevant `SKILL.md` and follows its steps.

## Repository layout

```
.
├── README.md
└── skills/
    ├── readthedocs-search-api/
    │   └── SKILL.md
    └── rtd-write-config/
        └── SKILL.md
```

## Next steps

Start by reviewing the available skills and their usage examples.
If you want to add another skill, follow the contribution guide.
