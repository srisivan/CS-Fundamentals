```markdown
# Exception Handling in Python

## Syntax
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero.")
finally:
    print("Cleanup done.")
```

## raise
Manually raise an exception:
```python
raise ValueError("Invalid value")
```
```