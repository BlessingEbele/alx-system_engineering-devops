# 0x03. Shell, init files, variables and expansions

## Task 0: `<o>`

### Script: `0-alias`

This script creates an alias named `ls` which is defined to run `rm *`.  
When the script is sourced using `source ./0-alias`, any call to `ls` will delete all files in the current directory.

**Usage:**
```bash
source ./0-alias
ls       # Deletes all files
\ls      # Runs the original ls command
