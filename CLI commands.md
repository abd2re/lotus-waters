---
tags:
  - COMP206
---
# CLI commands

## Paths

- A _path_ is a:: (specially formatted) string that locates an entry in a filesystem.
<!--SR:!2025-03-28,122,250-->
- `pwd` stands for:: "print working directory".
<!--SR:!2025-01-03,79,270-->
- The very first `/` in a path means:: "start at the root of the filesystem".
<!--SR:!2025-02-26,104,250-->
- The root is the topmost directory in the whole filesystem.
- `home/` means:: then go into the `home` subdirectory.
<!--SR:!2025-04-15,134,250-->
- A path is _absolute_ when:: it **begins at the root.**
<!--SR:!2024-12-15,64,270-->
- Paths not beginning with a slash are called:: **relative paths.** They are interpreted _relative to_ the current working directory.
<!--SR:!2025-02-15,97,250-->
- A shorthand for our current directory is:: `.`.
<!--SR:!2025-06-10,194,310-->
- A shorthand for our parent's directory is:: `..`.
<!--SR:!2025-06-13,197,310-->
- A shorthand for the absolute path to the current user's home directory is:: the tilde `~`.
<!--SR:!2025-01-26,91,270-->

## File and Directory Operations

### Creating and Navigating

- To create a new file we use:: `touch`.
<!--SR:!2025-01-14,83,270-->
- To create a new directory we use:: `mkdir`.
<!--SR:!2024-12-23,69,270-->
- To change directory, we use:: `cd`.
<!--SR:!2025-03-19,132,290-->

### Listing and Viewing

- To see the components of a directory, we use:: `ls`.
<!--SR:!2025-06-10,194,310-->
- To see **all** (with hidden) components of a directory, we use:: `ls -a`.
<!--SR:!2025-04-18,142,270-->
- To see the components **and** subcomponents of a directory, we use:: `tree`.
<!--SR:!2024-12-24,69,270-->
- To read a file we can use these commands:: `cat, less, vim, nano, ...`
<!--SR:!2025-01-05,77,270-->

### Copying, Moving, and Removing

- To copy a file to another destination we do:: `cp FILE DST`
<!--SR:!2025-04-08,129,250-->
- To copy a directory to another destination we do:: `cp DIR DST -r`
<!--SR:!2024-12-11,59,250-->
- To remove a file we do:: `rm FILE`
<!--SR:!2025-02-26,115,290-->
- To move a file to another destination we do:: `mv FILE DST`
<!--SR:!2024-12-31,50,230-->
- To move a directory to another destination we do:: `mv DIR DST`
<!--SR:!2024-12-16,31,210-->
- To remove a directory we can do (2):: `rm DIR -r` or `rmdir DIR` (if the directory is empty)
<!--SR:!2025-01-25,84,250-->
- To rename an entry (file/directory) we do:: `mv ENTRY OTHER` where `OTHER` is another entry.
<!--SR:!2025-03-20,117,250-->

## Arguments

- The argument `-a` means:: all.
<!--SR:!2025-01-16,85,270-->
- The argument `-r` means:: recursively
<!--SR:!2025-03-11,124,290-->

## Wildcards
- A wildcard for matching any number of characters is:: `*`.
<!--SR:!2024-12-10,3,142-->
- A wildcard for matching exactly one character is:: `?`.
<!--SR:!2025-01-10,72,262-->
- A wildcard for matching any chosen one character is:: `[ ]` where we put characters/ranges inside the brackets (you can also use `!` to negate).
<!--SR:!2025-01-12,43,222-->

## Archiving and Extracting
- **Create an archive**:  
  Use `tar -cf ARCHIVE.tar FILE1 FILE2 ...` to:: create an archive (`.tar` file) containing multiple files or directories.
<!--SR:!2025-01-20,67,242-->
  - `-c` stands for "create" an archive.
  - `-f` specifies the filename of the archive.

- **List contents of an archive**:  
  Use `tar -tf ARCHIVE.tar` to:: display the contents of an archive without extracting it.
<!--SR:!2025-01-03,67,262-->
  - `-t` stands for "list" the contents.
  - `-f` specifies the filename of the archive.

- **Extract an archive**:  
  Use `tar -xf ARCHIVE.tar` to:: extract files from an archive.
<!--SR:!2024-12-30,65,262-->
  - `-x` stands for "extract" files from the archive.
  - `-f` specifies the filename of the archive.

- **Extract to a specific directory**:  
  Use `tar -xf ARCHIVE.tar -C /path/to/directory` to:: extract an archive to a specified directory.
<!--SR:!2025-02-09,84,242-->
  - `-C` changes to the directory specified before performing the extraction.

- **Compress an archive using gzip**:  
  Use `tar -czf ARCHIVE.tar.gz FILE1 FILE2 ...` to create a compressed archive using gzip.  
  - `-z` stands for compressing with gzip.

- **Compress an archive using bzip2**:  
  Use `tar -cjf ARCHIVE.tar.bz2 FILE1 FILE2 ...` to create a compressed archive using bzip2.  
  - `-j` stands for compressing with bzip2.

- **Extract a gzip-compressed archive**:  
  Use `tar -xzf ARCHIVE.tar.gz` to extract files from a gzip-compressed archive.  
  - `-z` option is included to decompress gzip.

- **Extract a bzip2-compressed archive**:  
  Use `tar -xjf ARCHIVE.tar.bz2` to extract files from a bzip2-compressed archive.  
  - `-j` option is included to decompress bzip2.

- **Show verbose output**:  
  Add the `-v` flag (e.g., `tar -xvf ARCHIVE.tar`) to:: show detailed output of the files being processed.
<!--SR:!2025-01-21,81,282-->
  - `-v` stands for "verbose" mode, providing more details.
  
A tarbomb is:: a tarball that, when extracted, releases its contents into the current directory, potentially cluttering it or overwriting existing files.
<!--SR:!2025-03-23,114,262-->