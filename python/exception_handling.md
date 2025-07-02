# Exception Handling in Python

## Why?
- Handle runtime errors gracefully.

## Syntax
```python
try:
    risky()
except Exception as e:
    print(e)
else:
    print("No error")
finally:
    print("Always runs")
```

## Raise
- Manually throw error.
```python
raise ValueError("Invalid input")
```