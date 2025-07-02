# Preprocessing in C

## Preprocessor Directives
- `#define`: Macros/constants.
- `#include`: Add header files.
- `#if`, `#elif`, `#else`: Conditional compilation.
- `#error`: Trigger compilation error intentionally.

## Example
```c
#define PI 3.14
#define SQUARE(x) ((x)*(x))
#include <stdio.h>

#if PI < 4
#error "PI is too small!"
#endif
```