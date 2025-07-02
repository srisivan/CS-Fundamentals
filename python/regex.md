# Regular Expressions in Python

## What is Regex?
- Used for searching, matching, pattern recognition.

## Module
- `import re`

## Common Methods
- `re.match()`
- `re.search()`
- `re.findall()`
- `re.sub()`

## Example
```python
import re
pattern = r"\d+"
result = re.findall(pattern, "There are 2 apples and 5 oranges")
print(result)
```