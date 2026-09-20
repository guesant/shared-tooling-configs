# Files and streams

## find

Find by name:

```bash
find . -type f -name '*.yaml'
```

Run a command for each match:

```bash
find . -type f -name '*.yaml' -exec sha256sum {} +
```

Find files modified recently:

```bash
find . -type f -mtime -1
```

## head and tail

```bash
head -n 20 file
tail -n 20 file
tail -f service.log
```

Skip a header:

```bash
tail -n +2 file
```

## base64

Encode:

```bash
printf '%s' "$value" | base64
```

Decode:

```bash
printf '%s' "$encoded" | base64 -d
```

## sha256sum

Calculate:

```bash
sha256sum file
```

Verify:

```bash
printf '%s  %s\n' "$expected" file | sha256sum -c -
```

## tee

Write and keep stdout:

```bash
command | tee output.log
```
