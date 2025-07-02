# Binary Tools: objdump, objsize, nm

## objdump
- Disassembles binary object files.
- Shows assembly instructions.
- Example: `objdump -d a.out`.
- Can display headers, symbol tables, relocation entries.

## size / objsize
- Shows size of different sections: text, data, bss.
- Example: `size a.out`
- Useful to optimize code size.

## nm
- Lists symbols from object files.
- Shows which functions and variables are defined or undefined.
- Example: `nm a.out` → see which symbols are linked.