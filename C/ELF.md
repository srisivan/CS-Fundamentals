# ELF (Executable and Linkable Format)

The ELF format is the standard binary file format for executables, object code, shared libraries, and core dumps in Unix-like operating systems.

## Purpose
- Defines how code and data are organized.
- Enables linking and loading on different systems.

## Main Parts
- **Header:** Identifies file type (relocatable, executable, shared object, core dump).
- **Program Header Table:** Describes segments for the loader (used at runtime).
- **Section Header Table:** Describes sections for the linker (used at compile/link time).

## Common Sections
- **.text:** Executable machine instructions.
- **.data:** Initialized global/static variables.
- **.bss:** Uninitialized global/static variables.
- **.rodata:** Read-only data (string literals).
- **.symtab:** Symbol table.
- **.strtab:** String table for symbol names.
- **.rel.text / .rela.text:** Relocation info for `.text`.

## Tools
- `readelf`: Display ELF headers and sections.
- `objdump`: Disassemble ELF binaries.
- `nm`: Inspect symbols.

## Example
Run `readelf -h your_program` to see the ELF header.