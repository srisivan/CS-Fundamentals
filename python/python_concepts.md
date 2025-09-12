# Python Programming Concepts

## 1. Prefix and Postfix Operators

In Python, **there are no explicit prefix or postfix increment/decrement operators** like C (`++a` or `a++`).  
Instead, Python uses `+= 1` or `-= 1` for increment and decrement.

### Example in Python
```python
a = 5

# Equivalent to prefix increment (++a in C)
a += 1
print("After increment:", a)

# Equivalent to decrement (--a in C)
a -= 1
print("After decrement:", a)
```

---

## 2. Structures and Unions

Python does not have `struct` or `union` keywords like C. Instead, it uses:

- **Classes** → similar to structures (group variables and methods).  
- **NamedTuples / Dataclasses** → lightweight alternatives.  
- **Unions** (from `typing` module) → specify that a variable can take multiple types, not memory-sharing like in C.

### Example: Class (like Structure)
```python
class Student:
    def __init__(self, roll, name, marks):
        self.roll = roll
        self.name = name
        self.marks = marks

s1 = Student(1, "Alice", 88.5)
print(f"Roll: {s1.roll}, Name: {s1.name}, Marks: {s1.marks}")
```

### Example: Union Type
```python
from typing import Union

def process(value: Union[int, float, str]):
    print("Value is:", value)

process(10)
process(3.14)
process("Hello")
```

---

## 3. Conditional Statements

Python supports similar conditional constructs as C but uses indentation instead of braces `{}`.

### if Statement
```python
x = 10
if x > 5:
    print("x is greater than 5")
```

### if-else Statement
```python
x = 3
if x % 2 == 0:
    print("Even")
else:
    print("Odd")
```

### if-elif-else Ladder
```python
score = 85
if score >= 90:
    print("Grade A")
elif score >= 75:
    print("Grade B")
else:
    print("Grade C")
```

### match-case (Python 3.10+)
```python
day = 3
match day:
    case 1: print("Monday")
    case 2: print("Tuesday")
    case 3: print("Wednesday")
    case _: print("Other day")
```
