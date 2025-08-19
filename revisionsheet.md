## **Midterm 1 Revision Sheet**

### **I. Multiple Choice & Short Answer Topics**

#### **1. Important Flags for Commands**
- **cd**: change directory  
  - `cd -`: switch to previous directory
- **ls**: list directory contents  
  - `-l`: long format  
  - `-a`: show hidden files  
  - `-h`: human-readable sizes
- **cp**: copy files  
  - `-r`: recursive (for directories)
- **mv**: move/rename files  
  - `-i`: prompt before overwrite
- **rm**: remove files  
  - `-r`: recursive (for directories)  
  - `-f`: force (no confirmation)
- **mkdir**: make directories  
  - `-p`: create parent directories as needed
- **rmdir**: remove empty directories
- **grep**: search using regex  
  - `-i`: case-insensitive  
  - `-v`: invert match (show lines that don’t match)  
  - `-r`: recursive
- **cut**: cut sections from lines  
  - `-d`: specify delimiter  
  - `-f`: specify fields
- **curl**: transfer data from URLs  
  - `-O`: download file with its original name  
  - `-L`: follow redirects
- **echo**: print to the terminal
- **read**: read input from stdin
- **git**: version control  
  - `git clone`: clone repository  
  - `git commit -m`: commit with a message  
  - `git push`: push to remote repo
- **tar**: archive utility  
  - `-c`: create archive  
  - `-x`: extract archive  
  - `-f`: specify filename  
  - `-v`: verbose (list files processed)

#### **2. Paths**
- **Absolute Path**: starts from root `/`  
  Example: `/home/user/documents/file.txt`
- **Relative Path**: starts from current directory  
  Example: `./documents/file.txt`  
  - `.` refers to current directory  
  - `..` refers to parent directory

#### **3. Shell Wildcards**
- `*`: matches any number of characters  
  Example: `*.txt` matches all `.txt` files
- `?`: matches a single character  
  Example: `file?.txt` matches `file1.txt`, `file2.txt`, but not `file12.txt`
- `[]`: matches any one character inside the brackets  
  Example: `file[12].txt` matches `file1.txt` and `file2.txt`
- `{}`: sequence of alternatives  
  Example: `file{1,2}.txt` matches `file1.txt` and `file2.txt`

#### **4. String Matching with Regex**
- **Basic Symbols**:  
  - `.`: any single character  
  - `^`: start of line  
  - `$`: end of line  
  - `*`: 0 or more of the preceding character
  - `+`: 1 or more of the preceding character  
  - `[abc]`: matches 'a', 'b', or 'c'  
  - `\`: escape special character

#### **5. Permissions**
- **Representation**: `rwx` (read, write, execute)
  - `chmod` to change permissions  
    Example: `chmod 755 file.txt` (user: rwx, group: rx, others: rx)
  - **File Ownership**: `chown user:group file`

#### **6. Theoretical Role of the OS**
- **Key Functions of OS**:
  - Resource Management (CPU, memory, etc.)
  - Process Management (scheduling, multitasking)
  - File System Management (handling files, directories)
  - I/O System Management (input/output devices)
  - Security and Access Control

---

### **II. Bash Scripting**

#### **1. Shebang Line**
- `#!/bin/bash`: Specify that the script should be run with the bash shell.

#### **2. Positional Parameters**
- `$1, $2, $3...`: Arguments passed to the script.
- Looping over parameters:
  ```bash
  for arg in "$@"; do
    echo "$arg"
  done
  ```

#### **3. Reading from stdin**
- **Basic Input**:
  ```bash
  read input_var
  echo "You entered: $input_var"
  ```
- **Reading and Looping Over Lines**:
  ```bash
  while read line; do
    echo "$line"
  done
  ```

#### **4. If Statements**
- **Basic Structure**:
  ```bash
  if [ condition ]; then
    # do something
  fi
  ```
- **Checking Command Success**:
  ```bash
  if command; then
    echo "Command succeeded"
  else
    echo "Command failed"
  fi
  ```
- **Comparisons**:
  - String comparison: `[ "$var" == "value" ]`
  - Numeric comparison: `[ "$num1" -eq "$num2" ]`
  
#### **5. For Loops to Iterate Over Files**
```bash
for file in *.txt; do
  echo "Processing $file"
done
```

#### **6. Command Substitution**
```bash
result=$(command)
echo "The result is: $result"
```

#### **7. Functions in Bash**
```bash
function_name() {
  # commands
}

function_name arg1 arg2
```

---

### **III. Key Commands Cheat Sheet**
- `cd <directory>`: Change directory
- `ls -l`: List files with details
- `cp <source> <destination>`: Copy files
- `mv <source> <destination>`: Move/Rename files
- `rm <file>`: Remove files
- `mkdir <directory>`: Create directory
- `rmdir <directory>`: Remove empty directory
- `grep <pattern> <file>`: Search for pattern in file
- `cut -d <delimiter> -f <fields>`: Cut sections of a file
- `curl <url>`: Transfer data from URL
- `echo <text>`: Print text
- `read <variable>`: Read input
- `git clone <url>`: Clone a Git repository
- `tar -cvf <archive.tar> <files>`: Create tar archive
- `tar -xvf <archive.tar>`: Extract tar archive