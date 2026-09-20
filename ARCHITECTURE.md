# Architecture

The repository is a multidimensional tooling catalog rather than a directory tree that tries to encode every classification.

## Canonical tool namespace

Every cataloged engineering tool has exactly one canonical namespace under `tools/<id>/`.

During discovery, that namespace may contain only `.gitkeep`. A placeholder means "this tool has been cataloged", not "this repository already provides a configuration for it".

## Evidence

### Repository inventory

Repository inventory answers what a source repository actually uses, configures, deploys, or executes.

### Documentation inventory

Documentation inventory is intentionally broader. It includes named software, CLIs, operators, runtimes, engineering platforms, and engineering services that documentation discusses or compares even when they are not deployed.

The documentation audit excludes protocols, standards, data formats, abstract concepts, organizations, programming languages, and hardware.

This separation prevents a comparison such as "Cilium versus Calico" from falsely implying that both are deployed while still giving both a stable catalog namespace.

## Concepts

### Tool

Named software, a CLI, operator, runtime, engineering platform, or engineering service that can reasonably have reusable configuration or reference material.

### Utility

A small command-line tool may be cataloged exactly like a larger tool. The size of the program does not determine whether it deserves a namespace.

### Cheatsheet

Every tool discovered in documentation receives a reference page under `docs/cheatsheets/tools/`.

Cheatsheets start as minimal reference skeletons and can grow independently from configuration presets.

### Capability

A problem or responsibility a tool can address. A tool may provide one or many capabilities.

### Preset

A reusable configuration belonging to one tool.

### Profile

A cross-tool set of engineering expectations such as minimal, recommended, or strict.

### Recipe

A composition of tool presets for a concrete project context.

### Policy

A tool-independent engineering rule. Tools and presets implement policies.

### Template

A reusable artifact that is not necessarily a tool configuration.

## Navigation

The physical tree answers where the canonical namespace lives.

The catalogs answer why an item exists and where it was discovered.

The cheatsheets answer how to approach the tool quickly.

Symlinks are not used as the primary navigation mechanism because they cannot express evidence, capabilities, overlap, or whether a tool is deployed versus merely documented.
