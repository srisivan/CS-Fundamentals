# C Programming Concepts

## 1. Prefix and Postfix Operators

In C, **increment (`++`)** and **decrement (`--`)** operators can be used in two forms:

- **Prefix**: The operator comes **before** the variable.  
  The operation is performed first, then the value is used.

- **Postfix**: The operator comes **after** the variable.  
  The current value is used first, then the operation is performed.

### Example in C
```c
#include <stdio.h>
int main() {
    int a = 5, b, c;

    b = ++a;  // prefix: a is incremented first, then assigned
    printf("Prefix: a = %d, b = %d\n", a, b);

    a = 5;
    c = a++;  // postfix: a is assigned first, then incremented
    printf("Postfix: a = %d, c = %d\n", a, c);

    return 0;
}
```
**Output:**
```
Prefix: a = 6, b = 6
Postfix: a = 6, c = 5
```

---

## 2. Structures and Unions

### Structures
- A **structure** is a user-defined data type that groups variables of different types under one name.
- Each member has **separate memory** allocation.

```c
#include <stdio.h>
struct Student {
    int roll;
    char name[20];
    float marks;
};

int main() {
    struct Student s1 = {1, "Alice", 88.5};
    printf("Roll: %d, Name: %s, Marks: %.2f\n", s1.roll, s1.name, s1.marks);
    return 0;
}
```

### Unions
- A **union** is similar to a structure, but **all members share the same memory location**.
- Only one member can hold a value at a time.

```c
#include <stdio.h>
union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    union Data data;

    data.i = 10;
    printf("i = %d\n", data.i);

    data.f = 3.14;  // overwrites i
    printf("f = %.2f\n", data.f);

    return 0;
}
```
**Key Difference:**
- Structure → memory allocated for all members (sum of sizes).
- Union → memory shared (size = largest member).

---

## 3. Conditional Statements

Conditional statements allow decision-making in programs.

### if Statement
```c
int x = 10;
if (x > 5) {
    printf("x is greater than 5\n");
}
```

### if-else Statement
```c
int x = 3;
if (x % 2 == 0)
    printf("Even\n");
else
    printf("Odd\n");
```

### else-if Ladder
```c
int score = 85;
if (score >= 90)
    printf("Grade A\n");
else if (score >= 75)
    printf("Grade B\n");
else
    printf("Grade C\n");
```

### switch Statement
```c
int day = 3;
switch(day) {
    case 1: printf("Monday\n"); break;
    case 2: printf("Tuesday\n"); break;
    case 3: printf("Wednesday\n"); break;
    default: printf("Other day\n");
}
```
