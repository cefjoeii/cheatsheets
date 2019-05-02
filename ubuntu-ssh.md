---
title: Ubuntu SSH
---

### SSH Key for Git Authorization

```bash
# 0. Go home
  cd ~

# 1. Generate key
  ssh-keygen -t rsa

# 2. When prompted, enter password. Leave passphrase empty (Press enter). Key name can be left the same (Press enter).

# 3. Open file with a text editor
  <text-editor> /home/<user-name>/.ssh/id_rsa.pub

# 4. Copy and paste to a repository provider (GitHub, etc.)
```
