# C Keywords: `volatile`, `extern`, and `register`

This document explains three important C keywords: **`volatile`**, **`extern`**, and **`register`**. Each plays a unique role in controlling storage, linkage, and optimization in C programming.

---

## 1. `volatile`

### Definition:
The **`volatile`** keyword is a type qualifier that tells the compiler **not to optimize** the variable because its value may change unexpectedly (outside normal program flow).

### Use Cases:
- Hardware registers (memory-mapped I/O)
- Shared variables in multithreading
- Signal handling

### Example:
```c
#include <stdio.h>

volatile int flag = 0; // Value may change unexpectedly

void someInterrupt() {
    flag = 1;  // Changed by interrupt
}

int main() {
    while (flag == 0) {
        // Compiler won’t optimize this away due to 'volatile'
    }
    printf("Flag changed!\n");
    return 0;
}
```

---

## 2. `extern`

### Definition:
The **`extern`** keyword is used to declare a global variable or function that is **defined in another file or scope**. It provides linkage between files.

### Use Cases:
- Accessing global variables across multiple `.c` files
- Sharing function declarations

### Example:
**file1.c**
```c
#include <stdio.h>

int counter = 10; // Defined here
```

**file2.c**
```c
#include <stdio.h>

extern int counter; // Declared here

int main() {
    printf("Counter = %d\n", counter);
    return 0;
}
```

---

## 3. `register`

### Definition:
The **`register`** keyword is a storage class specifier that suggests to the compiler that a variable should be stored in a **CPU register** instead of RAM (for faster access).

⚠️ Modern compilers usually ignore this hint and optimize automatically.

### Use Cases:
- Loop counters
- Frequently accessed small variables

### Example:
```c
#include <stdio.h>

int main() {
    register int i; // Suggest storing in CPU register
    for (i = 0; i < 5; i++) {
        printf("%d ", i);
    }
    return 0;
}
```

⚠️ You **cannot take the address** of a `register` variable using `&`.

---

## Summary Table

| Keyword   | Purpose | Example Use Case |
|-----------|---------|------------------|
| `volatile` | Prevents compiler optimizations for variables that may change unexpectedly | Hardware registers, interrupts |
| `extern`   | Declares variables/functions defined elsewhere | Sharing globals across files |
| `register` | Suggests storing variable in CPU register for fast access | Loop counters |

---

