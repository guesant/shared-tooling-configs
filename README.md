# shared-tooling-configs

Reusable configurations, presets, references, and engineering tooling shared across projects.

## Purpose

This repository centralizes reusable engineering tooling without coupling discovery to a single directory hierarchy.

Tool-specific namespaces live under `tools/`. A directory may initially contain only `.gitkeep`: its existence reserves a canonical location and does not imply that a reusable configuration has already been extracted.

## Structure

- `tools/`: canonical namespace for every cataloged tool.
- `catalog/`: taxonomies and generated catalogs, including tools discovered in documentation.
- `docs/cheatsheets/`: concise reference for cataloged tools and supporting utilities.
- `profiles/`: cross-tool levels of strictness and engineering expectations.
- `recipes/`: compositions for concrete project types and stacks.
- `policies/`: tool-independent engineering rules and expectations.
- `templates/`: reusable repository and project artifacts.
- `inventory/`: evidence collected from existing repositories and documentation.
- `scripts/`: validation, generation, inventory, and maintenance automation.

## Discovery model

The repository distinguishes two kinds of evidence:

1. runtime/repository inventory records tools that a source repository actually uses or configures;
2. documentation inventory records tools that its documentation discusses, compares, teaches, or references.

A documentation mention reserves both `tools/<id>/` and `docs/cheatsheets/tools/<id>.md`, even when no preset exists yet.

## Workflow

1. inventory repositories and documentation;
2. normalize names and aliases;
3. reserve a canonical tool namespace;
4. add a cheatsheet reference;
5. classify capabilities and targets;
6. promote proven reusable configuration into presets;
7. compose presets through profiles and recipes.
