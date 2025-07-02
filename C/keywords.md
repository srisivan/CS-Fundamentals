# C Keywords: volatile, extern, register

- `volatile` → variable can change unexpectedly.
- `extern` → declare a global defined elsewhere.
- `register` → suggest storing in CPU register.

# Keywords: volatile, extern, register

## volatile
- Tells compiler variable may change unexpectedly.
- Prevents unwanted optimization.
- Example: hardware registers.

## extern
- Declare variable or function defined in another file.
- Used in multi-file projects.

## register
- Suggests storing variable in CPU register for faster access.
- Modern compilers often ignore it.