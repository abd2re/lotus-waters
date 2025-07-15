### Operating System (OS) Role

- **Resource management:** Controls hardware (CPU, memory, I/O devices) and allocates resources efficiently.
- **Process management:** Schedules and manages running programs (processes), handles multitasking.
- **File system management:** Provides hierarchical file structure, file operations (read/write), and permissions.
- **Abstraction layer:** Offers a standard interface to interact with complex hardware systems.

---

### Paths

- **Absolute paths:** Begin with `/` (e.g., `/home/user/docs`). They describe the full directory route from the root directory.
- **Relative paths:** Based on the current working directory (e.g., `docs/` or `../parentDir`). No leading `/`.

---

### Shell Wildcards & String Matching

- `*` matches any string of characters (e.g., `ls *.txt` matches all `.txt` files).
- `?` matches exactly one character (e.g., `ls file?.txt` matches `file1.txt` but not `file10.txt`).
- `[abc]` matches any one character in the brackets.
- `{pattern1,pattern2}` matches either pattern1 or pattern2.

**Note:** These are shell filename expansion patterns, not full regex. For regex (often used with `grep`):

- `.` matches any single character.
- `^` matches start of line, `$` matches end of line.
- `*` matches zero or more of the preceding element.
- `[...]` character class, `|` alternation (OR), `()` grouping.

---

### Permissions

- **Permission sets:** `r` (read), `w` (write), `x` (execute).
- **Entities:** user (u), group (g), others (o).
- **Changing permissions:** `chmod u+x filename` adds execute permission for the user.
- **Symbolic vs. octal:** `chmod u+rwx,g+rx,o+r filename` or `chmod 755 filename`.

---

### Piping & Redirection

- **Piping (`|`):** Sends the standard output of one command to the standard input of another (e.g., `ls | grep "txt"`).
- **Redirection:**
    - `>` redirect stdout to a file (overwrite).
    - `>>` append stdout to a file.
    - `<` redirect file content as stdin.
    - `2>` redirect stderr.
    - `&>` redirect both stdout and stderr to a file.

---

### Bash Scripting Essentials

- **Shebang line:** `#!/usr/bin/env bash` at the top of scripts.
    
- **Positional parameters:** `$1`, `$2` for arguments; `$@` for all args.
    
- **Reading from stdin:** `read variable`, `while read line; do ... done`.
    
- **If statements:**
    
    ```bash
    if command; then
      # executes if command succeeded (exit status 0)
    fi
    
    if [ "$var" = "value" ]; then
      # string comparison
    fi
    ```
    
    Common tests:
    
    - `[ -f file ]` file exists and is a regular file
    - `[ -d dir ]` directory exists
    - `[ "$var" = "value" ]` string equals
    - `[ "$num1" -eq "$num2" ]` numeric comparison
- **For loops:**
    
    ```bash
    for file in *.txt; do
      echo "Processing $file"
    done
    ```
    
- **Command substitution:** `var=$(command)` captures command’s output into a variable.
    
- **Defining functions:**
    
    ```bash
    my_func() {
      echo "Function body"
    }
    ```
    

---

### Commands & Key Options

**cd** – Change directory

- `cd /absolute/path`
- `cd relativePath`
- `cd ..` go up one directory

**ls** – List directory contents

- `ls -l` long listing (permissions, ownership, size, date)
- `ls -a` show hidden files (starting with `.`)
- `ls -h` human-readable file sizes (often used with `-l`)

**cp** – Copy files and directories

- `cp source dest`
- `cp -r sourceDir destDir` copy directories recursively
- `cp -i` prompt before overwrite

**mv** – Move/rename files

- `mv oldName newName` (renames)
- `mv file /path/to/dest/` moves file to another directory
- `mv -i` prompt before overwrite

**rm** – Remove files/directories

- `rm file` remove file
- `rm -r dir` remove directory and contents
- `rm -i` interactive, `rm -f` force no prompt

**mkdir** – Create directory

- `mkdir newDir`
- `mkdir -p parent/child` creates parent if not exist

**rmdir** – Remove empty directory

- `rmdir emptyDir`

**grep** – Search text using patterns (regex)

- `grep pattern file` print lines that match
- `grep -i` case-insensitive
- `grep -r` recursive
- `grep -E` use extended regex

**cut** – Extract sections of lines

- `cut -fN` select the Nth field (used with `-d` to specify delimiter)
- `cut -d',' -f2 file.csv` gets the second column from a CSV

**curl** – Transfer data from/to server (HTTP)

- `curl URL` fetches URL content
- `curl -O URL` save to file with remote filename
- `curl -o localFile URL` save to custom filename
- `curl -I URL` fetch headers only

**echo** – Print text

- `echo "Hello"` prints "Hello"
- `echo $VAR` prints the value of VAR

**read** – Read input into variables

- `read var` reads one line of input into `var`

**git** – Version control

- `git clone URL` clone repository
- `git status` show changes
- `git add file` stage changes
- `git commit -m "msg"` commit staged changes
- `git push` push changes to remote
- `git pull` fetch and merge from remote

**tar** – Archive utility

- `tar -cvf archive.tar file(s)` create an archive
- `tar -xvf archive.tar` extract an archive
- `tar -czvf archive.tar.gz dir` create gzipped archive
- `tar -xzvf archive.tar.gz` extract gzipped archive
