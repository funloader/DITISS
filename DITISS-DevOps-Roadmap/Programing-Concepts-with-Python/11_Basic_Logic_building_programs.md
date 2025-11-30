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
