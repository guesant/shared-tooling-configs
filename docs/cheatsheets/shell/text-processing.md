# Text processing

## grep

Recursive search:

```bash
grep -RIn -- 'pattern' path/
```

Fixed-string search:

```bash
grep -F -- 'literal.text' file
```

Only matching text:

```bash
grep -oE 'v[0-9]+\.[0-9]+\.[0-9]+' file
```

## sed

Replace the first match on each line:

```bash
sed 's/old/new/' file
```

Replace every match:

```bash
sed 's/old/new/g' file
```

Print a line range:

```bash
sed -n '20,40p' file
```

## awk

Select a field:

```bash
awk '{print $1}' file
```

Custom delimiter:

```bash
awk -F: '{print $1}' /etc/passwd
```

Filter and print:

```bash
awk '$3 > 1000 {print $1, $3}' file
```

## cut

```bash
cut -d: -f1 /etc/passwd
```

## tr

Delete characters:

```bash
tr -d '\n'
```

Translate characters:

```bash
tr '[:lower:]' '[:upper:]'
```

## sort and uniq

```bash
sort file | uniq
sort file | uniq -c | sort -nr
```

## wc

```bash
wc -l file
printf '%s\n' "$value" | wc -c
```
