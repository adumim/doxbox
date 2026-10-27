# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

DoxBox (doxbox.com) is an AI assistant for business meetings and interviews. The pipeline has two stages:

1. **Recording → transcript**: a transcriber turns the meeting recording into a text transcript.
2. **Transcript → document**: Claude (via the Anthropic API) turns the transcript into a structured document based on a template.

The repository is still an early scaffold: no source code, dependency manifest, or tests exist yet. Update this file (architecture, entry point, commands) as they appear.

## Stack

- Python
- `anthropic` SDK for the Claude API
- `pytest` for tests

## Commands

Setup (Windows, Git Bash):

```bash
python -m venv .venv
source .venv/Scripts/activate
pip install anthropic pytest
cp .env.example .env   # then set ANTHROPIC_API_KEY
```

Tests:

```bash
pytest                                      # all tests
pytest tests/test_module.py                 # one file
pytest tests/test_module.py::test_name      # one test
```

Run: no entry point exists yet — add the run command here when it is created.

## Rules

- **English only**: code, identifiers, comments, docstrings, commit messages, PR descriptions, and docs.
- **Branches and PRs only**: never commit directly to `main`. Create a branch for every change and merge it through a pull request.
- **A test for every function**: each new or changed function gets pytest coverage in the same PR.
- **No secrets in code**: configuration such as `ANTHROPIC_API_KEY` is read from `.env` (gitignored). Keep `.env.example` in sync when adding variables.
- **Ask before adding dependencies**: get the user's approval before adding any new package.
