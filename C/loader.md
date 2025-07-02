# Loader in C

## What is a Loader?
- OS component that loads executable into memory.
- Allocates memory space.
- Resolves addresses for dynamic linking.
- Starts execution at `main()`.

## Steps
1. Read executable headers.
2. Allocate virtual memory.
3. Map sections (text, data, bss).
4. Pass control to entry point.