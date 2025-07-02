# Object File Format

## Sections
- `.text`: Machine code.
- `.data`: Initialized data.
- `.bss`: Uninitialized data.
- `.rodata`: Read-only literals.
- `.symtab`: Symbol table.
- `.strtab`: String table.

## Purpose
- Organizes code & data.
- Used by linker to create executables.
- Keeps symbols for debugging.

## Tools
- Inspect with `objdump`, `readelf`, `nm`.