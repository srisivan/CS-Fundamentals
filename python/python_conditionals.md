# Conditional Statements in Python

Conditional statements allow programs to make decisions.

## 1. `if` Statement
Executes a block if condition is true.
```python
x = 10
if x > 0:
    print("x is positive")
```

## 2. `if-else` Statement
Alternative block when condition is false.
```python
if x % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

## 3. `if-elif-else` Ladder
Used when checking multiple conditions.
```python
day = 3
if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday")
else:
    print("Other day")
```

## 4. Nested `if`
Conditions inside conditions.
```python
if x > 0:
    if x < 100:
        print("x is between 1 and 99")
```

## 5. `match-case` (Python 3.10+)
Similar to `switch` in C.
```python
day = 3
match day:
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case _:
        print("Other day")
```

## 6. Ternary Expression
Shorthand for if-else.
```python
y = 1 if x > 0 else -1
print(y)
```

---
# Summary
- **if / if-else / if-elif-else** → General decision-making  
- **nested if** → Complex conditions  
- **match-case** → Equivalent to switch in C  
- **Ternary expression** → Compact conditional assignment
