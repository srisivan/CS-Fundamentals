# Build Systems in C/C++

## 1. What is the use of a Makefile?
A **Makefile** is a special file used by the `make` build automation tool to:
- Compile and link programs automatically.
- Specify how source files depend on each other.
- Rebuild only the parts of the code that changed.

### Example Makefile:
```makefile
# Simple Makefile

app: main.o utils.o
	gcc -o app main.o utils.o

main.o: main.c
	gcc -c main.c

utils.o: utils.c
	gcc -c utils.c

clean:
	rm -f *.o app
```
🔹 Running `make` will build the program, and `make clean` removes generated files.

---

## 2. What is `make`?
- `make` is a **build automation tool**.  
- It reads instructions from a `Makefile`.  
- It checks file dependencies and only recompiles modified files.

### Example:
```bash
make        # Builds target as per Makefile
make clean  # Cleans build files
```

---

## 3. What is `cmake`?
- `cmake` is a **cross-platform build system generator**.  
- It generates platform-specific build files (e.g., Makefiles, Visual Studio projects).  
- It is more flexible and modern compared to `make`.

### Example:
```bash
cmake .        # Generates Makefile
make           # Builds project using generated Makefile
```

`CMakeLists.txt` example:
```cmake
cmake_minimum_required(VERSION 3.10)
project(MyApp)

add_executable(app main.c utils.c)
```

---

## 4. Different Methods to Build Object Files

### (a) Manual Compilation
```bash
gcc -c main.c
gcc -c utils.c
gcc main.o utils.o -o app
```

### (b) Using Makefile (with `make`)
```bash
make        # Builds based on Makefile rules
```

### (c) Using CMake
```bash
cmake .
make
```

### (d) Other Build Systems
- **Ninja** → Fast build system often used with CMake.  
- **Meson** → High-level build system that generates Ninja files.  
- **Autotools** → Traditional build system for Unix/Linux.  

---

# Summary
- **Makefile** → Script that defines how to build a project.  
- **make** → Tool that executes the Makefile.  
- **cmake** → Cross-platform build system generator.  
- **Object files** can be built manually, with `make`, `cmake`, or other build systems.
