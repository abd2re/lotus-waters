---
tags:
  - COMP206
---
# Streams

## Program and process
- A program is:: something you can run on a computer.
<!--SR:!2025-02-27,88,210-->
- A process is:: a running instance of a program.
<!--SR:!2024-12-10,56,250-->
- Each process is given a numeric ID called:: a process ID (PID).
<!--SR:!2025-01-10,77,270-->
- Each process had to be started by another process, except the very first one, with PID 1, which is started by:: the Linux kernel itself.
<!--SR:!2024-12-12,57,250-->
- Programs that can act as PID 1 are called:: init systems.
<!--SR:!2025-01-05,58,210-->
- The init system of most modern Linux systems is called:: systemd.
<!--SR:!2025-01-01,61,230-->

A file descriptor (FD) is:: a numeric identifier associated with each opened file. Used by the operating system to track open files for a process.
<!--SR:!2024-12-10,16,150-->

When a process A spawns a new process B, A is the parent process and B is the child process. The child process (B) inherits:: all open file descriptors from the parent process (A).
<!--SR:!2025-02-02,86,250-->

Each process has three special file descriptors by default:
?
  - `FD 0` is called standard input (`stdin`).
  - `FD 1` is called standard output (`stdout`).
  - `FD 2` is called standard error (`stderr`).
<!--SR:!2024-12-26,52,210-->

- This inheritance mechanism explains why:: when a program runs from the bash shell, its output appears on your terminal.
<!--SR:!2025-01-09,66,230-->

### Redirection
- **`>`**:: Redirect stdout (overwrite).
<!--SR:!2025-01-02,27,230-->
- **`>>`**:: Redirect stdout (append).
<!--SR:!2025-01-21,85,270-->
- **`2>`**:: Redirect stderr (overwrite).
<!--SR:!2024-12-09,54,250-->
- **`2>>`**:: Redirect stderr (append).
<!--SR:!2025-01-27,97,290-->
- **`<`**:: Redirect stdin.
<!--SR:!2025-01-31,91,270-->
- **`>&`**:: Redirect both stdout and stderr together.
<!--SR:!2024-12-12,19,190-->