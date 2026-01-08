## 🐚 Session 21 & 22: BASH CLI Error Handling, Debugging, Redirection, Control Structures, Variables & Regular Expressions

---

## 🧠 **1. Concept Overview**

* **BASH (Bourne Again SHell)** is the default Linux shell used for **command execution & scripting**.
* Shell scripting automates system tasks using:

  * Variables
  * Conditions
  * Loops
  * Input/Output redirection
  * Error handling
* PG-DITISS focus is on **syntax, behavior, exit status, and MCQ traps**.

---

## 📖 **2. Key Definitions**

* **Shell Script:** File containing Linux commands executed sequentially.
* **Shebang:** `#!/bin/bash` – specifies interpreter.
* **Exit Status:** Numeric value returned after command execution.
* **STDIN / STDOUT / STDERR:** Standard input, output, error streams.
* **Regex:** Pattern used for matching strings.

---

## 🧩 **3. Main Content (Organized & Exam-Oriented)**

---

## ⚠️ **A. BASH CLI Error Handling**

### 🔹 Exit Status

* Every command returns an **exit code**.
* `0` → Success
* `1–255` → Failure

```bash
echo $?
```

📌 **MCQ Fact:**

* `$?` stores exit status of **last executed command**

---

### 🔹 Common Error Handling Techniques

* **Using exit**

```bash
exit 1
```

* **Using logical operators**

```bash
command && success
command || failure
```

---

## 🐞 **B. Debugging of Shell Scripts**

### 🔹 Debugging Options

| Option | Meaning                         |
| ------ | ------------------------------- |
| `-x`   | Print commands before execution |
| `-v`   | Print shell input lines         |
| `-n`   | Syntax check only               |

```bash
bash -x script.sh
```

📌 **MCQ Trap:**

* `-n` does **not execute** script

---

## 🔁 **C. Redirection in Shell Scripts**

### 🔹 Standard Streams

| Stream | FD | Description |
| ------ | -- | ----------- |
| STDIN  | 0  | Keyboard    |
| STDOUT | 1  | Screen      |
| STDERR | 2  | Error       |

---

### 🔹 Redirection Operators

* `>` → overwrite output
* `>>` → append output
* `<` → input redirection
* `2>` → redirect error
* `&>` → stdout + stderr

```bash
ls abc > out.txt 2> err.txt
```

📌 **MCQ Fact:**

* `2>&1` → redirect error to output

---

## 🔀 **D. Control Structures**

---

## 🔹 Conditional Statements

### 🔸 if Statement

```bash
if [ condition ]
then
   commands
fi
```

### 🔸 if–else

```bash
if [ condition ]
then
   commands
else
   commands
fi
```

---

### 🔹 Test Operators

* `-eq` equal
* `-ne` not equal
* `-gt` greater than
* `-lt` less than
* `-f` file exists
* `-d` directory exists

📌 **MCQ Trap:**

* `=` is for **string**, `-eq` for **integer**

---

## 🔁 **E. Loops**

### 🔹 for Loop

```bash
for i in 1 2 3
do
  echo $i
done
```

### 🔹 while Loop

```bash
while [ condition ]
do
  commands
done
```

### 🔹 until Loop

```bash
until [ condition ]
do
  commands
done
```

📌 **MCQ Fact:**

* `until` runs while condition is **false**

---

## 📦 **F. Variables & Strings**

### 🔹 Variable Declaration

```bash
name="Linux"
```

📌 **Rules:**

* No space around `=`
* Case-sensitive
* Default type: **string**

---

### 🔹 Access Variable

```bash
echo $name
```

---

### 🔹 Special Variables

| Variable | Meaning              |
| -------- | -------------------- |
| `$0`     | Script name          |
| `$1…$9`  | Positional arguments |
| `$#`     | Number of arguments  |
| `$*`     | All arguments        |
| `$$`     | PID                  |
| `$?`     | Exit status          |

---

### 🔹 String Operations

```bash
${#var}        # length
${var:0:3}    # substring
```

---

## 🔍 **G. Regular Expressions (Regex)**

### 🔹 Purpose

* Pattern matching using `grep`, `sed`, `awk`, `[[ ]]`

---

### 🔹 Common Regex Symbols

| Symbol  | Meaning              |
| ------- | -------------------- |
| `^`     | Start of line        |
| `$`     | End of line          |
| `.`     | Any single character |
| `*`     | Zero or more         |
| `+`     | One or more          |
| `[a-z]` | Character range      |

---

### 🔹 Regex with grep

```bash
grep "^root" /etc/passwd
```

📌 **MCQ Trap:**

* Regex ≠ Wildcards

---

## 🎯 **4. Important Facts / Points for MCQs**

* Default shell = **bash**
* `$?` gives last exit code
* `#!/bin/bash` mandatory for scripts
* `-x` used for debugging
* `2>` redirects errors
* `[[ ]]` better than `[ ]`
* Regex used with `grep`, not `ls`

---

## 🧪 **5. Examples**

* Check file exists:

```bash
if [ -f file.txt ]
```

* Loop through arguments:

```bash
for i in "$@"
```

* Regex email search:

```bash
grep "@gmail.com" file.txt
```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* Space inside `[ ]` is **mandatory**
* `$var` ≠ `${var}`
* `=` ≠ `-eq`
* `*` wildcard ≠ regex `*`
* `exit 0` ≠ script output
* `&&` stops on failure

---

📌 **One-Line Exam Memory Aid:**

> **BASH scripting = Variables + Conditions + Loops + Redirection + Regex**

