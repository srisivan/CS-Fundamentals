# Linking in C/C++

## 1. What is the Function of a Linker?
A **linker** is a program that combines object files (`.o` or `.obj`) and libraries into a single executable file.  
Its main functions are:
- **Symbol resolution**: Matches function calls with their definitions.  
- **Address binding**: Assigns memory addresses to functions and variables.  
- **Library linking**: Links standard libraries (e.g., libc, libstdc++).

### Example Compilation Process:
```bash
gcc -c main.c   # Compiles to main.o
gcc -c utils.c  # Compiles to utils.o
gcc main.o utils.o -o app   # Linker combines into app executable
```

---

## 2. What is Static Linking?
- In **static linking**, all library code used by a program is copied into the executable at compile time.  
- The resulting executable is **self-contained** and does not need external libraries at runtime.

### Example:
```bash
gcc main.c -static -o app
```
This creates a fully statically linked binary.

**Advantages:**
- No dependency on external libraries at runtime.  
- Easier deployment (single executable).  

**Disadvantages:**
- Larger executable size.  
- Must rebuild to update libraries.  

---

## 3. What is Dynamic Linking?
- In **dynamic linking**, external libraries are not copied into the executable.  
- Instead, references are stored, and the required libraries are loaded at runtime.  

### Example:
```bash
gcc main.c -o app   # Default uses dynamic linking with libc.so
```
Here, the executable depends on system libraries.

**Advantages:**
- Smaller executable size.  
- Library updates automatically benefit all programs.  

**Disadvantages:**
- Requires correct version of libraries at runtime.  
- Programs may break if library compatibility changes.  

---

## 4. Which is Better?
- **Static Linking** → Better for portability (single binary, no external dependencies).  
- **Dynamic Linking** → Better for efficiency (smaller size, shared libraries).  

### When to Use:
- Use **static linking** for embedded systems, portable software, or when dependency issues are critical.  
- Use **dynamic linking** for desktop/server applications where saving memory and updating libraries easily is important.  

---

# Summary
- **Linker**: Combines object files and libraries into an executable.  
- **Static Linking**: Copies libraries into the executable → larger but portable.  
- **Dynamic Linking**: Uses shared libraries at runtime → smaller but dependent on system libraries.  


---

## 📊 Static vs Dynamic Linking (Comparison Table)

| Feature              | Static Linking 🚀                      | Dynamic Linking 🔗                   |
|----------------------|----------------------------------------|---------------------------------------|
| **Executable Size**  | Large (library code included)          | Small (only references stored)        |
| **Dependencies**     | None (self-contained)                  | Requires external shared libraries    |
| **Performance**      | Faster startup (no runtime linking)    | Slightly slower (library loaded at runtime) |
| **Memory Usage**     | Higher (duplicate code in each program)| Lower (shared libraries in memory)    |
| **Updates**          | Requires recompilation for updates     | Libraries can be updated separately   |
| **Portability**      | Highly portable (single binary)        | Less portable (needs correct libraries) |
| **Best For**         | Embedded systems, standalone programs  | Desktop/server apps, frequent updates |
