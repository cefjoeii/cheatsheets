---
title: Python 3
---

### Package Manager (pip3)

```bash
# List all installed packages
  pip3 list

# Install package
  pip3 install <package-name>

# Uninstall package
  pip3 uninstall <package-name>

# Update pip3
  pip3 install -U pip
```

### Virtual Environments

```bash
# Install
  pip install virtualenv virtualenvwrapper

# Make
  mkvirtualenv -p python3 <virtualenv-name>

# Delete
  rmvirtualenv <virtualenv-name>

# Enter
  workon <virtualenv-name>

# Exit
  deactivate
```
