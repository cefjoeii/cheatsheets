---
title: Ubuntu Pomodoro
---

### Pomodoro Tomate

```bash
RELEASE=`sed -n 's/VERSION_ID="\(.*\)"/\1/p' /etc/os-release`
sudo wget -O- http://download.opensuse.org/repositories/home:/eliostvs:/tomate/xUbuntu_$RELEASE/Release.key | sudo apt-key add -
sudo bash -c "echo 'deb http://download.opensuse.org/repositories/home:/eliostvs:/tomate/xUbuntu_$RELEASE/ ./' > /etc/apt/sources.list.d/tomate.list"
sudo apt update
sudo apt install tomate-gtk
sudo apt install tomate-indicator-plugin
sudo apt install tomate-alarm-plugin
```
