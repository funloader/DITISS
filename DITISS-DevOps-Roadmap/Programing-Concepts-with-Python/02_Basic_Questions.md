## ❓ Q11. Find working of various functions (min 7) from math library of python which is provided as standard library. 
``https://docs.python.org/3/library/math.html`` You can also try it yourself.

Ex. 
```python
import math
print(math.factorial(4))
print(math.sin(90))
```
### 1️⃣ math.sqrt() — Square Root
```
import math
print(math.sqrt(25))   # Output: 5.0

```
### 2️⃣ math.pow() — Exponentiation
```
print(math.pow(2, 5))   # Output: 32.0

```
### 3️⃣ math.factorial() — Factorial of a number
```
print(math.factorial(6))    # Output: 720

```
### 4️⃣ math.sin() / math.cos() / math.tan()
(These use radians, not degrees)
```
print(math.sin(math.radians(90)))   # 1.0
print(math.cos(math.radians(0)))    # 1.0
print(math.tan(math.radians(45)))   # 1.0

```
### 5️⃣ math.log() — Natural logarithm (base e)
```
print(math.log(10))      # 2.302585...
print(math.log(100, 10)) # base-10 log → 2
```
### 6️⃣ math.ceil() — Round up
```
print(math.ceil(4.2))   # Output: 5
```
### 7️⃣ math.floor() — Round down
```
print(math.floor(4.8))   # Output: 4
```
### 🧪 Bonus: math.pi & math.e
```
print(math.pi)   # 3.141592653589793
print(math.e)    # 2.718281828459045
```

### ❓ Q12. Open VSCode IDE and create a python program (.py file) to print Hello world!. Run the program and check the put on console.
---

## ✅ Step-by-Step Solution

### **1️⃣ Open VS Code**
- Launch **Visual Studio Code**  
- Make sure the **Python extension** is installed  
  - Go to `Extensions` → Search **Python** → Install (Microsoft)

---

### **2️⃣ Create a Python File**
1. Create a new folder → open it in VS Code  
2. Create a new file → hello.py

---

### **3️⃣ Write the Program**
Inside `hello.py`, type:

```python
print("Hello World!")
```

### **4️⃣ Run the Program**
▶️ Method 1 — Using VS Code Run Button
- Click Run > Run Without Debugging
OR 
- Click the Run ▶️ icon in the top right

### **▶️ Method 2 — Using Terminal**
- Open VS Code terminal: Terminal → New Terminal
- Then run: ``python hello.py``
🎯 Expected Output ``Hello World!``

# 🧮 Q13 — Write a Program in VSCode to Compute GCD and LCM Using Python `math` Library

**Task:**  
Write a Python program using **VSCode IDE** that:  
- Imports the **math** library  
- Takes **two numbers** as input  
- Prints their **GCD** (Greatest Common Divisor)  
- Prints their **LCM** (Least Common Multiple)

---

## ✅ Python Program (Solution)

```python
# Q13 Solution — GCD and LCM using math library

import math

# Taking input from user
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

# Calculating gcd
gcd_value = math.gcd(num1, num2)

# Calculating lcm
lcm_value = abs(num1 * num2) // gcd_value

# Printing the results
print(f"GCD of {num1} and {num2} is: {gcd_value}")
print(f"LCM of {num1} and {num2} is: {lcm_value}")
```
### **📝 How to Run in VSCode**

- Open VSCode
- Create a new file → gcd_lcm.py
- Paste the above code
- Open terminal → run: ``python gcd_lcm.py``
- Enter two numbers when prompted
- View the output in the terminal
