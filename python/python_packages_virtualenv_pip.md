# Python Package Management

## 1. Python Packages
- A **package** is a way of organizing related Python modules into a single directory hierarchy.
- A package is simply a directory containing a special `__init__.py` file.

**Example: Creating a package**
```
mypackage/
    __init__.py
    module1.py
    module2.py
```
Usage:
```python
from mypackage import module1
module1.my_function()
```

---

## 2. Python Virtual Environments
- A **virtual environment** is an isolated environment for Python projects.
- Each environment has its own **Python interpreter** and libraries, so different projects can have different dependencies.

**Example:**
```bash
# Create a virtual environment
python -m venv myenv

# Activate (Linux/Mac)
source myenv/bin/activate

# Activate (Windows)
myenv\Scripts\activate

# Deactivate
deactivate
```

---

## 3. pip
- **pip** is the package installer for Python.
- Used to install, upgrade, and remove Python packages.

**Example:**
```bash
# Install a package
pip install requests

# Install specific version
pip install requests==2.28.0

# Upgrade a package
pip install --upgrade requests

# Uninstall a package
pip uninstall requests

# List installed packages
pip list
```
