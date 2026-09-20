# OpenSSL

## Random values

```bash
openssl rand -base64 48
openssl rand -hex 32
```

## Inspect a certificate

```bash
openssl x509 -in certificate.pem -noout -text
openssl x509 -in certificate.pem -noout -subject -issuer -dates
```

## Inspect a remote TLS endpoint

```bash
openssl s_client -connect example.test:443 -servername example.test </dev/null
```

## Certificate fingerprint

```bash
openssl x509 -in certificate.pem -noout -fingerprint -sha256
```

## Hash a file

```bash
openssl dgst -sha256 file
```

## Derive a public key

```bash
openssl pkey -in private-key.pem -pubout
```
