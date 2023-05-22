# C Programming

## Strings 

String declaration:
```c
char* name = "John";

// Compiler calculates length of array automatically
char name[] = "John";
```
Methods: 
- string length: `strlen()`
- string concatenation: `strcat()`
- string comparison: `strcmp()`
- string copy: `strcpy()`

## Functions

Pass by value:
```c
void foo(int val){
  val++; 
  printf("%d\n", val);
}

// Usage
int a = 1; 
foo(a); // a = 1, prints 2
```

Pass by reference:
```c
void foo(int* val){
  *val++; 
  printf("%d\n", val);
}

// Usage
int a = 1; 
foo(a); // a = 2, prints 2
```

## Decision Control Statements 

### If-Else
```c
if (isFirst) {
    // do something
} else if (isSecond) {
    // do something else
} else {
  // default do something
}
```

### Switch-Case
```c
switch (val) {

    // val == val1
    case val1:
        // do something
        break;

    // val == val2
    case val2:
        // do something else
        break;
    default:
        // default do something
        break;
}
```

## Variables & Types: 

Static variable: Expands scope of the variable to the entire file. 
Static function: Limits scope of the function to the entire file.

### Structs 
Usage:
- Serialize data into a single variable
- Create a data structure that can be used to store multiple data types
- Pass multiple arguments through a single variable 
```c

// Define struct type called my_struct
typedef struct {
    int a;
    char b;
    float c;
} my_struct;

// Create instance of my_struct & assign values
my_struct my_instance = {
  .a = 1,
  .b = 'a',
  .c = 3.14
}

// Modify values of my_instance
my_instance.a = 2;

```

### Union 
Each member of the datastructure is stored in the same memory location.
```c

// Declare union named my_union
union my_union {
    int a;
    char b;
    float c;
} my_union;

// Create instance of my_union 
union my_union U; 
U.a = 1;
U.b = 'a';

printf("%c\n", U.a); // Prints 'a'

```

### Memory Size 
8 Bits = 1 Byte 

(Assuming 32 bit OS, if 64 bit OS, then int and long length are double)
Type | Size | Value
---|---|---
char | 1 Byte | 0 - 255
int | 2 Bytes | -32,768 - 32,767
long | 4 Bytes | -2,147,483,648 - 2,147,483,647
float | 4 Bytes | 3.4E-38 - 3.4E38
double | 8 Bytes | 1.7E-308 - 1.7E308

### Volatile
Keyword that indeicates to the compiler that a vraible value can change at any time externally without any task in the source code triggering that change. 

## Arrays 

Dynamic 2D Array: 
```c
// Allocate top level pointer 
int **top = NULL; 
top = (int**)malloc(n*sizeof(int*));

// Allocate memory for each row
for (int i = 0; i < n; i++) {
    top[i] = (int*)malloc(m*sizeof(int));
}
```

## Pointers

### Pointer Arithmetic
Manipulate pointer address directly:
```c
int array[3] = {1, 2, 3};
int *ptr = &array[1];
ptr++; // Increment pointer's address by 1

printf("%d\n", *ptr); // Prints array[2]
```

### Dangling Pointer
Pointer assigned to a memory location that is no longer valid:
```c
void foo(int *ptr){
  int val = 10; 
  ptr = &val;
}
```

### Function Pointers
Structure: (return)(pointer to function)(arguments) => return(*ptr)(args);
```c
void (*ptr)(int); // Function pointer

// Array of function pointers 
void (*funcs[])(int) = {f1, f2, f3};

// Call
funcs[i](1);
```

### Void Pointer
Pointer which at compile time has an unknown type which is cast at runtime.
```c
void *ptr;

int val = 1;
ptr = &val;
printf("%d\n", *(int*)ptr); // Prints 1
```

## Bit Masks 
To manipulate given bit n: 

Set: `val |= (1 << n)`

Clear: `val &= ~(1 << n)`

Flip: `val ^= (1 << n)`

Check: `if(val & (1 << n))`

### Bit Masking Example
```c
#include <stdio.h>
#include <assert.h>

/* Finish initializing the flags */

const short FLAG_ON          = 1 << 0; // 1  (0x01)
const short FLAG_MOVEMENT    = 1 << 1; // 2  (0x02)
const short FLAG_TRANSPARENT = 1 << 2; // 4  (0x04)
const short FLAG_ALIVE       = 1 << 3; // 8  (0x08)
const short FLAG_BROKEN      = 1 << 4; // 16 (0x10)
const short FLAG_EDIBLE      = 1 << 5; // 32 (0x20)

int main() {
  short attributes = 0;

  /* Set the attributes ON, TRANSPARENT, and BROKEN */
  attributes |= 1 << 0; 
  attributes |= 1 << 2;
  attributes |= 1 << 4;

  assert(attributes == (FLAG_ON | FLAG_TRANSPARENT | FLAG_BROKEN));

  /* Modify (set/clear/toggle) so the only attributes are ON and ALIVE */
  attributes |= 1 << 3;
  attributes &= ~(1 << 2);
  attributes &= ~(1 << 4);

  assert(attributes == (FLAG_ON | FLAG_ALIVE));

  /* Check if the ALIVE flag is set */
  assert(attributes & (1 << 3));

  /* Check if the BROKEN flag is not set */
  assert(attributes & ~(1 << 4));

  /* Modify so only the EDIBLE attribute is set */
  attributes = 0;
  attributes |= 1 << 5;

  assert(attributes == FLAG_EDIBLE);

  printf("Done!");
}
```

## Operators
Precedence:
1. Unary Operators: `!, +, -, ++, &, ~`
2. Mathematical Operators: `*, %, /`
3. Relational Operators: `<, >, <=, >=`
4. Equality Operators: `==, !=`
5. Logical Operators: `&&, ||`
6. Assignment: `=`

`continue`: Skip one iteration of the loop.
`break`: Break out of the loop.
`~a`: Bitwise complement of a (1's complement). 
`!a`: Logical complement of a (NOT a). 
`a++`: Return a, then increment by 1.
`++a`: Increment by 1, then return.
`<<`: Bitwise left shift.
`>>`: Bitwise right shift.
`&`: Bitwise AND.
`|`: Bitwise OR.
`^`: Bitwise XOR.

Difference between `++` and `+=`: `++` Is unary, it simply increments the value by 1. `+=` is binary, it adds the value and assigns it to the variable.

## Dynamic Memory

### Malloc
Allocate memory on the heap of a specific size.
```c
// Definition 
void *malloc(size_t size);

// Usage 
int *ptr = (int*)malloc(sizeof(int));
```
**Note:** calloc() is similar to malloc(), but it initializes the memory to 0.

### Realloc
Change the size of an allocated block of memory.
```c
// Definition
void *realloc(void *ptr, size_t size);

// Usage
int *first = (int*)malloc(sizeof(int));
int *second = realloc(first, 2*sizeof(int));
```

### Free
Deallocate memory on the heap.
```c
// Definition
void free(void *ptr);

// Usage
int *ptr = (int*)malloc(sizeof(int));
free(ptr);
```

### Examples 
```c
// Variable 
int *ptr = (int*)malloc(sizeof(int));

// Array
int n = 5; // Size of array
int *array = (int*)malloc(n*sizeof(int));

// Struct 
typedef struct {
    int a;
    char b;
    float c;
} my_struct; 

struct my_struct* st = (struct my_struct*)malloc(sizeof(struct my_struct));
```

# Assembly Programming

Assembly has 3 basic types of statements: 
1. Executable instructions or instructions: tell the processor what to do
2. Assembler directives or pseudo-ops: tell the assembler about the various aspects of the assembly process (non-executatble)
3. Macros: a text substitution mechanism

General Syntax: 
```asm
[label]   mnemonic   [operands]   [;comment]
```

## Registers 
In general, there are a special registers as follows, other registers are special to the: 
**R0 (PC):** Program Counter - The address of the next instruction to be executed.
**R1 (SP):** Stack Pointer - The address of the top of the stack.

## Commands 

### Hello World in Assembly
```asm
section	.text
   global _start     ;must be declared for linker (ld)
	
_start:	            ;tells linker entry point
   mov	edx,len     ;message length
   mov	ecx,msg     ;message to write
   mov	ebx,1       ;file descriptor (stdout)
   mov	eax,4       ;system call number (sys_write)
   int	0x80        ;call kernel
	
   mov	eax,1       ;system call number (sys_exit)
   int	0x80        ;call kernel

section	.data
msg db 'Hello, world!', 0xa  ;string to be printed
len equ $ - msg     ;length of the string
```

# Rust Programming

# ROS Programming