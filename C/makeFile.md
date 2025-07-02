# Makefile in C

## Purpose
- Automate build steps.
- Handles dependencies.
- Reduces repetitive compilation.

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

## make vs cmake
- `make` uses manual Makefile.
- `cmake` generates Makefiles automatically.