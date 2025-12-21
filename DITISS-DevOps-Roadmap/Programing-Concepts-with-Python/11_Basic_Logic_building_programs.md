Here is a **simple and beginner-friendly Python program** for your question 👇
---
### 🧮 Simple Calculator Program

✅ Beginner-friendly, logic-building, menu-driven program
```
print("----- Simple Calculator -----")
print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

choice = int(input("Enter your choice (1-4): "))

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

if choice == 1:
    print("Result =", num1 + num2)
elif choice == 2:
    print("Result =", num1 - num2)
elif choice == 3:
    print("Result =", num1 * num2)
elif choice == 4:
    if num2 == 0:
        print("Error: Division by zero not allowed!")
    else:
        print("Result =", num1 / num2)
else:
    print("Invalid Choice!")

```
### 🔬 Scientific Calculator program


```
import math

print("----- Scientific Calculator -----")
print("1. Square Root")
print("2. Power (x^y)")
print("3. Factorial")
print("4. Sine")
print("5. Cosine")
print("6. Tangent")
print("7. Log (base e)")
print("8. Exponential (e^x)")

choice = int(input("Enter your choice (1-8): "))

if choice == 1:
    x = float(input("Enter number: "))
    print("Result =", math.sqrt(x))

elif choice == 2:
    x = float(input("Enter base: "))
    y = float(input("Enter power: "))
    print("Result =", math.pow(x, y))

elif choice == 3:
    x = int(input("Enter integer: "))
    print("Result =", math.factorial(x))

elif choice == 4:
    x = float(input("Enter angle (in degrees): "))
    print("Result =", math.sin(math.radians(x)))

elif choice == 5:
    x = float(input("Enter angle (in degrees): "))
    print("Result =", math.cos(math.radians(x)))

elif choice == 6:
    x = float(input("Enter angle (in degrees): "))
    print("Result =", math.tan(math.radians(x)))

elif choice == 7:
    x = float(input("Enter number: "))
    print("Result =", math.log(x))

elif choice == 8:
    x = float(input("Enter number: "))
    print("Result =", math.exp(x))

else:
    print("Invalid Choice!")

```
### 🐍 WAP to print the odd numbers from 1 to 99. Prints one number per line.

✅ **Program 1 —** *Using for loop*
```
for i in range(1, 100):
    if i % 2 != 0:
        print(i)
```
✅ **Program 2 —** *Using if condition*
```
for i in range(1, 100):
    if i % 2 != 0:
        print(i)
```
✅ **Program 3 —** *Using while loop*
```
i = 1
while i < 100:
    print(i)
    i += 2
```

### 🐍 WAP to accept a number and check whether it is even or odd

👉 Prints **1** if the number is even
👉 Prints **0** if the number is odd

```
num = int(input("Enter a number: "))

if num % 2 == 0:
    print(1)
else:
    print(0)
```

### ✅ Explanation:

* `%` (modulus) gives the remainder
* Even number → remainder is `0`
* Odd number → remainder is `1`

### 🔹 Example Output:

```
Enter a number: 8
1
```

```
Enter a number: 7
0
```
### 🐍 WAP to print numbers divisible by **3**, **5**, and **both 3 & 5**

```
print("Numbers divisible by 3:")
for i in range(1, 101):
    if i % 3 == 0:
        print(i, end=" ")

print("\n\nNumbers divisible by 5:")
for i in range(1, 101):
    if i % 5 == 0:
        print(i, end=" ")

print("\n\nNumbers divisible by both 3 and 5:")
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print(i, end=" ")
```

---

### ✅ Output Explanation:

* **Divisible by 3** → multiples of 3
* **Divisible by 5** → multiples of 5
* **Divisible by both** → multiples of **15**

---

### 🔹 Sample Output (Partial):

```
Numbers divisible by 3:
3 6 9 12 15 ...

Numbers divisible by 5:
5 10 15 20 ...

Numbers divisible by both 3 and 5:
15 30 45 60 75 90
```

---

### 🐍 WAP to accept three non-negative integers and return **True**

if **two or more** of them have the **same rightmost digit**

```
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

# Get rightmost digits
ra = a % 10
rb = b % 10
rc = c % 10

if ra == rb or rb == rc or ra == rc:
    print(True)
else:
    print(False)
```

---

### ✅ Explanation:

* `number % 10` gives the **rightmost digit**
* Compare all possible pairs:

  * `a & b`
  * `b & c`
  * `a & c`
* If **any two match**, print `True`

---

### 🔹 Example Outputs:

```
Enter first number: 23
Enter second number: 45
Enter third number: 13
True
```

(rightmost digits → 3, 5, 3)

```
Enter first number: 12
Enter second number: 34
Enter third number: 56
False
```

### 🐍 WAP to convert input number of seconds to **HH:MM:SS**

```
seconds = int(input("Enter total seconds: "))

hours = seconds // 3600
seconds = seconds % 3600

minutes = seconds // 60
seconds = seconds % 60

print(f"{hours:02d}:{minutes:02d}:{seconds:02d}")
```

---

### ✅ Explanation:

* **1 hour = 3600 seconds**
* **1 minute = 60 seconds**
* `//` → integer division
* `%` → remainder
* `:02d` → prints two digits (leading zero if needed)

---

### 🔹 Example Output:

```
Enter total seconds: 3661
01:01:01
```

---
### 🐍 WAP to print leap years from 2000 to 2100

```
print("Leap years between 2000 and 2100:")

for year in range(2000, 2101):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        print(year)
```

---

### ✅ Leap Year Conditions Used:

A year is a leap year if:

* **Divisible by 4 AND not divisible by 100**
  **OR**
* **Divisible by 400**

✔ Correct logic
✔ Covers century years (like 2000)
✔ Suitable for exams and beginners

---

### 🔹 Sample Output:

```
2000
2004
2008
2012
2016
...
2096
```

---
Here is a **simple, exam-oriented Python program** to print a **month calendar**, taking
✔ number of days in the month
✔ starting day of the month
as input.

---

### 🗓️ WAP to print calendar for a month

```
days = int(input("Enter number of days in month: "))
start_day = input("Enter starting day of month: ")

week_days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]

# Print day headers
for day in week_days:
    print(day[:3], end="\t")
print()

# Find index of starting day
start_index = week_days.index(start_day)

# Print initial empty spaces
for i in range(start_index):
    print("\t", end="")

# Print dates
for date in range(1, days + 1):
    print(date, end="\t")
    if (date + start_index) % 7 == 0:
        print()
```

---

### 📝 Example Input:

```
Enter number of days in month: 30
Enter starting day of month: Thursday
```

---

### 📅 Output (Day-wise Calendar like June 2022):

```
Sun     Mon     Tue     Wed     Thu     Fri     Sat
                        1       2       3       4
5       6       7       8       9       10      11
12      13      14      15      16      17      18
19      20      21      22      23      24      25
26      27      28      29      30
```

---

### ✅ Explanation:

* Uses a **list of weekdays**
* Finds the **starting day position**
* Prints blank spaces before the 1st date
* Prints dates row-wise (7 days per week)

---

Here is a **simple, logical, exam-ready Python program** to find the **day of a given date**, when the **day of the 1st of that month is known** 👇

---

### 🐍 WAP to print day of an input date

(Given the day of the 1st day of that month)

```
date = int(input("Enter date (day): "))
start_day = input("Enter day of 1st day of month: ")

week_days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]

# Find index of the starting day
start_index = week_days.index(start_day)

# Calculate index of required day
day_index = (start_index + date - 1) % 7

print("Day on given date:", week_days[day_index])
```

---

### 📝 Example Input:

```
Enter date (day): 16
Enter day of 1st day of month: Friday
```

### ✅ Output:

```
Day on given date: Saturday
```

---

### 🔍 Explanation:

* List stores all weekdays in order
* Find the position of the **1st day**
* Add `(date − 1)` to move forward
* Use `% 7` to wrap around the week

---

### ⭐ Exam Tip:

Formula used:

```
(day_of_1st + date - 1) % 7
```

---

## 🧮 1️⃣ Factorial Program using **Recursion**

```
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

num = int(input("Enter a number: "))
print("Factorial =", factorial(num))
```

### ✅ Explanation:

* Function calls itself
* Base condition: `0! = 1` and `1! = 1`
* Recursive relation: `n * factorial(n-1)`

---

## 🔁 2️⃣ Factorial Program using **Loop**

```
num = int(input("Enter a number: "))
fact = 1

for i in range(1, num + 1):
    fact = fact * i

print("Factorial =", fact)
```

### ✅ Explanation:

* Initialize `fact = 1`
* Multiply numbers from `1` to `n`

---

## 🔢 3️⃣ Fibonacci Series Program

```
n = int(input("Enter number of terms: "))

a = 1
b = 1

print("Fibonacci Series:")
for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

### ✅ Explanation:

* First two terms are `1, 1`
* Each next term = sum of previous two

---

### 🔹 Sample Output:

```
Enter number of terms: 8
Fibonacci Series:
1 1 2 3 5 8 13 21
```

---

## ⭐ Exam Notes:

| Program               | Concept Used             |
| --------------------- | ------------------------ |
| Factorial (Recursion) | Function + Base Case     |
| Factorial (Loop)      | for loop                 |
| Fibonacci             | Loop + variable swapping |

---

## 🔢 1️⃣ Armstrong Number Program

> A number is an **Armstrong number** if
> **sum of (each digit raised to power n) = number itself**
> where `n` = number of digits

```
num = int(input("Enter a number: "))
temp = num
n = len(str(num))
sum = 0

while temp > 0:
    digit = temp % 10
    sum = sum + (digit ** n)
    temp = temp // 10

if sum == num:
    print("Armstrong Number")
else:
    print("Not an Armstrong Number")
```

### ✅ Examples:

* 153 → ✔ Armstrong
* 1 → ✔ Armstrong
* 1634 → ✔ Armstrong

---

## 🔲 2️⃣ Perfect Square Program

> A number is a **perfect square** if it is the square of an integer

```
num = int(input("Enter a number: "))
i = 1

while i * i <= num:
    if i * i == num:
        print("Perfect Square")
        break
    i += 1
else:
    print("Not a Perfect Square")
```

---

## 🔢 3️⃣ Prime Number Program

> A **prime number** is divisible only by **1 and itself**

```
num = int(input("Enter a number: "))

if num <= 1:
    print("Not a Prime Number")
else:
    for i in range(2, num):
        if num % i == 0:
            print("Not a Prime Number")
            break
    else:
        print("Prime Number")
```

---

## ⭐ Summary Table (Exam Friendly)

| Program        | Key Logic          |
| -------------- | ------------------ |
| Armstrong      | Digits power & sum |
| Perfect Square | Check i × i        |
| Prime          | Divisibility check |

---

## 🔁 1️⃣ Reverse a String

```
s = input("Enter a string: ")
rev = ""

for ch in s:
    rev = ch + rev

print("Reversed string:", rev)
```

---

## 🔁 2️⃣ Reverse a Number

```
num = int(input("Enter a number: "))
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num = num // 10

print("Reversed number:", rev)
```

---

## 🔄 3️⃣ Check Palindrome Number

```
num = int(input("Enter a number: "))
temp = num
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num = num // 10

if temp == rev:
    print("Palindrome Number")
else:
    print("Not a Palindrome Number")
```

---

## 🔄 4️⃣ Check Palindrome String

```
s = input("Enter a string: ")
rev = s[::-1]

if s == rev:
    print("Palindrome String")
else:
    print("Not a Palindrome String")
```

---

## 🔍 5️⃣ Find Duplicate Characters in a String

```
s = input("Enter a string: ")
dup = ""

for ch in s:
    if s.count(ch) > 1 and ch not in dup:
        dup = dup + ch

print("Duplicate characters:", dup)
```

---

## 🔢 6️⃣ Permutation and Combination Program

```
import math

n = int(input("Enter n: "))
r = int(input("Enter r: "))

perm = math.factorial(n) // math.factorial(n - r)
comb = math.factorial(n) // (math.factorial(r) * math.factorial(n - r))

print("Permutation (nPr):", perm)
print("Combination (nCr):", comb)
```

---

## 🔢 7️⃣ Highest Number Using All Digits Once

```
num = input("Enter a number: ")

digits = sorted(num, reverse=True)
largest = ""

for d in digits:
    largest = largest + d

print("Highest possible number:", largest)
```

---

## ⭐ 8️⃣ Star Pattern Programs

### Pattern 1: Right Triangle

```
n = int(input("Enter number of rows: "))

for i in range(1, n + 1):
    print("*" * i)
```

Output:

```
*
**
***
****
```

---

### Pattern 2: Inverted Triangle

```
n = int(input("Enter number of rows: "))

for i in range(n, 0, -1):
    print("*" * i)
```

---

### Pattern 3: Pyramid

```
n = int(input("Enter number of rows: "))

for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)
```

---

## 🧮 WAP to print table of a given number

```
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(num * i)
```

---

### 📝 Example Input:

```
Enter a number: 2
```

### ✅ Output:

```
2
4
6
8
10
12
14
16
18
20
```

---

### ⭐ Alternative Format (if multiplication format is required):

```
num = int(input("Enter a number: "))

for i in range(1, 11):
    print(num, "x", i, "=", num * i)
```

---

## 1️⃣ Bubble Sort Program

```
nums = list(map(int, input("Enter numbers separated by space: ").split()))
n = len(nums)

for i in range(n-1):
    for j in range(n-1-i):
        if nums[j] > nums[j+1]:
            nums[j], nums[j+1] = nums[j+1], nums[j]

print("Sorted numbers:", nums)
```

---

## 2️⃣ Area and Perimeter of a Circle

```
import math

r = float(input("Enter radius of circle: "))

area = math.pi * r * r
perimeter = 2 * math.pi * r

print("Area of circle:", area)
print("Perimeter of circle:", perimeter)
```

---

## 3️⃣ Average of Three Numbers

```
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))

avg = (a + b + c) / 3
print("Average:", avg)
```

---

## 4️⃣ Maximum and Minimum of Three Numbers

```
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
c = float(input("Enter third number: "))

maximum = max(a, b, c)
minimum = min(a, b, c)

print("Maximum number:", maximum)
print("Minimum number:", minimum)
```

---

## 5️⃣ Sum of Digits of an Integer

```
num = int(input("Enter an integer: "))
temp = num
sum_digits = 0

while temp > 0:
    sum_digits += temp % 10
    temp //= 10

print("Sum of digits:", sum_digits)
```

---

### ✅ Exam Tips:

* Bubble sort uses **nested loops**
* Area and perimeter use `math.pi`
* Average = sum ÷ number of elements
* Maximum/minimum can be done using `max()` / `min()`
* Sum of digits uses **modulus (%) and integer division (//)**

---

## 1️⃣ Swap Two Variables

### a) Using Temporary Variable

```python
a = int(input("Enter a: "))
b = int(input("Enter b: "))

temp = a
a = b
b = temp

print("After swapping: a =", a, "b =", b)
```

### b) Using Arithmetic Operations

```python
a = int(input("Enter a: "))
b = int(input("Enter b: "))

a = a + b
b = a - b
a = a - b

print("After swapping: a =", a, "b =", b)
```

### c) Using Python Unpacking

```python
a = int(input("Enter a: "))
b = int(input("Enter b: "))

a, b = b, a

print("After swapping: a =", a, "b =", b)
```

---

## 2️⃣ Add and Multiply Two Binary Numbers

```python
a = input("Enter first binary number: ")
b = input("Enter second binary number: ")

sum_bin = bin(int(a, 2) + int(b, 2))[2:]
prod_bin = bin(int(a, 2) * int(b, 2))[2:]

print("Sum:", sum_bin)
print("Product:", prod_bin)
```

---

## 3️⃣ Decimal to Binary Without Built-in

```python
num = int(input("Enter decimal number: "))
binary = ""

if num == 0:
    binary = "0"

while num > 0:
    binary = str(num % 2) + binary
    num //= 2

print("Binary:", binary)
```

---

## 4️⃣ Distance Between Two Points

```python
import math

x1 = float(input("Enter x1: "))
y1 = float(input("Enter y1: "))
x2 = float(input("Enter x2: "))
y2 = float(input("Enter y2: "))

distance = math.sqrt((x2 - x1)**2 + (y2 - y1)**2)
print("Distance:", distance)
```

---

## 5️⃣ Count Letters, Spaces, Numbers, Others

```python
s = input("Enter a string: ")

letters = spaces = digits = others = 0

for ch in s:
    if ch.isalpha():
        letters += 1
    elif ch.isspace():
        spaces += 1
    elif ch.isdigit():
        digits += 1
    else:
        others += 1

print("Letters:", letters)
print("Spaces:", spaces)
print("Digits:", digits)
print("Other characters:", others)
```

---

## 6️⃣ ASCII Value of Character

```python
ch = input("Enter a character: ")
print("ASCII value:", ord(ch))
```

---

## 7️⃣ Compute n + n*n + n*n*n

```python
n = int(input("Enter a number: "))
result = n + n*n + n*n*n
print("Result:", result)
```

---

## 8️⃣ Size of a File

```python
import os

filename = input("Enter file name: ")
size = os.path.getsize(filename)
print("Size of file:", size, "bytes")
```

---

## 9️⃣ Display System Time

```python
import time
print("Current system time:", time.strftime("%H:%M:%S"))
```

---

## 0️⃣ Current Date and Time in Specific Format

```python
from datetime import datetime

now = datetime.now()
print("Current date and time:", now.strftime("%d-%m-%Y %H:%M:%S"))
```

---

## 1️⃣ Count Factors of a Number

```python
n = int(input("Enter a number: "))
count = 0

for i in range(1, n+1):
    if n % i == 0:
        count += 1

print("Number of factors:", count)
```

---

## 2️⃣ Capitalize First Letter of Each Word

```python
sentence = input("Enter a sentence: ")
print("Capitalized:", sentence.title())
```

---

## 3️⃣ Penultimate Word of a Sentence

```python
sentence = input("Enter a sentence: ").split()
if len(sentence) >= 2:
    print("Penultimate word:", sentence[-2])
else:
    print("Not enough words")
```

---

## 4️⃣ Check if 4-digit Number Less Than 3000

```python
num = int(input("Enter a number: "))
if 1000 <= num <= 2999:
    print("Valid number")
else:
    print("Invalid number")
```

---

## 5️⃣ Second Last Maximum Value

```python
lst = list(map(int, input("Enter numbers: ").split()))
unique_lst = list(set(lst))
unique_lst.sort()
if len(unique_lst) >= 2:
    print("Second largest:", unique_lst[-2])
else:
    print("Not enough unique numbers")
```

---

## 6️⃣ Second Last Minimum Value

```python
lst = list(map(int, input("Enter numbers: ").split()))
unique_lst = list(set(lst))
unique_lst.sort()
if len(unique_lst) >= 2:
    print("Second smallest:", unique_lst[1])
else:
    print("Not enough unique numbers")
```

---

## 7️⃣ Number Repeated Exactly n Times

```python
lst = list(map(int, input("Enter numbers: ").split()))
n = int(input("Enter repetition count: "))

for num in set(lst):
    if lst.count(num) == n:
        print("Number repeated exactly", n, "times:", num)
```

---

## 1️⃣ Insert a Word in the Middle of Another String

```python
s = "Python 3.9"
word_to_insert = "Tutorial"

parts = s.split()
mid_index = len(parts) // 2
new_string = " ".join(parts[:mid_index] + [word_to_insert] + parts[mid_index:])
print("Result:", new_string)
```

**Output:**

```
Python Tutorial 3.9
```

---

## 2️⃣ Extract the First Half of a String

```python
s = input("Enter a string: ")
half_index = len(s) // 2
first_half = s[:half_index]
print("First half:", first_half)
```

---

## 3️⃣ Create String in Form `short + long + short`

```python
s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if len(s1) == len(s2):
    print("Error: Strings are of same length")
else:
    short, long = (s1, s2) if len(s1) < len(s2) else (s2, s1)
    result = short + long + short
    print("Result:", result)
```

---

## 4️⃣ Concatenate Two Strings Removing First Character

```python
s1 = input("Enter first string: ")
s2 = input("Enter second string: ")

if len(s1) >= 1 and len(s2) >= 1:
    result = s1[1:] + s2[1:]
    print("Result:", result)
else:
    print("Strings must be at least length 1")
```

---

## 5️⃣ New String Using First Three Characters (Use `#` if <3)

```python
s = input("Enter a string: ")

if len(s) >= 3:
    new_string = s[:3]
else:
    new_string = s + "#" * (3 - len(s))

print("Result:", new_string)
```

---

## 6️⃣ Split File Name and Extension

```python
filename = input("Enter file name with extension: ")
if "." in filename:
    name, ext = filename.rsplit(".", 1)
    print("Name:", name)
    print("Extension:", ext)
else:
    print("No extension found")
```

**Examples:**

```
my_photo.png → Name: my_photo  Ext: png
1.gz → Name: 1  Ext: gz
```

---

## 7️⃣ Check if String Starts with a Word

```python
string1 = "Hello how are you?"
word = "Hello"

print(string1.startswith(word))
```

**Output:**

```
True
```

---

## 8️⃣ Sort Array of Strings by Second Character

```python
arr = ["apple", "banana", "pear", "grape"]

sorted_arr = sorted(arr, key=lambda x: x[1])
print("Sorted array:", sorted_arr)
```

---

## 9️⃣ Find Strings Ending with "g" or Starting with "p"

```python
arr = ["ping", "python", "running", "play", "go"]

result = [s for s in arr if s.endswith("g") or s.startswith("p")]
print("Filtered strings:", result)
```

**Output:**

```
['ping', 'python', 'running', 'play']
```

---

## 1️⃣ Collatz Conjecture (Divide/Multiply until 1)

```python
n = int(input("Enter a number: "))

while n != 1:
    print(n, end=" -> ")
    if n % 2 == 0:
        n = n // 2
    else:
        n = n * 3 + 1
print(n)
```

**Example:** `6` → `6 -> 3 -> 10 -> 5 -> 16 -> 8 -> 4 -> 2 -> 1`

---

## 2️⃣ Check if 10 is First or Last Element

```python
arr = list(map(int, input("Enter integers separated by space: ").split()))

if len(arr) >= 2 and (arr[0] == 10 or arr[-1] == 10):
    print("10 is first or last element: True")
else:
    print("10 is first or last element: False")
```

---

## 3️⃣ Check if First or Last Element of Two Arrays are Same

```python
arr1 = list(map(int, input("Enter first array: ").split()))
arr2 = list(map(int, input("Enter second array: ").split()))

if len(arr1) >= 2 and len(arr2) >= 2 and (arr1[0] == arr2[0] or arr1[-1] == arr2[-1]):
    print("First or last element same: True")
else:
    print("First or last element same: False")
```

---

## 4️⃣ Merge Two Arrays Alternately

```python
arr1 = list(map(int, input("Enter first array: ").split()))
arr2 = list(map(int, input("Enter second array: ").split()))

merged = []
for i in range(min(len(arr1), len(arr2))):
    merged.append(arr1[i])
    merged.append(arr2[i])

# Add remaining elements if arrays are unequal
merged += arr1[len(arr2):] + arr2[len(arr1):]

print("Merged array:", merged)
```

---

## 5️⃣ Right Shift an Integer (Rotate Last Digit to Front)

```python
val = input("Enter an integer: ")
right_shifted_val = val[-1] + val[:-1]
print("Right shifted value:", right_shifted_val)
```

**Example:** `1234` → `4123`

---

## 6️⃣ Left Shift an Integer (Rotate First Digit to End)

```python
val = input("Enter an integer: ")
left_shifted_val = val[1:] + val[0]
print("Left shifted value:", left_shifted_val)
```

**Example:** `1234` → `2341`

---

## 7️⃣ Sum of Digits and Convert Sum to English Words

```python
num = int(input("Enter an integer: "))
total = sum(int(d) for d in str(num))

num_to_word = ["Zero", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine"]
words = [num_to_word[int(d)] for d in str(total)]
print(" ".join(words))
```

**Example:**
`1234 → One Zero`
`999999999999 → One Zero Eight`

---

## 8️⃣ Split Numbers Divisible by 5 and Remaining

```python
lst = list(map(int, input("Enter numbers: ").split()))

div5 = [x for x in lst if x % 5 == 0]
remaining = [x for x in lst if x % 5 != 0]

print("Divisible by 5:", div5)
print("Remaining:", remaining)
```

---

## 9️⃣ Count Even and Odd Elements in Array

```python
arr = list(map(int, input("Enter numbers: ").split()))

even_count = sum(1 for x in arr if x % 2 == 0)
odd_count = len(arr) - even_count

print("Even elements:", even_count)
print("Odd elements:", odd_count)
```

---

## 1️⃣ Check for Two Consecutive 10s or 20s but Not Both

```python
arr = list(map(int, input("Enter array of integers: ").split()))

has_10_pair = any(arr[i] == 10 and arr[i+1] == 10 for i in range(len(arr)-1))
has_20_pair = any(arr[i] == 20 and arr[i+1] == 20 for i in range(len(arr)-1))

# True if either 10 pair or 20 pair but not both
result = (has_10_pair != has_20_pair)
print(result)
```

**Examples:**

```
[10,30,50,10,10] → True  
[20,20,89,67] → True  
[10,10,20,20] → False
```

---

## 2️⃣ Unique Numbers in Array and Their Count

```python
arr = list(map(int, input("Enter numbers: ").split()))

unique_counts = {x: arr.count(x) for x in set(arr)}

print("Unique numbers and their counts:")
for num, count in unique_counts.items():
    print(num, ":", count)
```

---

## 3️⃣ Unique Words in a Sentence and Count

```python
sentence = input("Enter a sentence: ").split()

unique_words = {word: sentence.count(word) for word in set(sentence)}

print("Unique words and their counts:")
for word, count in unique_words.items():
    print(word, ":", count)
```

---

## 4️⃣ Unique Characters in a Sentence and Count

```python
sentence = input("Enter a sentence: ")

unique_chars = {ch: sentence.count(ch) for ch in set(sentence)}

print("Unique characters and their counts:")
for ch, count in unique_chars.items():
    print(ch, ":", count)
```

---

## 5️⃣ Check for Three Increasing Adjacent Numbers

```python
arr = list(map(int, input("Enter array of integers: ").split()))

found = any(arr[i] < arr[i+1] < arr[i+2] for i in range(len(arr)-2))

print(found)
```

**Examples:**

```
[1,3,5,2,5] → True  
[1,1,4,2,67,5] → False  
[1,9,2,67,100,124,34] → True
```

---

