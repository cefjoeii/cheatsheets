---
title: Android Debug Bridge (ADB)
---

### Wireless debugging

```bash
# 0. Add adb's path to Environment Variables or something similar

# 1. If needed, plug the device and run
  adb tcpip <port>

# 2. Connect
  adb connect <device-ip>
  OR
  adb connect <device-ip>:<port>

# 3. Disconnect
  adb disconnect <device-ip>
  OR
  adb disconnect <device-ip>:<port>
```

### USB debugging

```bash
# USB mode
  adb -s <device-ip>:<port> usb
```

### Extra

```bash
# List devices
  adb devices

# Shutdown device
  adb shell reboot -p
```
