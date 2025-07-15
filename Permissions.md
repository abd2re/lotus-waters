---
tags:
  - COMP206
---
# Permissions
## File Permissions
- File permissions in Unix are:: defined as a set of flags that dictate who can read, write, or execute a file.
<!--SR:!2024-12-31,38,170-->
- The first character represents:: the file type (`-` for regular files, `d` for directories).
<!--SR:!2024-12-12,56,250-->
- The next 9 characters are:: divided into three sets of three characters, representing the permissions for the owner, group, and others.
<!--SR:!2025-01-13,80,270-->

The three characters can be:
?
  - `r` for read
  - `w` for write
  - `x` for execute
  - `-` means the permission is not granted.
<!--SR:!2024-12-17,59,250-->

## Changing Permissions
- The `chmod` command is used to:: change the permissions of a file or directory.
<!--SR:!2024-12-19,56,230-->
- To change permission of an entry we do::`chmod 755 entry` sets the permissions to:: `rwxr-xr-x`.
<!--SR:!2025-04-11,127,250-->

Numeric codes can be used:
?
  - `4` stands for read
  - `2` stands for write
  - `1` stands for execute
- Combined, these sum to set permissions
  - `7` (rwx) (4+2+1)
  - `6` (rw-) (4+2)
  - `5` (r-x) (4+1)
  - `0` (---)
<!--SR:!2024-12-15,53,230-->

## File Ownership
- Each file in Unix is associated with:: an owner and a group.
<!--SR:!2024-12-14,41,210-->
- The owner has:: special permissions to the file that others do not.
<!--SR:!2025-03-25,117,250-->
- You can change the owner of an entry doing::  `chown newowner entry` command where `newowner` is the name of the new owner and `entry` is the name of the file/directoryy.
<!--SR:!2025-01-01,38,210-->

