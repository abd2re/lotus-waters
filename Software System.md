---
tags:
  - COMP206
---
# Software System
A software system is:: a set of communicating software artifacts (programs), together with their configuration files, documentation, etc., that work together to achieve a shared goal.
<!--SR:!2024-12-16,9,130-->

Primary function of an OS is:: managing the computer’s resources.
<!--SR:!2025-01-03,58,210-->

2 roles of the OS:
?
- “Insulates” applications running on a computer, both from the hardware of that computer and also from eachother.
- “Insulates” the user from the complex inner workings of the computer.
<!--SR:!2024-12-19,13,150-->


OS provides programmers with system libraries to perform OS-level operations, e.g. (4):: using network connections, allocating memory, managing files, using peripherals (bluetooth, USB, etc.).
<!--SR:!2024-12-10,13,130-->

OS is itself a system! Components include (4):: the kernel, the network stack, the filesystem, a hardware abstraction layer.
<!--SR:!2025-01-04,37,150-->

Kernel is just:: the core of the OS.
<!--SR:!2025-02-23,104,250-->

Kernel performs core OS functions, but what counts as “core”?. In a monolithic kernel, a lot (5+):: networking, filesystem, user accounts / permissions, memory management, device drivers, and even more.
<!--SR:!2024-12-28,38,170-->