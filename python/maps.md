# map() in Python

## What is map()?
- Applies a function to each item of an iterable.
- Returns a map object (iterator).

## Example
```python
nums = [1, 2, 3]
squared = map(lambda x: x*x, nums)
print(list(squared))
```