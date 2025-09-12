# Conditional Statements in C

Conditional statements allow decision-making in programs.

## 1. `if` Statement
Executes a block of code if a condition is true.
```c
int x = 10;
if (x > 0) {
    printf("x is positive");
}
```

## 2. `if-else` Statement
Provides an alternative block when the condition is false.
```c
if (x % 2 == 0) {
    printf("Even number");
} else {
    printf("Odd number");
}
```

## 3. Nested `if` Statements
Multiple conditions checked inside each other.
```c
if (x > 0) {
    if (x < 100) {
        printf("x is between 1 and 99");
    }
}
```

## 4. `switch` Statement
Efficient way to test multiple constant values.
```c
int day = 3;
switch(day) {
    case 1: printf("Monday"); break;
    case 2: printf("Tuesday"); break;
    case 3: printf("Wednesday"); break;
    default: printf("Other day");
}
```

## 5. Ternary Operator `?:`
Compact way to write conditional logic.
```c
int y = (x > 0) ? 1 : -1; // if x > 0, y=1 else y=-1
printf("%d", y);
```

---
# Summary
- **if / if-else** → General conditions  
- **nested if** → Complex conditions  
- **switch** → Multi-branch conditions with constants  
- **?:** → Shorthand for if-else
