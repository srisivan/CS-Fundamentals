```markdown
# Data Types in C

## Types
- **int**, **char**, **float**, **double**, **void**, **short**, **long**, **signed**, **unsigned**

## Usage
Examples:
```c
int a = 5;
char c = 'A';
float f = 3.14;
```

## Memory Size
- `char` → 1 byte  
- `int` → 4 bytes  
- `float` → 4 bytes  
- `double` → 8 bytes

## Prefix/Postfix Operators
```c
int a = 1;
int b = ++a; // prefix: a=2, b=2
int c = a++; // postfix: a=3, c=2
```

## Structures & Unions
```c
struct Person {
  char name[20];
  int age;
};

union Data {
  int i;
  float f;
  char str[20];
};
```
