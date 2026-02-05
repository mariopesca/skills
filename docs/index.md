# Read the Docs Skills

This project provides Agent Skills for interacting with Read the Docs APIs and services.
Each skill is a small, self-contained package that teaches a model how to perform a
specialized workflow.

> Warning: Most of the content in this repository is AI-generated and may contain mistakes. Review carefully before use.

## What is a skill?

A skill is a folder that includes:

- `SKILL.md` with instructions and examples.
- Optional scripts, references, or assets for the workflow.

Skills are discovered automatically by compatible agents. When a user request matches
a skill description, the agent loads the relevant `SKILL.md` and follows its steps.

## Featured skills

### Read the Docs API

Full Read the Docs API v3 client guidance. Use this skill when you are building or
updating an API client, generating requests, or answering questions about API v3
endpoints.

- **Location**: `skills/readthedocs-api/`.
- **Use when**: You need endpoint paths, parameters, request bodies, or response fields.
- **Hosts**:
  - Read the Docs Community: `https://app.readthedocs.org`.
  - Read the Docs Business: `https://app.readthedocs.com`.

See `skills/readthedocs-api/SKILL.md` for detailed instructions.

### Read the Docs Config Writer

Create or update Read the Docs `.readthedocs.yaml` v2 configuration files for Sphinx
or MkDocs builds.

- **Location**: `skills/readthedocs-write-config/`.
- **Use when**: You need a new `.readthedocs.yaml` file or changes to build images,
  tools, dependency installs, formats, build jobs, conda, submodules, or search
  settings.

See `skills/readthedocs-write-config/SKILL.md` for detailed instructions.

<details>
<summary>Other skills</summary>

- **Read the Docs Search API**: Query the Read the Docs Search API to find
  documentation across projects and repositories.
  (`skills/readthedocs-search-api/`).
- **Read the Docs Project Manager**: Manage projects via the RTD API (create
  projects, trigger builds, sync versions, check build status).
  (`skills/readthedocs-project-manager/`).
- **Read the Docs Redirects Manager**: List, create, update, and delete custom
  redirect rules for a project.
  (`skills/readthedocs-redirects-manager/`).
- **Read the Docs Build Failure Triage**: Analyze build failures using build logs
  and config context.
  (`skills/readthedocs-build-failure-triage/`).

</details>

## Repository layout

```
.
├── README.md
└── skills/
    ├── readthedocs-api/
    │   └── SKILL.md
    ├── readthedocs-write-config/
    │   └── SKILL.md
    └── ...
```

## Next steps

Start by reviewing the available skills and their usage examples.
If you want to add another skill, follow the contribution guide.
