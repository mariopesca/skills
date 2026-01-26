# Available skills

> Warning: Most of the content in this repository is AI-generated and may contain mistakes. Review carefully before use.

## readthedocs-search-api

Query the Read the Docs Search API to find documentation across projects and repositories.

**Location**: `skills/readthedocs-search-api/`

**Use when**:

- Searching documentation
- Finding related docs
- Looking up API references
- Gathering information about Read the Docs projects

**RTD_HOST**:

- Community: `https://app.readthedocs.org`
- Business: `https://app.readthedocs.com`

### Quick start

```bash
curl "${RTD_HOST}/api/v3/search/?q=authentication"
```

### Features

- Search across millions of pages of documentation
- No authentication required (public API)
- Paginated results
- Project and version information
- HTML highlights of matched text
- Section-level search results

### Scoped search example

Use fielded search syntax to scope by project:

```bash
curl "${RTD_HOST}/api/v3/search/?q=project:docs%20.readthedocs.yaml"
```

See `skills/readthedocs-search-api/SKILL.md` for detailed instructions.

## readthedocs-project-manager

Manage Read the Docs projects via the RTD API: create projects, trigger builds,
sync versions, and check build status.

**Location**: `skills/readthedocs-project-manager/`

**Use when**:

- Creating projects
- Listing repos
- Triggering builds
- Syncing versions
- Checking build status

### Create a project

```bash
curl -s -X POST "${RTD_HOST}/api/v3/projects/" \
  -H "Authorization: Token $RTD_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name":"Project Name","slug":"project-slug","repository":{"url":"https://github.com/org/repo","type":"git"}}'
```

See `skills/readthedocs-project-manager/SKILL.md` for detailed instructions.

## readthedocs-redirects-manager

Manage Read the Docs redirects via the RTD API: list, create, update, and delete
custom redirect rules for a project.

**Location**: `skills/readthedocs-redirects-manager/`

**Use when**:

- Listing redirects
- Creating redirects
- Updating redirects
- Deleting redirects

### Create a redirect

```bash
curl -s -X POST \
  -H "Authorization: Token $RTD_TOKEN" \
  -H "Content-Type: application/json" \
  "${RTD_HOST}/api/v3/projects/project-slug/redirects/" \
  -d '{
    "from_url": "/old-page/",
    "to_url": "/new-page/",
    "type": "page",
    "http_status": 301,
    "description": "Move old page to new location",
    "enabled": true
  }'
```

See `skills/readthedocs-redirects-manager/SKILL.md` for detailed instructions.

## readthedocs-build-failure-triage

Triage Read the Docs build failures using build logs and config context.

**Location**: `skills/readthedocs-build-failure-triage/`

**Use when**:

- A build fails
- Logs need analysis
- You need fix recommendations

### Fetch latest build metadata

```bash
curl -s -H "Authorization: Token $RTD_TOKEN" \
  "${RTD_HOST}/api/v3/projects/project-slug/builds/?limit=1"
```

See `skills/readthedocs-build-failure-triage/SKILL.md` for detailed instructions.

## rtd-write-config

Create or update Read the Docs `.readthedocs.yaml` v2 configuration files for Sphinx or MkDocs builds.

**Location**: `skills/rtd-write-config/`

**Use when**:

- Adding a new `.readthedocs.yaml` file
- Updating build images or tool versions
- Adjusting dependency installs
- Customizing build jobs or commands
- Configuring conda environments, submodules, or search settings

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

See `skills/rtd-write-config/SKILL.md` for detailed instructions.
