# Bash

## Strict mode

```bash
set -euo pipefail
```

## Parameters

```bash
value="${1:-default}"
: "${REQUIRED_VAR:?REQUIRED_VAR is required}"
```

## Arrays

```bash
items=(one two three)
for item in "${items[@]}"; do
  printf '%s\n' "$item"
done
```

## Read lines safely

```bash
while IFS= read -r line; do
  printf '%s\n' "$line"
done < file.txt
```

## Command existence

```bash
command -v jq >/dev/null 2>&1
```

## Temporary files

```bash
tmp="$(mktemp)"
trap 'rm -f "$tmp"' EXIT
```

## Script directory

```bash
script_dir="$(cd "$(dirname "${BASH_SOURCE[0]}")" && pwd)"
```
