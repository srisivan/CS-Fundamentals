# C Preprocessor Directives: Header Files, #error, and Conditional Compilation

## 1. Including Header Files

Header files in C contain function declarations, macros, and definitions. They are included using `#include`.

### a) Standard Header Files
Use angle brackets `<>` to include system-defined headers.
```c
#include <stdio.h>
#include <math.h>

int main() {
    printf("Square root of 16 is %.2f", sqrt(16));
    return 0;
}
```

### b) User-Defined Header Files
Use double quotes `""` to include files from the current directory.
```c
#include "myheader.h"

int main() {
    hello();  // function declared in myheader.h
    return 0;
}
```

---

## 2. `#error` Directive

The `#error` directive forces the compiler to stop and display an error message.  
Useful for catching invalid conditions at compile time.

```c
#if __STDC_VERSION__ < 199901L
    #error "C99 or later compiler required"
#endif

int main() {
    return 0;
}
```
If compiled with a compiler older than C99, this will stop with the error message.

---

## 3. Conditional Compilation: `#if`, `#elif`, `#else`, `#endif`

These directives allow compilation of code based on conditions.

### Example 1: Simple `#if` and `#else`
```c
#define VALUE 10

#if VALUE > 5
    #include <stdio.h>
    int main() {
        printf("Value is greater than 5");
        return 0;
    }
#else
    int main() {
        return 0;
    }
#endif
```

### Example 2: `#if`, `#elif`, `#else`
```c
#define MODE 2

#if MODE == 1
    #define MESSAGE "Mode 1 selected"
#elif MODE == 2
    #define MESSAGE "Mode 2 selected"
#else
    #define MESSAGE "Unknown mode"
#endif

#include <stdio.h>
int main() {
    printf("%s", MESSAGE);
    return 0;
}
```

---

# Summary
- **Header Files**: Included with `#include` (`<>` for system, `""` for user-defined).  
- **#error**: Generates custom compile-time error messages.  
- **#if / #elif / #else**: Used for conditional compilation to include/exclude code depending on conditions.
