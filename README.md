# PyPI_IID

**IID**, short for **Index Integer Date**, is a 4/8/12/16-byte format designed for seamless communication across various network systems, including UDP, WebSocket, and Mirror.

By standardizing the code and API to work exclusively with integer values:
- It enables the creation of action index tables.
- It supports the development of specialized tools for specific tasks, allowing IID to facilitate remote actions effectively.

The **IID format** was developed to streamline QA testing across multiple devices and computers with precise timing coordination.

### Key Features of IID:
1. **Index on your own server**: Identifies the target device.
2. **Index on a shared server**: Identifies the user.
3. **Value**: Represents the transported integer value.
4. **Date**: Encoded in a specific `ulong` format:
   - **01.....TICK**: Sent using NTP time.
   - **02.....TICK**: Intended for execution at a designated NTP time.
   - **.......TICK**: Sent from an unknown source time but uses `DateTime.Now` in UTC since 1970.

If you need assistance or are interested in contributing to this project, feel free to reach out.  
Since 2024, all my tools have been built around this principle.

---

```
/*
 * ----------------------------------------------------------------------------
 * "PIZZA LICENSE":
 * https://github.com/EloiStree wrote this file.
 * As long as you retain this notice, you
 * can do whatever you want with this code.
 * If you think my code saved you time,
 * consider sending me a 🍺 or a 🍕 at:
 *  - https://buymeacoffee.com/apintio
 * 
 * You can also support my work by building your own DIY input device
 * using these Amazon links:
 * - https://github.com/EloiStree/HelloInput
 *
 * May the code be with you.
 *
 * Updated version: https://github.com/EloiStree/License
 * ----------------------------------------------------------------------------
 */
```

--------------------


--------------------


## Creating a Python Package

Tutorial:
- https://youtu.be/9Ii34WheBOA?t=457


This is my first Python package. Here’s how to build one.

### Steps to Create a Pip Package:

1. Install or upgrade the build tool:  
   ```bash
   pip install --upgrade build
   ```

2. Navigate to your project’s root directory:  
   ```bash
   cd "GIT_PROJECT_ROOT"
   ```

3. Build the package:  
   ```bash
   python -m build
   ```

4. A `.whl` file will be created. You can install it using pip:  
   ```bash
   pip install iid-2025.1.8-py3-none-any.whl
   ```

### Example Workflow:

```bash
pip uninstall iid -y
python -m build
pip install dist/iid-2025.1.8-py3-none-any.whl
python
```

### Example Usage:

```python
import iid
iid.say_hello()
```


