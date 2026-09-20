# shared-tooling-configs

Reusable configurations and presets for code quality, CI/CD, documentation, dependency management, security, infrastructure, and development tooling.

## Purpose

This repository centralizes reusable engineering tooling without coupling discovery to a single directory hierarchy.

Tool-specific configurations live under `tools/`. The catalog describes the capabilities, languages, targets, and lifecycle stages associated with those tools. Profiles and recipes compose reusable configurations for different levels of strictness and project contexts.

## Structure

- `tools/`: canonical location for tool-specific configurations and presets.
- `catalog/`: shared taxonomy used to classify and discover tooling.
- `profiles/`: cross-tool levels of strictness and engineering expectations.
- `recipes/`: compositions intended for concrete project types and stacks.
- `policies/`: tool-independent engineering rules and expectations.
- `templates/`: reusable repository and project artifacts.
- `inventory/`: findings extracted from existing repositories before promotion into shared presets.
- `scripts/`: validation, generation, inventory, and maintenance automation.

## Workflow

1. inventory existing repositories;
2. identify reusable tooling and patterns;
3. classify them using the catalog;
4. promote reusable configurations into tool presets;
5. compose presets through profiles and recipes.

Tool configuration is intentionally left empty during the initial inventory phase.
