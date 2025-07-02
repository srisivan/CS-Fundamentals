```markdown
# Makefile in C

## Purpose
Automates compilation: dependencies & rules.

## Tools
- `make` reads Makefile instructions.
- `cmake` generates Makefiles or other build systems.

## Example
```makefile
all: main.o utils.o
\tgcc -o app main.o utils.o

main.o: main.c
\tgcc -c main.c

utils.o: utils.c
\tgcc -c utils.c

clean:
\trm *.o app
```