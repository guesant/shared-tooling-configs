# jq

## Read a field

```bash
jq '.name' file.json
jq -r '.name' file.json
```

## Select objects

```bash
jq '.items[] | select(.enabled == true)' file.json
```

## Map values

```bash
jq '[.items[] | .name]' file.json
```

## Build a new object

```bash
jq '{name: .metadata.name, namespace: .metadata.namespace}' file.json
```

## Pass a shell value

```bash
jq --arg name "$name" '.items[] | select(.name == $name)' file.json
```

## Use exit status

```bash
jq -e '.items | length > 0' file.json >/dev/null
```

## Read stdin

```bash
curl -fsSL https://example.test/api | jq -r '.result'
```
