# Data Types in C

## 1. What are Data Types?  
Data types define:
- The **type of data** a variable can hold (e.g., integer, character, floating-point).  
- The **amount of memory** reserved.  
- The **operations** that can be performed on that variable.

In C, data types are broadly classified into:

1. **Basic (Primitive) Data Types**  
   - `int`, `char`, `float`, `double`  

2. **Derived Data Types**  
   - Arrays, Pointers, Structures, Unions  

3. **Enumeration Data Type**  
   - `enum`  

4. **Void Data Type**  
   - `void`  

---

## 2. Basic Data Types in C

### (a) int  
- Used to store whole numbers (positive/negative).  
- Typical size: **4 bytes** (on most modern compilers).  
- Range (32-bit): `-2,147,483,648` to `2,147,483,647`.  

```c
#include <stdio.h>
int main() {
    int age = 25;
    printf("Age = %d\n", age);
    return 0;
}
```

---

### (b) char  
- Stores a **single character** or small integer (ASCII value).  
- Size: **1 byte**  
- Range: `-128 to 127` (signed) OR `0 to 255` (unsigned).  

```c
#include <stdio.h>
int main() {
    char grade = 'A';
    printf("Grade = %c\n", grade);
    return 0;
}
```

---

### (c) float  
- Stores real numbers with **single precision** (about 6 decimal digits).  
- Size: **4 bytes**  

```c
#include <stdio.h>
int main() {
    float pi = 3.14159;
    printf("Value of pi = %f\n", pi);
    return 0;
}
```

---

### (d) double  
- Stores real numbers with **double precision** (about 15 decimal digits).  
- Size: **8 bytes**  

```c
#include <stdio.h>
int main() {
    double price = 12345.6789012345;
    printf("Price = %lf\n", price);
    return 0;
}
```

---

## 3. Type Modifiers in C
Modifiers change the **size** or **sign** of basic data types.  

- `short int` → usually **2 bytes**  
- `long int` → usually **8 bytes**  
- `unsigned int` → only positive values (doubles positive range)  

```c
#include <stdio.h>
int main() {
    short int a = 32767;     // 2 bytes
    long int b = 2147483647; // 8 bytes
    unsigned int c = 4000000000; // 4 bytes, only positive
    printf("%hd, %ld, %u\n", a, b, c);
    return 0;
}
```

---

## 4. Derived Data Types

### (a) Arrays  
Collection of same type of data stored in contiguous memory.  
```c
int numbers[5] = {1, 2, 3, 4, 5};
```

### (b) Pointers  
Variables that store **addresses**.  
```c
int x = 10;
int *p = &x;
printf("Value: %d, Address: %p\n", *p, p);
```

### (c) Structures  
User-defined grouping of variables of different types.  
```c
struct Student {
    int roll;
    char name[20];
    float marks;
};
```

### (d) Unions  
Like structures, but **share memory** among members.  

---

## 5. Enumeration Data Type
Used to assign names to integral constants.  
```c
enum Week {Mon, Tue, Wed, Thu, Fri, Sat, Sun};
enum Week today = Wed;
printf("%d", today); // Output: 2
```

---

## 6. Void Data Type
- Represents **no value**.  
- Used in functions that don’t return anything.  
```c
void greet() {
    printf("Hello World!\n");
}
```

---

## 7. Memory Summary Table

| Data Type            | Typical Size (bytes) | Range / Precision |
|-----------------------|----------------------|------------------|
| `char`               | 1 byte              | -128 to 127 / 0–255 |
| `unsigned char`      | 1 byte              | 0 to 255 |
| `short int`          | 2 bytes             | -32,768 to 32,767 |
| `unsigned short int` | 2 bytes             | 0 to 65,535 |
| `int`                | 4 bytes             | -2.1B to 2.1B |
| `unsigned int`       | 4 bytes             | 0 to 4.2B |
| `long int`           | 8 bytes             | Huge range |
| `float`              | 4 bytes             | ~6 decimal digits |
| `double`             | 8 bytes             | ~15 decimal digits |
| `long double`        | 16 bytes            | ~18–19 digits |

*(Note: Sizes may differ on 16-bit, 32-bit, 64-bit systems, and compilers. Always use `sizeof(type)` in C to check.)*  
