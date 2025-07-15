---
tags:
  - COMP273
---
# Linker

Compiler generates:: assembly code and directives that respect conventions.
<!--SR:!2025-04-19,23,230-->

Assembler actions:
?
- Reads and Uses Directives
- Replace Pseudoinstructions
- Produce Machine Language
- Creates Object File
<!--SR:!2025-04-14,1,130-->

Object File Format
?
- **object file header**: size and position of the other pieces of the object file
- **text segment**: the machine code
- **data segment**: binary representation of the data in the source file
- **relocation table**: identifies lines of code that need to be “handled”
- **symbol table**: list of this file’s labels and data that can be referenced
- **debugging information**
<!--SR:!2025-05-16,42,250-->

Linker actions:
?
- Step 1: Combine text segment from each .o file
- Step 2: Combine data segment from each .o file, and concatenate this onto end of text segments
- Step 3: Resolve References – Go through Relocation Table – Handle each entry using the Symbol Table. That is, fill in all absolute addresses.
![[Pasted image 20250305142635.png]]
<!--SR:!2025-04-27,16,150-->


Four Types of Addresses
?
- PC-Relative Addressing (`beq`, `bne`): – never fix up (never “relocate”)
- Absolute Address (`j`, `jal`): – always relocate
- External Reference (usually `jal`): – always relocate
- Symbolic Data Reference (often `la`, `lw`, `sw`): – always relocate
<!--SR:!2025-04-14,6,150-->

Loader actions
?
- Reads executable file’s header to determine size of text and data segments
- Creates new address space for program large enough to hold text and data segments, along with a stack segment
- Copies instructions and data from executable file into the new address space
<!--SR:!2025-04-19,8,130-->

Compiler →:: Assembler → Linker (→ Loader).
<!--SR:!2025-05-12,40,250-->

Assembler does 2 passes to:: resolve addresses, handling internal forward references.
<!--SR:!2025-04-18,14,170-->

Steps to Starting a Program
?
![[Pasted image 20250305161436.png]]
![[Pasted image 20250305161445.png]]
<!--SR:!2025-04-24,20,170-->

