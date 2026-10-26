# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project status

This repository is a fresh scaffold: it currently contains only `README.md`, `.gitignore` (the standard GitHub Python template), and `.env.example`. There is no source code, build system, dependency manifest, or test suite yet, so there are no build/lint/test commands to document. Update this file once those exist.

## Known conventions

- Intended language is Python (inferred from the `.gitignore` template).
- The project will call the Anthropic API: configuration is read from a `.env` file with `ANTHROPIC_API_KEY` (see `.env.example`). `.env` is gitignored; keep `.env.example` in sync when adding new variables.
