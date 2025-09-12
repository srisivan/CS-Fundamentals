# C Concepts: Statements, #define, and Macros

## 1. Differences Between Types of Statements in C

In C, statements are instructions for the compiler to execute. Common types are:

### a) Declaration Statements
Used to declare variables or functions.
```c
int a;     // declares an integer variable
float b;   // declares a floating-point variable
```

### b) Assignment Statements
Assign values to variables.
```c
a = 10;    // assigns 10 to a
b = 20.5;  // assigns 20.5 to b
```

### c) Expression Statements
Expressions followed by a semicolon.
```c
a + b;     // expression statement, though result unused
a++;       // valid expression statement, increments a
```

### d) Control Statements
Control the flow of execution.
```c
if (a > b) {
    printf("a is greater");
} else {
    printf("b is greater");
}

for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
```

### e) Jump Statements
Alter the flow of execution.
```c
break;     // exits a loop or switch
continue;  // skips current iteration
return 0;  // exits a function
goto label; // jumps to a label
```

---

## 2. `#define` in C

`#define` is a preprocessor directive used to define constants or macros.

### Example (constant definition):
```c
#define PI 3.14159

int main() {
    float r = 5;
    float area = PI * r * r;
    printf("Area = %f", area);
    return 0;
}
```
Here, every occurrence of `PI` is replaced with `3.14159` before compilation.

---

## 3. Macros in C

Macros are fragments of code defined using `#define`. They can be simple or parameterized.

### a) Object-like Macros
Behave like constants.
```c
#define MAX 100

int arr[MAX];
```

### b) Function-like Macros
Act like inline functions.
```c
#define SQUARE(x) ((x) * (x))

int main() {
    int a = 5;
    printf("Square = %d", SQUARE(a));
    return 0;
}
```

⚠️ Be careful: Macros don’t perform type checking. For example:
```c
printf("%d", SQUARE(1+2));  // expands to (1+2 * 1+2) = 5 (not 9)
```

### c) Parameterized Macros with Safety
```c
#define SAFE_SQUARE(x) ((x) * (x))

printf("%d", SAFE_SQUARE(1+2)); // (1+2)*(1+2) = 9
```

---

# Summary
- **Statements**: Different categories control execution and logic.
- **#define**: Preprocessor replacement tool.
- **Macros**: Code snippets (constant or function-like) expanded before compilation.
