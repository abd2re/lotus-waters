---
tags:
  - COMP206
---

# Piping
#### 1. Basic Pipe Syntax

Pipe (`|`):
?
Takes the output of one command and uses it as the input for another command.
  ```bash
  command1 | command2
  ```
<!--SR:!2025-01-06,75,270-->

#### 2. Common Commands Used with Pipes

`grep`:
?
Searches for patterns in text.
  ```bash
  ls -l | grep "pattern"
  ```
  - Options:
    - `-i`: Ignore case.
    - `-v`: Invert match (show lines that do not match).
    - `-n`: Show line numbers.
<!--SR:!2024-12-14,21,230-->

`sort`:
?
Sorts lines of text.
  ```bash
  cat file.txt | sort
  ```
  - Options:
    - `-r`: Reverse sort.
    - `-n`: Numeric sort.
<!--SR:!2024-12-08,53,250-->

`uniq`:
?
Removes duplicate lines from sorted input.
  ```bash
  cat file.txt | sort | uniq
  ```
  - Options:
    - `-c`: Count the occurrences of each line.
    - `-d`: Only show duplicate lines.
<!--SR:!2024-12-14,58,270-->

`cut`:
?
Cuts out sections from each line of files.
  ```bash
  cat file.txt | cut -d ',' -f 1
  ```
  - Options:
    - `-d`: Specify a delimiter.
    - `-f`: Select fields.
<!--SR:!2024-12-20,61,250-->

`awk`:
?
Pattern scanning and processing language.
  ```bash
  cat file.txt | awk '{print $1, $3}'
  ```
  - Example: Print the 1st and 3rd columns of each line.
<!--SR:!2024-12-22,15,150-->

`sed`:
?
Stream editor for filtering and transforming text.
  ```bash
  cat file.txt | sed 's/old/new/g'
  ```
  - Example: Replace all occurrences of 'old' with 'new'.
<!--SR:!2024-12-25,21,130-->

`wc -l`:: Count number of lines of output
<!--SR:!2025-02-03,76,240-->
#### 3. Combining Commands with Pipes

- Count lines containing a pattern:

  ```bash
  cat file.txt | grep "pattern" | wc -l
  ```

- Find the top 5 largest files in a directory:

  ```bash
  ls -l | sort -k 5 -n -r | head -5
  ```


- Show the 10 most common words in a file:
  ```bash
  cat file.txt | tr ' ' '\n' | sort | uniq -c | sort -nr | head -10
  ```
