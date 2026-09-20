# curl

## Fail on HTTP errors

```bash
curl -fsS https://example.test/health
```

Follow redirects:

```bash
curl -fsSL https://example.test/file
```

## Download to a file

```bash
curl -fsSLo artifact.tar.gz https://example.test/artifact.tar.gz
```

## Headers

```bash
curl -fsS -H "Authorization: Bearer $TOKEN" https://example.test/api
```

## JSON request

```bash
curl -fsS -X POST https://example.test/api \
  -H 'Content-Type: application/json' \
  --data '{"enabled":true}'
```

## Retry transient failures

```bash
curl --fail --silent --show-error --retry 5 --retry-all-errors https://example.test/api
```

## Inspect response headers

```bash
curl -I https://example.test
```
