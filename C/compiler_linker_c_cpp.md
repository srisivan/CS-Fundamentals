# Compiler and Linker in C/C++

## 1. What is a Compiler?
A **compiler** translates source code (written in C/C++) into **object code** (machine-readable instructions).  
It performs:
- Syntax checking  
- Semantic analysis  
- Optimization  
- Code generation  

### Example in C:
```bash
gcc -c main.c   # Produces main.o (object file)
```

---

## 2. What is a Linker?
A **linker** combines object files and libraries into an executable.  
It resolves function calls, assigns memory addresses, and links external libraries.

### Example:
```bash
gcc main.o utils.o -o app
```

---

## 3. Difference Between Compiler and Linker

| Feature              | Compiler (C/C++)                             | Linker (C/C++)                                  |
|----------------------|-----------------------------------------------|------------------------------------------------|
| **Function**         | Converts source code into object code         | Combines object files into executable           |
| **Input**            | Source files (`.c`, `.cpp`)                   | Object files (`.o`, `.obj`) and libraries       |
| **Output**           | Object file                                   | Executable file                                 |
| **Error Types**      | Syntax & semantic errors                      | Linking errors (undefined references)           |
| **Stage**            | Compilation stage                            | Linking stage                                   |

---
