# shared-tooling-configs

Reusable configurations and presets for code quality, CI/CD, documentation, dependency management, security, infrastructure, and development tooling.

## Purpose

This repository centralizes reusable engineering tooling without coupling discovery to a single directory hierarchy.

Tool-specific configurations live under `tools/`. The catalog describes the capabilities, languages, targets, lifecycle stages, and supporting utilities associated with those tools. Profiles and recipes compose reusable configurations for different levels of strictness and project contexts.

## Structure

- `tools/`: canonical location for tool-specific configurations and presets.
- `catalog/`: shared taxonomy used to classify and discover tooling and utilities.
- `docs/cheatsheets/`: concise command reference for tools and supporting utilities.
- `profiles/`: cross-tool levels of strictness and engineering expectations.
- `recipes/`: compositions intended for concrete project types and stacks.
- `policies/`: tool-independent engineering rules and expectations.
- `templates/`: reusable repository and project artifacts.
- `inventory/`: findings extracted from existing repositories before promotion into shared presets.
- `scripts/`: validation, generation, inventory, and maintenance automation.

## Workflow

1. inventory existing repositories;
2. identify reusable tooling, utilities, and patterns;
3. classify them using the catalog;
4. document recurring commands in cheatsheets;
5. promote reusable configurations into tool presets;
6. compose presets through profiles and recipes.

A utility may have a cheatsheet without having a reusable configuration under `tools/`. Tool configuration is intentionally left empty during the initial inventory phase.
