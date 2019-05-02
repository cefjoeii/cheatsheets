---
title: Ubuntu Service
---

### List

```bash
# Get the list
  service --status-all

# Find from the list and highlight
  service --status-all | grep <service-name>
```

### Start, stop, or check the status

```bash
service <service-name> start
service <service-name> stop
service <service-name> status
```

or

```bash
systemctl start <service-name>
systemctl stop <service-name>
systemctl status <service-nam>
```

### Enable or disable at boot time

```bash
systemctl enable <service-name>
systemctl disable <service-name>
```
