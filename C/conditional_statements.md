# Conditional Statements in C

## Purpose
Control flow based on conditions.

## Statements
- `if`: Checks condition.
- `else if`: Checks additional conditions.
- `else`: Executes when no prior condition is true.
- `switch`: Multi-way branch for discrete values.

## Syntax
```c
if (x > 0) {
  // Positive
} else if (x == 0) {
  // Zero
} else {
  // Negative
}

switch (x) {
  case 1:
    break;
  default:
    break;
}
```

## Best Practices
- Use braces `{}` even for single-line blocks.
- Prefer `switch` for fixed options.