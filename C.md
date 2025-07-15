---
tags:
  - COMP206
---
# C

- To compile a program and run it we do:: `gcc source.c`, `./a.out`
<!--SR:!2025-01-13,49,250-->
- To compile a program into a custom name and run it we do:: `gcc -o my_program source.c`, `./custom`
<!--SR:!2024-12-16,34,270-->
- To enable a broad set of warning messages during compilation we do::`gcc -Wall -o my_program source.c`
<!--SR:!2025-01-28,57,250-->

The two most common included libraries are:
?
```c
#include <stdio.h>
#include <stdlib.h>
```
<!--SR:!2025-01-09,47,267-->

To print formatted output to the standard output we do:: `printf("Hello, %s!", "world");`
<!--SR:!2025-01-27,57,250-->
To read formatted input from the standard input:: `scanf("%d", &number);`
<!--SR:!2024-12-09,16,190-->
To read a character from standard in:: `char c=getc(stdin);`
<!--SR:!2025-01-16,45,230-->

`sizeof` runs at:: compile time.
<!--SR:!2025-01-12,47,250-->

Which type of data is `char`:: it's `int` type that represents a number between 0-255.
<!--SR:!2025-01-31,59,250-->


In C, when a function is called, the call stack is used to manage the function's execution context. Here’s what happens step-by-step:
?
1. **Pushing the Return Address**: The address to return to after the function finishes is pushed onto the stack.
2. **Allocating Space for Local Variables**: Space is reserved on the stack for the function’s local variables and any parameters passed to it. This forms the function's _stack frame_.
3. **Passing Arguments**: If arguments are passed to the function, they are typically pushed onto the stack, though sometimes they’re passed in registers depending on the system's calling convention.
4. **Updating the Stack Pointer**: The stack pointer (`SP`) adjusts to mark the top of the stack for the new frame.
5. **Executing the Function**: The program counter jumps to the function’s address, and the function begins executing with its own stack frame.
*When the function finishes:*
1. **Popping the Stack Frame**: The stack frame is removed, freeing memory for other uses.
2. **Returning to the Caller**: The return address is popped from the stack, and the program counter jumps back to the caller function.
<!--SR:!2025-01-16,42,227-->


- When we create an array of size $x$, the initializer has to be the same size as $x$?:: False, if the initializer `{a,b,...}` is shorter than $x$ in size, the rest is 0.
<!--SR:!2024-12-27,39,267-->
- If an array initializer is used, size can be omitted?:: True.
<!--SR:!2025-01-30,60,267-->


The size of an address on modern computers is:: 64 bits or 8 bytes.
<!--SR:!2025-02-03,58,247-->

A pointer is:: a variable that stores the memory address of another variable. It allows for indirect manipulation of the variable's value using `*` (dereference operator). Declared with `*`, e.g., `int *p;`.
<!--SR:!2025-01-30,56,247-->

We can have an address of a variable using:: `&`.
<!--SR:!2025-01-29,60,267-->

Local variables live on:: the (call) stack.
<!--SR:!2025-01-31,56,247-->
Arrays in C are:: pointers that point to the first element.
<!--SR:!2024-12-12,28,247-->

Can we return pointers to local variables in a call stack?:: We can but we should never do it because it's dangerous when the call stack of that function gets popped and other functions can have access to the space of the call stack and overwrite data. The reference will outlive the object/value.
<!--SR:!2024-12-10,26,247-->

Dynamic memory enables us to:: allocate a block of memory that outlives the current function.
<!--SR:!2025-01-16,46,247-->
The blocks of memory allocated using dynamic memory are stored in:: the heap (outside the call stack).
<!--SR:!2024-12-13,28,247-->

`void *` means:: a pointer that can hold the address of any data type (unknown size).
<!--SR:!2024-12-31,41,267-->

`malloc` and `free` functions' type and argument types:
?
```c
void *malloc(size_t n)
void free(void *p)
```
<!--SR:!2024-12-25,28,207-->

Pros and cons of dynamic memory:
?
**Pros**
- Can support very large allocations, unlike the stack.
- Allocated memory outlives function scope.
- Enables dynamic data structures, e.g. resizable arrays, linked lists, trees, and graphs.
**Cons**
- Memory leaks: forgetting to free a block is easy.
- Double-free and use-after-free security vulnerabilities.
- Performance: dynamic allocation is slower than stack allocation, and following chains of pointers thru dynamic memory is also slower than thru stack memory (which is cached and close to the CPU).
<!--SR:!2025-01-15,42,227-->


To allocate N bytes of memory on the heap we write:
?
```c
p = malloc(N)
```
where `p` is a pointer of any type. `malloc(N)` will return a pointer to that block.
<!--SR:!2024-12-19,33,247-->

To release a block previously obtained by malloc we write:
?
```c
free(p)
```
where `p` is any pointer that pointed at the beginning of the block.
<!--SR:!2024-12-11,26,247-->

Compilation is:: the process of translating source code written in a high-level programming language into a lower-level language, such as machine code, that can be executed by a computer.
<!--SR:!2024-12-16,30,246-->

Is machine code specific to the hardware architecture and the operating system ?:: Yes.
<!--SR:!2025-02-01,60,266-->

The compilation process different steps are:
?
- Preprocessing
- Compiling
- Assembling
- Linking
<!--SR:!2024-12-12,24,226-->

Illustration of the compiling process:
?
![[image-20241029133929859.png|center|400]]
<!--SR:!2024-12-08,22,226-->

1. The preprocessor performs the following actions:
?
- It removes all the comments in the source file(s).
- It includes the code of the header file(s), which is a file with extension .h which contains C function declarations and macro definitions.
- It replaces all of the macros (fragments of code which have been given a name) by their values.
<!--SR:!2024-12-08,20,226-->

The output of the preprocessing step will be stored in:: a file with a `.i` extension, so here it will be in `main.i`. In order to stop the compilation right after this step, we can use the option `-E` with the gcc command on the source file, and press Enter.
<!--SR:!2024-12-22,25,206-->

2. The compiler generates:: the IR code (Intermediate Representation) from the preprocessed file, so this will produce a `.s` file. That being said, other compilers might produce assembly code at this step of compilation. We can stop after this step with the `-S` option on the gcc command, and press Enter.
<!--SR:!2024-12-09,6,186-->
3. The assembler takes:: the IR code and transforms it into object code, that is code in machine language (i.e. binary). This will produce a file ending in `.o`. We can stop the compilation process after this step by using the option `-c` with the `gcc` command, and pressing Enter.
<!--SR:!2024-12-19,28,226-->
4. The linker creates:: the final executable, in binary. It links object codes of all the source files together. The linker knows where to look for the function definitions in the **static libraries** or the **dynamic libraries**. Static libraries are the result of the linker making a copy of all the used library functions to the executable file. The code in dynamic libraries is not copied entirely, only the name of the library is placed in the binary file.
<!--SR:!2024-12-16,29,246-->


Structures (`sturct`) are:: a collection of items that may have different types.
<!--SR:!2024-12-20,32,246-->
We access the elements of a `struct` using:: their name like dictionary in python.
<!--SR:!2024-12-20,31,246-->

Syntax of `struct`
?
```c
struct OPTIONAL_TAG { 
	MEMBERS; 
};
```
`OPTIONAL_TAG`: user-defined tag. If not present, we say the struct is anonymous
`MEMBERS`
	- Is a list of semi-colon separated variable declarations
	- `TYPE1 VAR1`; `TYPE2 VAR2`; etc.
	- Declared using `struct OPTIONAL_TAG car`
	- Note that we cannot initialize members from inside the struct definition (i.e. couldn't write `int age = 0;`)
	- We can declare global variables after the `}`
<!--SR:!2024-12-21,31,246-->


When assigning one `struct` to another of the same type (e.g., `b = a;`), the operation creates:: a _shallow copy_ of the struct. This means that each field in the source struct (`a`) is copied to the corresponding field in the target struct (`b`). For arrays within the struct, this results in a complete copy of the array elements rather than sharing the same memory (Pointer fields are copied as-is, meaning both structs will point to the same memory location if a pointer is present).
<!--SR:!2024-12-27,36,246-->

null in C::`NULL`
<!--SR:!2025-01-02,39,266-->

Syntax of `typedef struct`
?
```c
struct OPTIONAL_TAG { 
	MEMBERS; 
} NEW_ALIAS;
```
- Declared using `NEW_ALIAS var` or `struct OPTIONAL_TAG var`
<!--SR:!2024-12-17,29,246-->

To declare a list of struct:: `struct TAG var[N];`
<!--SR:!2024-12-08,26,266-->

**`sizeof(struct)`**: Returns:: the total size of a struct, including the size of all data members plus any padding bytes added by the compiler to align data members to the system’s memory boundaries for efficient access.
<!--SR:!2024-12-24,33,246-->


Syntax of `union`
?
```c
union OPTIONAL_TAG { 
	FIELDS; 
};
```
<!--SR:!2024-12-15,28,246-->

With structs, the arrow syntax `->` is:: a sign that combines dereference and field access
<!--SR:!2024-12-24,30,242-->

A `union` in C is a data structure similar to a struct, but with a key difference:: while a struct allocates separate memory for each of its members, a union shares the same memory space for all its members. This means that a union can only hold one of its members' values at a time, and its size is equal to its largest member.
<!--SR:!2024-12-24,33,246-->

Updating one member in a union:: overwrites the others due to the shared memory.
<!--SR:!2024-12-08,24,246-->

To define a rule in a Makefile, you:: start with the target name, followed by a colon, and then the dependencies.
<!--SR:!2024-12-12,26,246-->

The default target is:: the first target listed in the Makefile unless another target is specified when running `make`.
<!--SR:!2024-12-10,25,246-->

Makefile template:
?
```bash
# Compiler and flags
CC = gcc
CFLAGS = -Wall -Wextra -g

# Target program name and source files
TARGET = my_program
SRC = main.c utils.c

# Default target
all: $(TARGET)

# Rule to build the target program
$(TARGET): $(SRC)
	$(CC) $(CFLAGS) -o $(TARGET) $(SRC)

# Phony target to run the program
.PHONY: test
test: $(TARGET)
	./$(TARGET)

# Phony target to clean up generated files
.PHONY: clean # optional, only to be safe
clean:
	rm -f $(TARGET)
```
<!--SR:!2024-12-09,24,246-->

A file is:: an object stored in a permanent storage device like a hard disk, USB key, flash drive, etc. This is unlike internal storage devices: RAM, cache, and buffers.
<!--SR:!2024-12-11,9,206-->

Files come in two forms:: text and binary.
<!--SR:!2025-01-04,31,226-->

Files can be accessed in two modes:: sequentially and randomly.
<!--SR:!2024-12-09,21,246-->

- To access the file from the start address :: `FILE *fopen(const char *filename, const char *mode)`
<!--SR:!2025-01-09,43,246-->
- To terminate file access :: `int fclose(FILE *stream)`
<!--SR:!2025-01-05,41,246-->
- To read a single character from the file :: `int fgetc(FILE *stream)`
<!--SR:!2024-12-25,32,246-->
- To read one entire line from a file :: `char *fgets(char *buffer, int n, FILE *stream)`
<!--SR:!2024-12-17,11,226-->
- To write a single character to the file :: `int fputc(int char, FILE *stream)`
<!--SR:!2024-12-15,24,226-->
- To write one entire line to the file :: `int fputs(const buffer *str, FILE *stream)`
<!--SR:!2024-12-26,26,206-->
- To read a formatted line from the file :: `int fscanf(FILE *stream, const char *format, ...)`
<!--SR:!2024-12-24,34,246-->
- To write a formatted line to the file :: `int fprintf(FILE *stream, const char *format, ...)`
<!--SR:!2024-12-14,26,246-->
- End of the file test :: `int feof(FILE *stream)`
<!--SR:!2024-12-11,25,246-->
- To obtain the current file position of a stream:: `int ftell(FILE *stream)`
<!--SR:!2024-12-19,12,166-->

`fopen` syntax is with all its properties:
?
`FILE *fopen(FILENAME, MODE)`
- `FILE` is a built-in pointer type to reference a file (on success returns a pointer to the file, on failure returns a NULL pointer)
- `FILENAME` is a Unix path/filename descriptor as a string
- `MODE`: `rt` - read from text file (file must exist); `wt` - write to text file (if file exists, overwrites); `at` - append to text file (if file exists it appends, or creates file)
Remember to `fclose` when finished.
<!--SR:!2024-12-22,31,246-->

`fgets` syntax with all its properties:
?
`char *fgets(char *str, int n, FILE *stream)`
- Parameters:
    - `str`: Pointer to a character array (buffer) where the read string will be stored.
    - `n`: The maximum number of characters to read, including the null-terminator (`\0`).
    - `stream`: The file pointer of the file to read from (e.g., `stdin` or a file opened with `fopen`).
- Returns:
    - On success, it returns `str`.
    - On failure or when the end of file (EOF) is reached without reading anything, it returns `NULL`.
<!--SR:!2024-12-10,24,246-->

`fputs` syntax with all its properties:
?
`int fputs(const char *str, FILE *stream)`
- Parameters:
    - `str`: Pointer to a null-terminated string to be written.
    - `stream`: The file pointer of the file to write to (e.g., `stdout` or a file opened with `fopen`).
- Returns:
    - On success, it returns a non-negative value.
    - On failure, it returns `EOF`.
<!--SR:!2024-12-18,17,226-->

`fseek` syntax with all its properties:
?
`int fseek(FILE *ptr, long int offset, int position)`
- `ptr` is a pointer to an opened file
- `offset` is the number of bytes to jump
- `position` is the direction to jump
	- `SEEK_END` jump backwards from end of the file
	- `SEEK_SET` jump forwards from beginning of the file
	- `SEEK_CUR` jump from current location
Return value
- 0 = success
- Anything else is an error
<!--SR:!2024-12-14,8,186-->


`strtod` syntax:
?
`double strtod(const char *str, char **endptr);`
- Converts string to double. `str` is the input string.
- `endptr` is set to the character after the last converted character or NULL if unused.
<!--SR:!2024-12-28,33,243-->

`strtol` syntax:
?
`long strtol(const char *str, char **endptr, int base);`
- Converts string to long. `str` is the input string.
- `endptr` is set to the character after the last converted character or NULL if unused.
- `base` specifies the number base (e.g., 10 for decimal, 16 for hexadecimal).
<!--SR:!2024-12-20,17,203-->


To exit a program we can do:: `exit(code)`
<!--SR:!2024-12-12,23,242-->