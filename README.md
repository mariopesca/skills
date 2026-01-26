# Read the Docs Skills

A collection of Agent Skills for interacting with Read the Docs APIs and services.

> Warning: Most of the content in this repository is AI-generated and may contain mistakes. Review carefully before use.

## What are Agent Skills?

Agent Skills are modular packages that extend AI agent capabilities. Each skill is a folder containing a `SKILL.md` file with instructions, plus optional supporting files like scripts and templates.

Skills are **model-invoked** — agents autonomously decide when to use them based on your request and the skill's description.

Learn more at [agentskills.io](https://agentskills.io)

## Available Skills

### Read the Docs Search API

Query the Read the Docs Search API to find documentation across projects and repositories.

- **Location**: `skills/readthedocs-search-api/`
- **Use when**: Searching documentation, finding related docs, finding API documentation, or gathering information about projects on Read the Docs
- **RTD_HOST**:
  - Community: `https://app.readthedocs.org`
  - Business: `https://app.readthedocs.com`

#### Features

- Search across millions of pages of documentation
- No authentication required (public API)
- Paginated results
- Project and version information
- HTML highlights of matched text
- Section-level search results

See `skills/readthedocs-search-api/SKILL.md` for detailed instructions.

### Read the Docs Project Manager

Manage Read the Docs projects via the RTD API: create projects, trigger builds, sync
versions, and check build status.

- **Location**: `skills/readthedocs-project-manager/`
- **Use when**: Creating projects, listing repos, triggering builds, syncing versions, or checking build status

See `skills/readthedocs-project-manager/SKILL.md` for detailed instructions.

### Read the Docs Redirects Manager

Manage Read the Docs redirects via the RTD API: list, create, update, and delete
custom redirect rules for a project.

- **Location**: `skills/readthedocs-redirects-manager/`
- **Use when**: Listing, creating, updating, or deleting custom redirects

See `skills/readthedocs-redirects-manager/SKILL.md` for detailed instructions.

### Read the Docs Build Failure Triage

Triage Read the Docs build failures using build logs and config context.

- **Location**: `skills/readthedocs-build-failure-triage/`
- **Use when**: A build fails, logs need analysis, or you need fix recommendations

See `skills/readthedocs-build-failure-triage/SKILL.md` for detailed instructions.

### Read the Docs Config Writer

Create or update Read the Docs `.readthedocs.yaml` v2 configuration files for Sphinx or MkDocs builds.

- **Location**: `skills/rtd-write-config/`
- **Use when**: You need a new `.readthedocs.yaml` file or changes to build images, tools, dependency installs, formats, build jobs, conda, submodules, or search settings

See `skills/rtd-write-config/SKILL.md` for detailed instructions.

## Installation

Clone this repository and use the skill directories directly:

```bash
git clone https://github.com/readthedocs/skills.git
```

Or add it as a submodule and reference the skill directories you need:

```bash
git submodule add https://github.com/readthedocs/skills.git
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
    ├── readthedocs-search-api/
    │   └── SKILL.md
    └── rtd-write-config/
        └── SKILL.md
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
