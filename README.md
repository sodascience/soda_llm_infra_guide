# Guide to LLM Computing Infrastructure in the Netherlands

This repository contains a MkDocs (GitBook theme) documentation project for:

- How to use LLMs in research
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

## Build Static Site (uv)

```bash
uv run mkdocs build
```

The generated site is written to the `site/` directory.

