# OpenSSH

## Connect

```bash
ssh user@host
ssh -i ~/.ssh/id_ed25519 user@host
```

## Run a remote command

```bash
ssh user@host 'systemctl status k3s'
```

## Generate an Ed25519 key

```bash
ssh-keygen -t ed25519 -a 100 -f ~/.ssh/id_ed25519
```

## Derive a public key

```bash
ssh-keygen -y -f ~/.ssh/id_ed25519
```

## Inspect a fingerprint

```bash
ssh-keygen -lf ~/.ssh/id_ed25519.pub
```

## Fetch a host key

```bash
ssh-keyscan -H host.example.test
```

Treat fetched host keys as unverified until their fingerprint is checked through a trusted channel.
