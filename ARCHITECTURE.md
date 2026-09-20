# Architecture

The repository is modeled as a multidimensional tooling catalog rather than a directory tree that tries to encode every classification.

## Source of truth

Each concrete tool has one canonical location under `tools/`.

A configuration must not be duplicated merely to expose it through another dimension such as code quality, security, language, project type, architecture, or lifecycle stage.

Those relationships belong to catalog metadata.

## Concepts

### Tool

A concrete tool or platform used during software development, delivery, maintenance, or operations.

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

The catalog should answer questions such as which tools provide duplication detection, which tools apply to TypeScript, which options can run in CI, and which recipes suit a given project.

Symlinks are not used as the primary navigation mechanism. They encode filesystem relationships but cannot explain why a tool belongs to a category, how strongly it covers a capability, or how it overlaps with other tooling.
