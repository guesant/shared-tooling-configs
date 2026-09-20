# Architecture

The repository is modeled as a multidimensional tooling catalog rather than a directory tree that tries to encode every classification.

## Source of truth

Each concrete tool has one canonical location under `tools/`.

A configuration must not be duplicated merely to expose it through another dimension such as code quality, security, language, project type, architecture, or lifecycle stage.

Those relationships belong to catalog metadata.

## Concepts

### Tool

A concrete tool or platform used during software development, delivery, maintenance, or operations.

A tool belongs under `tools/` when reusable configuration, presets, policies, or integration artifacts are expected for it.

### Utility

A command or small supporting program that is useful during engineering work but does not necessarily justify reusable configuration.

Utilities are cataloged in `catalog/utilities.yaml`. A utility may later be promoted to a tool without changing its cheatsheet.

### Cheatsheet

A concise reference for recurring commands and operational patterns.

Cheatsheets live under `docs/cheatsheets/`. They are reference documentation, not tutorials, and may cover both full tools and small utilities.

### Capability

A problem or responsibility a tool can address. A tool may provide one or many capabilities.

### Preset

A reusable configuration belonging to one tool. Presets may vary by language, framework, target, or strictness.

### Profile

A cross-tool set of engineering expectations, such as minimal, recommended, or strict.

### Recipe

A composition of tool presets intended for a concrete project context.

### Policy

A tool-independent engineering rule. Tools and presets are implementations of policies.

### Template

A reusable artifact that is not necessarily a tool configuration.

### Inventory

A record of tooling observed in an existing repository. Inventory entries are evidence, not shared standards.

## Navigation

The physical tree answers where the canonical configuration lives.

The catalog should answer questions such as which tools provide duplication detection, which tools apply to TypeScript, which utilities are commonly used for structured data, and which recipes suit a given project.

The cheatsheets answer how to perform recurring operations quickly without turning every utility into a configured tool.

Symlinks are not used as the primary navigation mechanism. They encode filesystem relationships but cannot explain why a tool belongs to a category, how strongly it covers a capability, or how it overlaps with other tooling.
