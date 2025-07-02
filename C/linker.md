# Linker in C

## What is a Linker?
- Combines multiple object files into a single executable.
- Resolves external symbols and addresses.

## How it works
1. Reads object files.
2. Matches function and variable references.
3. Puts code/data in final memory layout.
4. Creates final executable.

## Static Linking
- Libraries copied into executable.
- No dependency at runtime.

## Dynamic Linking
- Links to shared libraries at runtime.
- Smaller executables.
- Uses `.so` files on Linux.