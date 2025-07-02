# Data Types in C

## Primitive Types
- `int`: Integer numbers.
- `char`: Single character.
- `float`: Single-precision float.
- `double`: Double-precision float.
- `void`: No data.

## Qualifiers
- `signed` / `unsigned`: Controls sign.
- `short` / `long`: Changes size.

## Memory Size
- Platform dependent.
- Typical: `char` (1B), `int` (4B), `float` (4B), `double` (8B).

## Prefix/Postfix
- `++a` → Increment then use.
- `a++` → Use then increment.

## Structures
- Group multiple variables of different types.
- Example:
```c
struct Student {
  char name[50];
  int age;
};


