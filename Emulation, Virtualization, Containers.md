---
tags: []
---
# Emulation, Virtualization, Containers

- Each process pretends that it has access to:: the full memory of the computer, but it only has access to virtual addresses.
<!--SR:!2024-12-08,7,250-->
- The CPU translates virtual addresses into:: physical addresses
<!--SR:!2024-12-10,9,250-->

5 levels of virtualization are:
?
1. Emulator
2. Virtual machine
3. Container
4. Interpreted programming languages
	4.5. Just-In-Time (JIT) compilation
5. Native code execution
<!--SR:!2024-12-10,9,250-->


## Emulator
- An emulator simulates:: the complete hardware of another machine, including its CPU.
<!--SR:!2024-12-11,10,250-->
- It is effectively an interpreter for:: the machine code of a different CPU architecture.
<!--SR:!2024-12-04,2,170-->
- Commonly used for old computers, because CPU simulation is:: very slow.
<!--SR:!2024-12-08,7,250-->

## Virtual machine
- A virtual machine simulates:: all the hardware except the CPU.
<!--SR:!2024-12-09,8,250-->
- Machine code from inside the VM is run:: directly on the physical CPU.
<!--SR:!2024-12-08,7,250-->
- We have good security between VMs because:: there is a very high degree of isolation between VMs.
<!--SR:!2024-12-09,8,250-->
- Software used to run a VM is called:: a **hypervisor**.
<!--SR:!2024-12-10,9,250-->
- The machine running the hypervisor is called:: the host.
<!--SR:!2024-12-08,7,250-->
- The VM is called:: a guest.
<!--SR:!2024-12-05,2,190-->

There are two kinds of hypervisors:
?
- **Type 1 hypervisor**:  Runs on “bare metal”. The hypervisor runs directly on the hardware. It is essentially a “very thin” OS that runs exactly one program, i.e. the virtualization software used to run the VMs. Often used in servers. ![[image-20241127172024699.png]]
- **Type 2 hypervisor**: Is an “ordinary application”. Often used by developers or powerusers. You can try out different OSes in a lightweight way. Run apps for other OSes without actually needing to install that OS on your computer. Mobile app development. ![[image-20241127172343021.png]]
<!--SR:!2024-12-07,6,250-->



By using a hypervisor to isolate virtual machines and manage access to CPU (which has some prebuilt security levels), ensuring:: each guest OS operates in its own secure environment.
<!--SR:!2024-12-10,9,250-->

## Containers
- A container shares:: the OS kernel of the host with the guest.
<!--SR:!2024-12-06,4,210-->
- Containers isolate:: individual application processes using the host OS kernel, rather than virtualizing an entire operating system for each instance.
<!--SR:!2024-12-05,4,230-->
- Each process inside the container is actually:: a process running on the host.
<!--SR:!2024-12-06,5,230-->
- The virtualization for containers is provided by:: the OS kernel.
<!--SR:!2024-12-07,6,250-->

VMs vs Containers:
?
![[image-20241127174141434.png]]
<!--SR:!2024-12-09,8,250-->


## Interpreted programming languages
- The same program can run on:: any computer/OS for which an interpreter is written.
<!--SR:!2024-12-09,8,250-->
- Often compiled into:: bytecode, which is what the interpreter interprets.
<!--SR:!2024-12-11,10,250-->
- Is there isolation ?: No.

### Just-In-Time (JIT) compilation
- Use an interpreter at first, but:: collect usage statistics to guide native-code compilation of select, high-profile functions.
<!--SR:!2024-12-11,10,250-->

## Native code execution
- Source code is compiled directly into:: machine code.
<!--SR:!2024-12-09,8,250-->
- Many CPUs actually use an internal interpreter written in a special language called:: microcode that is not exposed to the programmer.
<!--SR:!2024-12-06,5,230-->