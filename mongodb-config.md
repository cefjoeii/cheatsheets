---
title: MongoDB Configuration
---

### Change data directory (Ubuntu)

```
# Stop service
  systemctl stop mongod

# Open config file
  <text-editor> /etc/mongod.conf

# Change paths in the config file
  ...

  storage:
    dbPath: /home/<user-name>/<some-path>/mongodb/

  ...

  systemLog:

    ...

    path: /home/<user-name>/<some-path>/mongodb/mongod.log

  ...

# Create directory
  mkdir /home/<user-name>/<some-path>/mongodb/

# Change permission (!important)
  chown mongodb:mongodb /home/<user-name>/<some-path>/mongodb/

# Move data from previous to new directory
  mv /var/lib/mongdb/ /home/<user-name>/<some-path>/mongodb/

# Start MongoDB service
  sytemctl start mongod

# Confirm status
  systemctl status mongod
```

