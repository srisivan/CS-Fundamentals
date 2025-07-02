```markdown
# Regex in Python

## Module
`import re`

## Functions
- `re.match()`: checks for match at beginning.
- `re.search()`: searches anywhere.
- `re.findall()`: all matches.

## Example
```python
import re
pattern = r"[a-z]+"
text = "Hello123"
result = re.findall(pattern, text)
print(result)
```
```