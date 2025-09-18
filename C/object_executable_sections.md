# Object and Executable Format in C/C++

When source code is compiled, it is first translated into an **object file** (usually `.o` or `.obj`) and then linked to form an **executable file** (like `.exe` on Windows or `a.out` on Linux).  
These files follow a structured format (ELF in Linux, PE in Windows, Mach-O in macOS).

---

## Different Sections in an Object/Executable File

An object or executable typically has the following sections:

### 1. **.text (CODE Section)**
- Contains the **compiled machine code** (instructions to be executed).  
- Read-only and usually marked as executable.  

**C Example:**
```c
#include <stdio.h>

void hello() {
    printf("Hello, World!\n");
}

int main() {
    hello();
    return 0;
}
```
Here, the compiled instructions for `hello()` and `main()` go into the `.text` section.

---

### 2. **.data (Initialized DATA Section)**
- Contains **global and static variables that are initialized** by the programmer.  
- Both read and write permissions.  

**C Example:**
```c
#include <stdio.h>

int global_var = 42;   // Goes into .data

int main() {
    printf("%d\n", global_var);
    return 0;
}
```
Here, `global_var` is stored in the `.data` section because it has an initial value.

---

### 3. **.bss (Uninitialized DATA Section)**
- Contains **uninitialized global and static variables**.  
- At runtime, this section is filled with zeros.  

**C Example:**
```c
#include <stdio.h>

int counter;  // Goes into .bss (default initialized to 0)

int main() {
    printf("%d\n", counter);
    return 0;
}
```
Here, `counter` is placed in the `.bss` section.

---

### 4. **.rodata (Read-Only DATA Section)**
- Stores **constants, string literals, and constant variables**.  
- Marked read-only to prevent modification.  

**C Example:**
```c
#include <stdio.h>

const int limit = 100;        // Goes into .rodata
char *msg = "Hello, World!";  // String literal in .rodata

int main() {
    printf("%s\n", msg);
    return 0;
}
```
Here, `limit` and the string `"Hello, World!"` are placed in `.rodata`.

---

### 5. **Stack**
- Stores **local variables and function call information**.  
- Grows and shrinks dynamically during program execution.  

**C Example:**
```c
#include <stdio.h>

int main() {
    int x = 10;  // Stored on stack
    printf("%d\n", x);
    return 0;
}
```

---

### 6. **Heap**
- Used for **dynamically allocated memory** (`malloc`, `calloc`, `new` in C++).  
- Managed manually by the programmer.  

**C Example:**
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr = (int*)malloc(5 * sizeof(int)); // Stored in heap
    arr[0] = 42;
    printf("%d\n", arr[0]);
    free(arr);
    return 0;
}
```

---

## Summary Table

| Section  | Purpose | Example Variables | Permissions |
|----------|---------|-------------------|-------------|
| .text    | Machine code | Functions, main() | Read + Execute |
| .data    | Initialized globals/statics | `int x = 5;` | Read + Write |
| .bss     | Uninitialized globals/statics | `int y;` | Read + Write |
| .rodata  | Constants & string literals | `const int c = 10;` | Read-only |
| Stack    | Local variables | `int a = 20;` | Read + Write |
| Heap     | Dynamic memory | `malloc(), new` | Read + Write |

---

## Key Notes
- The `.text`, `.data`, `.bss`, and `.rodata` sections are part of the **object/executable file**.  
- The **stack** and **heap** exist at runtime in process memory, not in the object file.  
- Tools like `objdump`, `nm`, and `readelf` (Linux) or `dumpbin` (Windows) can be used to inspect these sections.

