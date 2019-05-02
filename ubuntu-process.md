---
title: Ubuntu Process
---

### Process

```bash
# Get processes list
  ps

# Get processes list including system processes
  ps ax

# Send an interrupt signal to get back terminal control
  [CTRL+C]

# Run the command in background and retain terminal control
  <command-name> &

# Get jobs list
  jobs

# Bring the background process into the foreground
  fg %<job-number>

# Pause the running background process
  [CTRL+Z]

# Terminate the process
  kill <process-id>

# Freeze the process
  kill -STOP <process-id>

# Unfreeze the process
  kill -CONT <process-id>
```

You can only kill processes that you own. To kill those can't, use `sudo`.
