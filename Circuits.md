---
tags:
  - COMP273
---
# Circuits

## Circuits for Binary Arithmetic

1-Bit Half Adder
?
![[Pasted image 20250122215042.png|700]]![[Pasted image 20250122215307.png|400]]
<!--SR:!2025-08-06,118,250-->

1-Bit Full Adder
?
![[Pasted image 20250122215448.png|700]]
<!--SR:!2025-04-17,30,150-->

Multi-Bit Adder
?
![[Pasted image 20250122220016.png|700]]
<!--SR:!2025-05-20,66,230-->

Multi-Bit Subtractor
?
![[Pasted image 20250122220215.png|700]]
<!--SR:!2025-05-21,55,190-->

Potential problems multi-bit adder/subtractor:: Carry must ripple (propagate) through each adder.
<!--SR:!2025-04-21,54,250-->

Decoder circuit
?
![[Pasted image 20250122221726.png|700]]
<!--SR:!2025-04-16,7,170-->

Multiplexor circuit
?
![[Pasted image 20250122222453.png|700]]![[Pasted image 20250122223012.png|400]]![[Pasted image 20250122223156.png|700]]|
<!--SR:!2025-04-16,43,210-->

Read-only Memory (ROM) circuit table
?
![[Pasted image 20250127190916.png|700]]
<!--SR:!2025-05-19,64,233-->

Programmable Logic Array (PLA)
?
![[Pasted image 20250127190951.png|700]]
<!--SR:!2025-06-25,78,213-->

1 bit Arithmetic Logic Unit (ALU)
?
![[Pasted image 20250127191124.png|700]]
<!--SR:!2025-05-07,57,233-->

## Sequential circuits

- Combinatorial circuits have no:: memory. Output is simply a function of inputs.
<!--SR:!2025-05-02,53,233-->
- Sequential circuits contain:: “state”. Combinatorial circuits + memory. The mechanism for remembering information (i.e., bits) inside the CPU and in the main memory. Repeating itself the infomation.
<!--SR:!2025-05-10,59,233-->

RS Latch
?
![[Pasted image 20250127192851.png|700]]![[Pasted image 20250127193130.png|700]]
<!--SR:!2025-06-08,57,193-->

Clocks
?
![[Pasted image 20250127193454.png|700]]![[Pasted image 20250127193523.png|700]]
<!--SR:!2025-05-16,62,233-->

D Latch
?
![[Pasted image 20250127193816.png|700]] ![[Pasted image 20250127194210.png|700]]
- Still not good enough
- Data passes freely though the circuit while C =1. – Might want do things like x := x + 27
<!--SR:!2025-04-14,1,130-->

D flip-flop
?
![[Pasted image 20250127194530.png|700]]![[Pasted image 20250127194557.png|700]] ![[Pasted image 20250127204642.png|700]]
<!--SR:!2025-04-12,12,193-->

- Falling edge $\rightarrow$:: Master writes when clock is high; slave latches the value when clock goes low.
<!--SR:!2025-05-06,57,233-->
- Rising edge $\rightarrow$:: Master writes when clock is low; slave latches the value when clock goes high.
<!--SR:!2025-04-27,50,233-->

Toggle flip-flop
?
![[Pasted image 20250127215428.png|700]]
<!--SR:!2025-04-15,20,193-->

