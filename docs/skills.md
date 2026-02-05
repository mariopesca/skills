# Available skills

> Warning: Most of the content in this repository is AI-generated and may contain mistakes. Review carefully before use.

## Featured skills

### readthedocs-api

Full Read the Docs API v3 client reference with short and full endpoint guides.

**Location**: `skills/readthedocs-api/`

**Use when**:

- Building or updating an API client.
- Looking up API v3 endpoints and parameters.
- Creating requests for projects, versions, builds, or related resources.

### Quick start

```bash
curl -H "Authorization: Token $RTD_TOKEN" \
  "${RTD_HOST}/api/v3/projects/"
```

See `skills/readthedocs-api/SKILL.md` for detailed instructions.

### readthedocs-write-config

Create or update Read the Docs `.readthedocs.yaml` v2 configuration files for Sphinx or MkDocs builds.

**Location**: `skills/readthedocs-write-config/`

**Use when**:

- Adding a new `.readthedocs.yaml` file.
- Updating build images or tool versions.
- Adjusting dependency installs.
- Customizing build jobs or commands.
- Configuring conda environments, submodules, or search settings.

### Minimal Sphinx config

```yaml
version: 2

build:
  os: ubuntu-24.04
  tools:
    python: "3.12"

python:
  install:
    - requirements: docs/requirements.txt

sphinx:
  configuration: docs/conf.py
```

See `skills/readthedocs-write-config/SKILL.md` for detailed instructions.

<details>
<summary>Other skills</summary>

The following skills are available but not highlighted in this overview. See each
skill's `SKILL.md` for full details.

- **readthedocs-search-api**: Query the Read the Docs Search API to find
  documentation across projects and repositories.
  (`skills/readthedocs-search-api/`).
- **readthedocs-project-manager**: Manage projects via the RTD API (create
  projects, trigger builds, sync versions, check build status).
  (`skills/readthedocs-project-manager/`).
- **readthedocs-redirects-manager**: List, create, update, and delete custom
  redirect rules for a project.
  (`skills/readthedocs-redirects-manager/`).
- **readthedocs-build-failure-triage**: Analyze build failures using build logs
  and config context.
  (`skills/readthedocs-build-failure-triage/`).

</details>
