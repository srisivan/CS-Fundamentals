# Python Data Structures and Regex

## 1. List
- A **list** is a built-in data structure in Python that stores an ordered collection of items.
- Lists are **mutable** (can be changed after creation).

**Example:**
```python
# Creating a list
fruits = ["apple", "banana", "cherry"]

# Adding elements
fruits.append("orange")

# Accessing elements
print(fruits[0])  # Output: apple

# Iterating
for fruit in fruits:
    print(fruit)
```

---

## 2. Dictionary
- A **dictionary** is a collection of key-value pairs.
- Keys are unique and immutable; values can be of any type.
- Often used to store mappings.

**Example:**
```python
# Creating a dictionary
student = {"name": "Alice", "age": 21, "course": "CS"}

# Accessing values
print(student["name"])  # Output: Alice

# Adding new key-value
student["grade"] = "A"

# Iterating through keys and values
for key, value in student.items():
    print(key, ":", value)
```

---

## 3. Regex (Regular Expressions)
- The **re** module in Python allows us to work with **regular expressions**.
- Regex is used for pattern matching and text manipulation.

**Example:**
```python
import re

# Match a pattern
pattern = r"\d+"  # one or more digits
text = "My number is 12345"

matches = re.findall(pattern, text)
print(matches)  # Output: ['12345']

# Validate an email
email = "test@example.com"
if re.match(r"[^@]+@[^@]+\.[^@]+", email):
    print("Valid email")
else:
    print("Invalid email")
```
