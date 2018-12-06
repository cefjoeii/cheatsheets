---
title: Ubuntu File
---

### File

```
  # Read the content
  cat <file-name>

  # Create if it doesn't exist
  touch <file-name>

  # Delete
  rm <file-name>

  # Copy
  cp <file-name> <file-name-2>

  # Rename or move
  mv <old-name> <some-path>/<new-name>
  
  # Search for the word and print each
  grep <key-word> <file-name>

  # Compare and display the difference
  diff <file-name> <file-name-2>

  # Get the result of whatever command and save it to a file
  <command-name> > <file-name>

  # Append the result to an existing file
  <command-name> >> <file-name>
```

### Checksum

```
  # Display the SHA1 value
  sha1sum <file-name>

  # Compare and highlight if matched
  sha1sum <file-name> | grep <checksum-code>
```
