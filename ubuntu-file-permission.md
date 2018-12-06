---
title: Ubuntu File Permission
---

### Indicator

`-` => a file<br>
`d` => a directory<br>
`r` => read<br>
`w` => write<br>
`x` => execute<br>

### Example

`-rwxrw-r--`<br>
`drwxrw-r--`

### Table

type | user | group | other
-- | -- | -- | --
\- | rwx | rw- | r--
d | rwx | rw- | r--

### Owner

`u` => user<br>
`g` => group<br>
`o` => other people (from the outside world)<br>

### Change mode for each owner

```
# Give (+) the others (o) permission to write
  chmod o+w <file-or-folder-name>

# Give (+) everyone permission to read and execute
  chmod +rx <file-or-folder-name>

# Remove (-) the group's (g) permission to execute
  chmod g-x <file-or-folder-name>
```

### Individual permission

`4` => read<br>
`2` => write<br>
`1` => execute<br>
`0` => no permissions<br>

### Figure

7 | 5 | 4
-- | -- | --
user | group | other
4+2+1 | 4+1 | 4
rwx | r-x | r--

### Change mode for multiple owners

```
# Give the directory and its subdirectories full permission
  chmod 777 -R <file-or-folder-name>

# Give multiple permission types
  chmod 754 <file-or-folder-name>
```

