---
tags:
  - COMP273
---
# IO interrupts

What must the processor do for I/O?
?
- Input: reads a sequence of bytes
- Output: writes a sequence of bytes
<!--SR:!2025-05-13,41,268-->

1 GHz microprocessor can execute:: 1 billion load or store instructions per second, or 4 GB/s data rate.
<!--SR:!2025-05-09,34,248-->


Processor Checks Status before Acting properties
?
![[Pasted image 20250313145259.png]]
<!--SR:!2025-04-15,4,130-->

I/O Control and Data Registers
?
![[Pasted image 20250313145434.png]]
![[Pasted image 20250313145757.png]]
<!--SR:!2025-04-15,3,148-->

Processor waiting for I/O called:: polling.
<!--SR:!2025-05-29,47,250-->


What is the alternative to polling?
?
![[Pasted image 20250313151122.png]]
<!--SR:!2025-04-20,12,228-->

I/O Interrupt
?
![[Pasted image 20250313151216.png]]
<!--SR:!2025-04-20,8,190-->


Exception, Interruption and Trap
?
![[Pasted image 20250313151536.png]]
<!--SR:!2025-04-20,20,208-->