# 🐍 Programming Concepts — Python (Sessions 6–17)
**Duration:** 24 Theory Hours + 26 Lab Hours  
**Module:** Programming Concepts (PG-DITISS August 2025)  
**Objective:**  
To build core Python programming skills required for automation, scripting, data handling, exploit development, socket programming, and working within Linux environments.

---

# 🧩 Session-wise Breakdown

---

## 🧠 **Session 06: Python Basics**
- [ ] Installing Python (Windows / Linux)  
- [ ] Your First Python Program  
- [ ] Declaring Functions  
- [ ] Overview of Objects  
- [ ] Indentation Rules  
- [ ] Native Data Types  

### 🧪 Lab Assignment
- [ ] Install Python in **Windows** and **Linux**  
- [ ] Write programs using Python **data types**  
- [ ] Print “Hello World”  
- [ ] Create & run a Python **script file**  
- [ ] Accept **user input** and print output  
- [ ] Use **for/while loops**  
- [ ] Implement **if-else** conditions  

---

## 🧠 **Sessions 07 & 08: Dictionaries and Lists**
### Dictionaries
- [ ] Introducing Dictionaries  
- [ ] Defining Dictionaries  
- [ ] Modifying Dictionaries  
- [ ] Deleting Dictionary Items  

### Lists
- [ ] Introducing Lists  
- [ ] Defining Lists  
- [ ] Adding Elements  
- [ ] Searching Lists  
- [ ] Deleting List Elements  
- [ ] List Operators  

### 🧪 Lab Assignment
- [ ] Create & print a dictionary  
- [ ] Use loops (for/while)  
- [ ] Insert/Delete entries in dictionary  

---

## 🧠 **Session 09: Tuples, Variables, Sets**
- [ ] Introducing Tuples  
- [ ] Declaring Variables  
- [ ] Referencing Variables  
- [ ] Assigning Multiple Values  
- [ ] Joining Lists & Splitting Strings  
- [ ] Introduction to Sets  

### 🧪 Lab Assignment
- [ ] Create & print a tuple  
- [ ] Use loops  
- [ ] Insert/Delete tuple items (conceptually—immutable)  

---

## 🧠 **Session 10: Built-ins, Objects & Sockets**
- [ ] Optional & Named Arguments  
- [ ] Built-in functions: `type`, `str`, `dir`, etc.  
- [ ] Object References  
- [ ] Python Sockets  

### 🧪 Lab Assignment
- [ ] Append/Insert/Extend/Remove/Sort/Reverse a list  
- [ ] Perform same operations on **strings**  
- [ ] Use built-in functions (`dir`, `type`, `len`, etc.)  

---

## 🧠 **Session 11: Regex & Scripting**
- [ ] Regular Expressions  
- [ ] Python Scripting  
- [ ] Functions & Functional Programming  

### 🧪 Lab Assignment
Using **regex**, match:
- [ ] Any single character except newline  
- [ ] A word  
- [ ] A whitespace character  
- [ ] Any non-whitespace character  
- [ ] Search for patterns in input text  

---

## 🧠 **Session 12 (2T + 4L): OOP & Linux Environment**
- [ ] Object-Oriented Linux Environment  
- [ ] Classes & Objects  
- [ ] OOPS Concepts: Inheritance, Encapsulation, Polymorphism  

### 🧪 Lab Assignment
- [ ] Memory management practice  
- [ ] Find **current directory**  
- [ ] List **all folders & files** in a directory  
- [ ] Get **absolute & relative paths**  
- [ ] Check if a file/folder exists  
- [ ] Create / Remove a directory  
- [ ] Check file permissions  

---

## 🧠 **Sessions 13 & 14: File Handling, Directories & Sockets**
- [ ] File Handling  
- [ ] Directory Permissions  
- [ ] Control Sockets  

### 🧪 Lab Assignment
- [ ] Read & write files using Python  
- [ ] Print complete file contents  
- [ ] Count lines  
- [ ] Count words  
- [ ] Read **web page content** using Python  

---

## 🧠 **Session 15: Libraries, Servers & Client Scripting**
- [ ] Libraries: `hashlib`, `shodan`, `datetime`  
- [ ] Server & Client Architecture  
- [ ] Web Servers & Client Scripts  

### 🧪 Lab Assignment
- [ ] Create a socket between **server and client**  
- [ ] Analyze & monitor client activities  

---

## 🧠 **Session 16: Exploit Development & Plugins**
- [ ] Exploit Development Techniques  
- [ ] Writing Python Plugins  

### 🧪 Lab Assignment
- [ ] Create a simple exploit using **socket programming**  

---

## 🧠 **Session 17: Exploit Automation & Debugging**
- [ ] Exploit Analysis Automation  
- [ ] Debugging Basics  

### 🧪 Lab Assignment
- Perform debugging tasks on Python scripts and exploit PoCs  

---

# 🧰 Tools & Platforms
| Category | Tools |
|---------|--------|
| Python Environment | Python 3, pip, venv |
| Editors | VS Code, PyCharm, Vim |
| Networking | netcat, Wireshark, Python sockets |
| Regex Testing | regex101, Python `re` module |
| Linux Commands | ls, pwd, chmod, chown, mkdir |
| Exploit/Debug | gdb, pwntools (optional), socket |
| Web Data | urllib, requests |

---

# 🎯 Learning Outcomes
By the end of this module, you will be able to:
- ✅ Write Python scripts for automation and DevOps tasks  
- ✅ Use data structures: lists, dicts, tuples, sets  
- ✅ Work with files, directories, and system information  
- ✅ Perform socket programming for client-server communication  
- ✅ Understand OOP and apply it in real projects  
- ✅ Use regular expressions for searching and parsing  
- ✅ Build small exploit PoCs and automate analysis  
- ✅ Debug Python applications  

---

# ✍️ Personal Notes
> Add your own examples, commands, and error fixes here.

```python
# Example socket snippet
import socket
s = socket.socket()
s.connect(("127.0.0.1", 8080))
print(s.recv(1024))
