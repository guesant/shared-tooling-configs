# systemd

## Units

```bash
systemctl status service
systemctl start service
systemctl restart service
systemctl enable --now service
```

## Validate enabled state

```bash
systemctl is-enabled service
systemctl is-active service
```

## Reload unit definitions

```bash
systemctl daemon-reload
```

## Logs

```bash
journalctl -u service
journalctl -u service --since today
journalctl -u service -f
```

## Timers

```bash
systemctl list-timers --all
systemctl status example.timer
```

## Failed units

```bash
systemctl --failed
```
