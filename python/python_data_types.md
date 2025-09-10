# Data Types in Python

## 1. What are Data Types?
In Python, data types tell us the **kind of value** a variable can hold and what **operations** can be performed on it.  
Unlike C, Python is dynamically typed — you don't need to declare the data type explicitly, it is inferred at runtime.

---

## 2. Basic Built-in Data Types in Python

### (a) int
- Stores whole numbers (positive/negative, unlimited precision).
- Memory usage grows with number size.

```python
age = 25
print("Age =", age)
```

---

### (b) float
- Stores floating-point numbers (decimal values).
- Typically 64-bit double precision.

```python
pi = 3.14159
print("Value of pi =", pi)
```

---

### (c) complex
- Stores complex numbers in the form `a + bj`.

```python
z = 2 + 3j
print("Complex number:", z)
```

---

### (d) bool
- Stores boolean values `True` or `False`.
- Internally represented as integers (1 and 0).

```python
is_active = True
print("Active?", is_active)
```

---

### (e) str
- Stores a sequence of characters (Unicode by default).

```python
name = "Alice"
print("Name:", name)
```

---

## 3. Collection Data Types

### (a) list
- Ordered, mutable collection of items.

```python
numbers = [1, 2, 3, 4, 5]
print(numbers)
```

---

### (b) tuple
- Ordered, immutable collection of items.

```python
point = (10, 20)
print(point)
```

---

### (c) set
- Unordered collection of unique items.

```python
fruits = {"apple", "banana", "cherry"}
print(fruits)
```

---

### (d) dict
- Key-value pairs (unordered, mutable).

```python
student = {"name": "Alice", "age": 20}
print(student)
```

---

## 4. NoneType
- Represents the absence of a value.

```python
x = None
print(x)
```

---

## 5. Memory and Size in Python
Unlike C, Python doesn’t have fixed sizes for data types (except floats which follow IEEE 754 double precision).  
You can check memory usage using `sys.getsizeof()`:

```python
import sys
print(sys.getsizeof(10))        # int
print(sys.getsizeof(3.14))      # float
print(sys.getsizeof("hello"))   # string
```

---

## 6. Summary Table

| Data Type  | Example                  | Mutable? | Notes |
|------------|--------------------------|----------|-------|
| `int`      | `10`                     | No       | Arbitrary precision |
| `float`    | `3.14`                   | No       | 64-bit double precision |
| `complex`  | `2+3j`                   | No       | Real + Imaginary parts |
| `bool`     | `True`, `False`          | No       | Subclass of int |
| `str`      | `"Hello"`                | No       | Unicode text |
| `list`     | `[1,2,3]`                | Yes      | Ordered collection |
| `tuple`    | `(1,2,3)`                | No       | Immutable list |
| `set`      | `{1,2,3}`                | Yes      | Unordered, unique |
| `dict`     | `{"a":1, "b":2}`         | Yes      | Key-value mapping |
| `NoneType` | `None`                   | N/A      | Represents no value |

*(Memory usage varies depending on implementation and object size. Use `sys.getsizeof()` for exact values.)*
