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

## ❓ Q12. Open VSCode IDE and create a python program (.py file) to print Hello world!. Run the program and check the put on console.
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

## 🧮 Q13 — Write a Program in VSCode to Compute GCD and LCM Using Python `math` Library

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

## 🧮 Q14. WAP using VSCode IDE. Use math library. Print number of options you have, when you are given 5 different characters and you need to select 3 of them without repeatitions. (find permutations)

**Task:**  
Write a Python program (WAP) using VSCode IDE.
- Use the math library to print the number of options (permutations) when you are given 5 different characters and need to select 3 of them without repetitions.

- Formula used:
- Permutations (P(n, r)) = nPr = n! / (n−r)!

- For n = 5, r = 3:
- 5P3 = 5! / 2! = 60

---

## ✅ Python Code (using math library)

```python
import math

n = 5
r = 3

# Using the permutations function directly
options = math.perm(n, r)

print("Number of options (permutations):", options)

```


## 🧮 Q15. WAP using VSCode IDE. Use math library. Print number of options you have to select 20 students out of 60 without repeatitions. ( Obviously here order doesn't matter, so find combinations) 

**Task:**
Write a Python program (WAP) using VSCode IDE.
- Use the math library to print the number of options (combinations) when selecting 20 students out of 60, without repetitions and order does not matter.

- Formula used:
- Combinations (C(n, r)) = nCr = n! / (r! × (n − r)!)

---

## ✅ Python Code (using math library)

```python
import math

n = 60
r = 20

# Using the combinations function directly
options = math.comb(n, r)

print("Number of options (combinations):", options)
```

## 🧮 Q16. WAP using VSCode IDE. Use math library. Try to find log of zero. Which error is given ? 
Also try to find square root of any negative number. What error is give?

**Task:**
- What happens when you try to find log of zero?
- What happens when you try to find square root of any negative number?

---
## ✅ Python Code (using math library)

```python
import math

# 1. Trying log of zero
try:
    print(math.log(0))
except Exception as e:
    print("Error when finding log(0):", e)

# 2. Trying square root of a negative number
try:
    print(math.sqrt(-25))
except Exception as e:
    print("Error when finding sqrt(-25):", e)
```
### **✔️ Explanation of Errors**
### 1️⃣ math.log(0)
- Error: ``ValueError: math domain error``
- Reason: Logarithm of zero is undefined (approaches negative infinity).

### 2️⃣ math.sqrt(-25)
- Error: ``ValueError: math domain error``
- Reason: Square root of a negative number is not defined in real numbers;
``math`` module only works with REAL math.

## 🧮 Q17. WAP to create a variable v1 and store any number. Find the square root of that number by using v1 in math.sqrt() function.

**Task:**
Write a Python program (WAP) using VSCode IDE.
- Create a variable ``v1``, store any number in it, and find the square root of that number using ``math.sqrt()``.

---
## ✅ Python Code (using math library)

```python
import math

v1 = 144   # you can store any number here
result = math.sqrt(v1)

print("Square root of", v1, "is:", result)
```

## 🧮 18. Why python is considered as slow compared to C, C++ ?

**Python is slower mainly because:**    [![Refer](https://img.shields.io/badge/StackOverflow-Reference-blue)](https://stackoverflow.com/questions/3033329/why-are-python-programs-often-slower-than-the-equivalent-program-written-in-c-or)

- Interpreted language – Python runs through an interpreter, while C/C++ code is compiled directly to machine code.
- Dynamic typing – Python checks data types at runtime, adding overhead.
- Objects for everything – Even simple numbers are stored as heavy objects, not raw values.
- Garbage collection – Python manages memory automatically, which slows execution.
- Less optimization – C/C++ compilers perform strong optimizations; Python cannot optimize at that level.
Conclusion:
- Python prioritizes ease and flexibility over raw speed, while C/C++ prioritize performance.


## 🧮 Q19. Check where .pyc files are stored after you run the program for Q15. 

When you run your Python program (including the code from Q15), Python automatically compiles it to bytecode and stores the  ``.pyc`` file in a folder named: ``__pycache__
``

## ✔️ Exact Location
Inside the same directory where your ``.py`` file is stored, you will find:
```
__pycache__/
    yourfilename.cpython-311.pyc   (version number may vary)
```
- If the file is: ``Q15.py`` 
- Then after running it, Python will create: ``__pycache__/Q15.cpython-311.pyc
``
## ✔️ Why this happens?
``.pyc`` files contain compiled bytecode, which makes future program runs faster.
