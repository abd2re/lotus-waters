---
tags:
  - COMP206
---
# Bash Scripting
### Shebang
- The `#!/bin/bash` line (shebang) specifies:: the script should run in the Bash shell.
<!--SR:!2024-12-20,56,250-->

### Basic Commands
- Use commands like `echo` to:: print messages:
<!--SR:!2025-01-14,77,270-->
  ```bash
  echo 'Hello world!'
  ```

### Exit Status
- Use `exit` to:: end the script:
<!--SR:!2025-02-02,88,270-->
  ```bash
  exit 0  # 0 means success, non-zero means failure
  ```

### Variables
- Define variables with:: `=` (no spaces around):
<!--SR:!2025-03-19,109,250-->
  ```bash
  name="$USER"  # Assigns the current username to `name`
  ```
- Command-line arguments are accessed with:: `$1`, `$2`, etc.
<!--SR:!2024-12-16,54,250-->
- The number of command-line arguments passed are accessed with:: `$#`.
<!--SR:!2025-01-10,62,243-->

### Control Flow
- **If-else statements:**
?
  ```bash
  if ls ~; then
      echo 'Your home directory exists!'
  else
      echo 'Uh-oh...'
  fi
  ```
  - Use `fi` to close an `if` block.
  - Redirect output to suppress it: `ls ~ >/dev/null 2>&1`
<!--SR:!2024-12-09,49,250-->

- **Testing for Equality:**
?
  - Use `test` or `[ ]` for string comparisons:
  ```bash
  if [ "$1" = "--help" ]; then
      echo "helpful message"
  fi
  ```
  - Always quote variables to prevent errors with special characters or spaces.
<!--SR:!2025-01-09,40,230-->

### Special Variables
- `$?` holds:: the exit status of the last command.
<!--SR:!2025-02-06,77,230-->
- `$USER` is:: an environment variable for the current username.
<!--SR:!2024-12-24,59,250-->

### Quoting
- **Double Quotes** (`" "`): Allow:: variable expansion.
<!--SR:!2024-12-21,57,250-->
- **Single Quotes** (`' '`): Prevent:: variable expansion.
<!--SR:!2025-02-28,97,250-->

### Tips
- Double-quote variables to avoid:: word-splitting issues.
<!--SR:!2025-01-16,66,230-->
- Use `/dev/null` to:: discard unwanted command output.
<!--SR:!2025-04-01,117,250-->

### Function

To write/call a function with arguments we do:
?
```bash
function_name() {
  # commands
  # use $1, $2, etc. for accessing arguments
}

function_name x y z
```
<!--SR:!2025-01-09,64,249-->

### Loops

While loop
?
```bash
while [ condition ]; do
  # commands
done
```
<!--SR:!2025-02-18,76,209-->

Iterative for loop
?
```bash
for variable in list; do
  # commands
done
```
<!--SR:!2024-12-20,23,149-->

Range for loop
?
```bash
for (( initial_value; condition; increment )); do
  # commands
done
```
<!--SR:!2024-12-30,24,189-->

### Evaluations

We can do arithmetic evaluations with:: `(( ))`
<!--SR:!2024-12-21,50,243-->