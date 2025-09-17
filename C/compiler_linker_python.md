# Compiler and Linker in Python

## 1. What is a Compiler in Python?
Python is primarily an **interpreted language**, but it still compiles code into **bytecode** before execution.  
- Python source (`.py`) → Bytecode (`.pyc`).  
- Done automatically by the Python interpreter.  

### Example:
```bash
python -m py_compile script.py   # Produces __pycache__/script.cpython-XYZ.pyc
```

---

## 2. What is a Linker in Python?
- Python does **not** use a traditional linker like C/C++.  
- Instead, it uses an **import system** to link modules and packages dynamically at runtime.  

### Example:
```python
import math   # Python dynamically links math module at runtime
print(math.sqrt(16))
```

---

## 3. Difference Between Compiler and Linker in Python

| Feature              | Compiler (Python)                           | Linker (Python)                                |
|----------------------|----------------------------------------------|------------------------------------------------|
| **Function**         | Converts `.py` to bytecode `.pyc`            | Dynamically loads modules at runtime            |
| **Input**            | Python source code                          | Bytecode + Python modules                       |
| **Output**           | Bytecode (`.pyc`)                           | Executed program with imported modules          |
| **Error Types**      | Syntax errors during compilation             | Import errors at runtime                        |
| **Stage**            | Before execution                            | During execution                                |

---
