# Python Concepts: Statements, Constants, and Macro Alternatives

## 1. Differences Between Types of Statements in Python

In Python, statements are also units of execution:

### a) Declaration Statements
Python does not require explicit declarations. Variables are created when first assigned.
```python
x = 10
y = "Hello"
```

### b) Assignment Statements
Assign values to variables.
```python
x = 5
y = x + 2
```

### c) Expression Statements
Evaluate and return a value.
```python
print(x + y)
x + 10   # expression, though unused
```

### d) Control Statements
Direct the flow of code.
```python
if x > 0:
    print("Positive")
else:
    print("Non-positive")

for i in range(5):
    print(i)
```

### e) Jump Statements
Change control flow.
```python
for i in range(5):
    if i == 3:
        break
    if i == 1:
        continue
    print(i)
```

---

## 2. `#define` Equivalent in Python

Python does **not** support `#define`. Instead, constants are defined by convention using **UPPERCASE variables**.
```python
PI = 3.14159

r = 5
area = PI * r * r
print("Area =", area)
```

---

## 3. Macros in Python

Python does not have macros like C. Instead, the same functionality is achieved using:

### a) Functions
```python
def square(x):
    return x * x

print(square(5))  # Output: 25
```

### b) Lambdas (inline functions)
```python
square = lambda x: x * x
print(square(4))  # Output: 16
```

### c) Decorators (meta-programming, similar to function-like macros)
```python
def debug(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with args {args}, kwargs {kwargs}")
        return func(*args, **kwargs)
    return wrapper

@debug
def add(a, b):
    return a + b

print(add(3, 4))
```

---

# Summary
- **Statements** in Python: assignment, control, and expression are common.  
- **No #define or macros**: Instead, Python uses constants, functions, and decorators.  
- Functions provide the safe and Pythonic alternative to C macros.
