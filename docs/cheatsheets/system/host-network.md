# Host network utilities

## rfkill

```bash
rfkill list
rfkill block wifi
rfkill unblock wifi
```

## ipset

List sets:

```bash
ipset list
```

Inspect one set:

```bash
ipset list set-name
```

Mutating an ipset can immediately affect firewall behavior. Inspect the owning firewall or fail2ban configuration before changing it.

## rpcbind

Check whether the service is active:

```bash
systemctl status rpcbind.service rpcbind.socket
```

List registered RPC programs when the tooling is available:

```bash
rpcinfo -p
```
