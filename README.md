# The SoDa Guide to LLM Computing Infrastructure in the Netherlands

This repository contains a MkDocs (GitBook theme) documentation project for:

- An overview of how to use LLMs in research
- Institutional resources in the Netherlands

## Prerequisites

- Python 3.12+
- [uv](https://docs.astral.sh/uv/)

## Setup (uv)

Install dependencies and create/sync the virtual environment:

```bash
uv sync
```

## Run Docs Locally (uv)

Start the MkDocs development server:

```bash
uv run mkdocs serve
```

Then open the local URL shown in your terminal (usually `http://127.0.0.1:8000`).

## Build Docs

Build the static site locally:

```bash
uv run mkdocs build
```

The generated site is written to the `site/` directory.

## Deployment

Deployment is automated via GitHub Actions.

- On every push to `main`, the workflow **Deploy MkDocs to GitHub Pages** runs `mkdocs gh-deploy --force`.
- This publishes the documentation to the `gh-pages` branch.

You can also trigger deployment manually from the Actions tab.

## Link Checking (Weekly)

External URL monitoring is handled by a separate workflow: **Weekly External Link Check**.

- Schedule: weekly on Sunday at 04:00 UTC
- Trigger: scheduled run or manual dispatch
- Scope: checks external links in docs and MkDocs configuration
- Reporting: creates or updates a single issue titled **Weekly link check: broken external URLs** with label `broken-links`
- Recovery behavior: if links are clean again, the workflow comments and closes that issue

This link-check workflow is intentionally independent from deployment, so publishing is not blocked by transient external link failures.