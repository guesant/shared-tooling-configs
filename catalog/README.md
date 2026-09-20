# Catalog

The catalog defines dimensions and indexes used to discover tooling independently from the physical repository tree.

Current catalog files include:

- `capabilities.yaml`: engineering capabilities;
- `languages.yaml`: language targets;
- `targets.yaml`: project and execution targets;
- `lifecycle.yaml`: lifecycle stages;
- `utilities.yaml`: supporting command references;
- `documented-tools.yaml`: normalized tool ids discovered by auditing project documentation.

The physical `tools/` tree is the canonical namespace. Catalog files explain relationships and evidence.
