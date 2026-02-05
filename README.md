# Read the Docs Skills

A collection of Agent Skills for interacting with Read the Docs APIs and services.

**Warning:** These skills can modify production Read the Docs data. Use with caution and review commands that will be run carefully.

## What are Agent Skills?

Agent Skills are modular packages that extend AI agent capabilities. Each skill is a folder containing a `SKILL.md` file with instructions, plus optional supporting files like scripts and templates.

Skills are **model-invoked** — agents autonomously decide when to use them based on your request and the skill's description.

Learn more at [agentskills.io](https://agentskills.io)

## Featured skills

### Read the Docs API

Full Read the Docs API v3 client guidance. Use this skill when you are building or
updating an API client, generating requests, or answering questions about API v3
endpoints.

- **Location**: `skills/readthedocs-api/`
- **Use when**: You need endpoint paths, parameters, request bodies, or response fields
- **Hosts**:
  - Read the Docs Community: `https://app.readthedocs.org`
  - Read the Docs Business: `https://app.readthedocs.com`

See `skills/readthedocs-api/SKILL.md` for detailed instructions.

### Read the Docs Config Writer

Create or update Read the Docs `.readthedocs.yaml` v2 configuration files for Sphinx
or MkDocs builds.

- **Location**: `skills/readthedocs-write-config/`
- **Use when**: You need a new `.readthedocs.yaml` file or changes to build images,
  tools, dependency installs, formats, build jobs, conda, submodules, or search
  settings

See `skills/readthedocs-write-config/SKILL.md` for detailed instructions.

<details>
<summary>Other skills</summary>

- **Read the Docs Search API**: Query the Read the Docs Search API to find
  documentation across projects and repositories.
  (`skills/readthedocs-search-api/`)
- **Read the Docs Project Manager**: Manage projects via the RTD API (create
  projects, trigger builds, sync versions, check build status).
  (`skills/readthedocs-project-manager/`)
- **Read the Docs Redirects Manager**: List, create, update, and delete custom
  redirect rules for a project.
  (`skills/readthedocs-redirects-manager/`)
- **Read the Docs Build Failure Triage**: Analyze build failures using build logs
  and config context.
  (`skills/readthedocs-build-failure-triage/`)

</details>

## Installation

Clone this repository and use the skill directories directly:

```bash
git clone https://github.com/readthedocs/skills.git
```

## Usage

Skills are automatically discovered by Claude and other compatible agents. Simply ask a question that matches a skill's description, and the agent will use it autonomously.

Example:
```
Can you find documentation on the Read the Docs YAML file
```

The Read the Docs Search API skill will activate and search the API for relevant documentation.

## Structure

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

## Contributing

To add a new skill:

1. Create a directory under `skills/` with a descriptive name
2. Add a `SKILL.md` file with YAML frontmatter and instructions
3. (Optional) Add supporting files like scripts or references
4. Test the skill with your agent
5. Submit a pull request

See [agentskills.io/specification](https://agentskills.io/specification) for the complete SKILL.md format specification.

## License

These skills are available under the MIT License. See LICENSE for details.

## Related Links

- [Agent Skills Home](https://agentskills.io)
- [Agent Skills Specification](https://agentskills.io/specification)
- [Read the Docs](https://readthedocs.org)
- [Read the Docs Search API Documentation](https://docs.readthedocs.com/platform/stable/server-side-search/syntax.html)
