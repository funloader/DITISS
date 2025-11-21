# 📝 Basic Questions — Python & Computer Fundamentals

These questions help build foundational understanding before diving into Python programming and system concepts.

---

## ❓ Q1. What are the components of a computer?
A computer is made up of:
- **Input Devices** – keyboard, mouse, scanner  
- **Output Devices** – monitor, printer  
- **CPU (Central Processing Unit)** – ALU + CU  
- **Memory** – RAM, ROM  
- **Storage** – HDD, SSD  
- **Motherboard**  
- **Power Supply Unit (PSU)**  

---

## ❓ Q2. Which CPU are you using in your laptop / mobile / PC?
Answer varies by user.  
Examples:
- Laptop → Intel i5/i7, AMD Ryzen  
- Mobile → Qualcomm Snapdragon, Apple A-Series, MediaTek  
- PC → Intel Core, AMD Ryzen  

> You can check using:  
> **Windows:** Task Manager → Performance  
> **Linux:** `lscpu`  
> **Android:** CPU-Z app  
> **iOS:** Device model (e.g., A15 Bionic)

---

## ❓ Q3. What is the size of RAM in your PC?
Typical values:
- **8 GB** (common)  
- **16 GB** (recommended)  
- **32 GB+** (for dev, gaming, virtualization)

To find:
- Windows: Task Manager → Performance  
- Linux: `free -h`  

---

## ❓ Q4. Read Python documentation  
🔗 https://docs.python.org/3/tutorial/index.html

This is the official Python tutorial — covers basics to advanced concepts.

---

## ❓ Q5. What are different implementations of Python? Which implementation are we using?

### 🔧 Popular Python Implementations
| Implementation | Description |
|----------------|-------------|
| **CPython** | Standard & most widely used implementation (written in C) |
| **PyPy** | Fast JIT-compiled implementation |
| **Jython** | Python running on JVM |
| **IronPython** | Python for .NET |
| **MicroPython** | For microcontrollers |

➡️ **Most users (including DITISS labs) use _CPython_**, the default one you get from python.org.

---

## ❓ Q6. Who created Python? In which year? Where?

- **Creator:** *Guido van Rossum*  
- **Year Started:** *1989 (Christmas holidays)*  
- **First Release:** *1991*  
- **Where:** *Centrum Wiskunde & Informatica (CWI), Netherlands*

---

## ❓ Q7. What is PVM?

**PVM = Python Virtual Machine**  
- The runtime engine that executes Python bytecode (`.pyc`).  
- Part of the CPython interpreter.  
- Reads bytecode → converts to machine instructions.  

It’s what makes Python an *interpreted* language.

---

## ❓ Q8. Is Python platform-independent? Which platforms can Python run on?

✅ **Yes — Python is platform independent.**  
It can run on:
- Windows  
- Linux  
- macOS  
- Unix  
- Android (with Termux)  
- iOS (limited)  
- Embedded devices (MicroPython)

---

## ❓ Q9. Why is Python platform independent? What makes it platform independent?

Python code → converted to **bytecode** → executed by **PVM**.  
Because PVMs exist for multiple OS platforms, the **same .py code runs everywhere**.

### ✔️ Platform independence =  
**Write Once → Run Anywhere (as long as PVM exists for that OS)**

---

## ❓ Q10.  
### **WAP to Print "Hello IACSD" and write a comment describing the author and date created**

**Example:**
```python
# Author: <Your Name>
# Date: <DD-MM-YYYY>
# Purpose: Basic print program

print("Hello IACSD")

```
