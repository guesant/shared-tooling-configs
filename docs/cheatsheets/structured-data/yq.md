# yq

Examples assume mikefarah/yq syntax.

## Read a field

```bash
yq '.metadata.name' file.yaml
```

## Read raw scalar output

```bash
yq -r '.image.tag' values.yaml
```

## Select entries

```bash
yq '.items[] | select(.enabled == true)' file.yaml
```

## Update a value

```bash
yq -i '.image.tag = "v1.2.3"' values.yaml
```

## Use an environment variable

```bash
TAG=v1.2.3 yq -i '.image.tag = strenv(TAG)' values.yaml
```

## Convert YAML to JSON

```bash
yq -o=json '.' file.yaml
```
