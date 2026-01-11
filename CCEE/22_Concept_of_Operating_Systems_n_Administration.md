> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 22

## **Session 22 : Linux OS**

---

### 1. In a Bash script, you need to store the integer value `10` in a variable `count`. Which of the following is correct?

* [ ] var == 10
* [ ] let var = 10
* [ ] count=10
* [ ] set var = 10

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** count=10
💡 In Bash, assignment is done without spaces around `=`. `let` is used for arithmetic evaluation but syntax `let var = 10` with spaces is incorrect. `==` is a comparison operator, not assignment.

</details>

---

### 2. You have a variable `username="admin"`. How would you correctly display its value in a Bash script?

* [ ] $(username)
* [ ] #username
* [ ] &username
* [ ] $username

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** $username
💡 Variables are referenced with `$` in Bash. `$(...)` is command substitution, `#` starts a comment, `&` has no such variable reference meaning.

</details>

---

### 3. Which Bash command correctly tests if two string variables, `$a` and `$b`, are equal?

* [ ] test $a == $b
* [ ] cmp $a $b
* [ ] strcomp $a $b
* [ ] if $a -eq $b

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** test $a == $b
💡 `test` or `[ ]` with `==` is used for string comparison. `-eq` is numeric comparison, `cmp` compares files, and `strcomp` is not a Bash command.

</details>

---

### 4. In Bash, which of the following correctly represents a string literal?

* [ ] "Hello"
* [ ] Hello
* [ ] 'Hello'
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Unquoted words are treated as strings if they do not match commands or variables. Both single and double quotes define string literals.

</details>

---

### 5. Inside a conditional `[ ]` in Bash, what does the `=` operator do?

* [ ] Checks string length
* [ ] Assigns a value
* [ ] Compares strings
* [ ] Ends a loop

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Compares strings
💡 Within `[ ]`, `=` is used to compare strings. Assignment uses `=` outside `[ ]`.

</details>

---

### 6. Given the command `echo "Welcome $USER"`, what is the output?

* [ ] Prints literally `Welcome $USER`
* [ ] Expands `$USER` to the current username
* [ ] Gives an error
* [ ] Prompts for input

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Expands `$USER` to the current username
💡 `$USER` is an environment variable representing the currently logged-in user.

</details>

---

### 7. In Bash, which symbol is used to indicate regex matching inside `[[ ]]`?

* [ ] /
* [ ] ?
* [ ] ~
* [ ] @

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ~
💡 The `[[ string =~ regex ]]` syntax uses `~` for regex matching.

</details>

---

### 8. In Bash scripting, what does the test `-z "$var"` check for?

* [ ] File is executable
* [ ] String is non-empty
* [ ] String is empty
* [ ] Integer equals zero

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** String is empty
💡 `-z` returns true if the string length is zero.

</details>

---

### 9. Which regular expression correctly matches any 3-digit number in Bash?

* [ ] [0-9]{3}
* [ ] [0-9][0-9][0-9]
* [ ] \d{3}
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** [0-9][0-9][0-9]
💡 Bash `[[ string =~ regex ]]` supports basic regex. `{3}` and `\d` may not be portable in all shells. `[0-9][0-9][0-9]` is reliable.

</details>

---

### 10. You want to check if a variable `var` is unset or empty. Which is correct?

* [ ] [ -n "$var" ]
* [ ] [ "$var" = "" ]
* [ ] [ -z "$var" ]
* [ ] if $var == NULL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** [ -z "$var" ]
💡 `-z` returns true if the variable is unset or empty. `-n` checks non-empty, `== NULL` is not standard.

</details>

---

### 11. Which operator tests for a regex match in Bash?

* [ ] =~
* [ ] ==
* [ ] !=
* [ ] =

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** =~
💡 `[[ string =~ regex ]]` uses `=~` for regex evaluation.

</details>

---

### 12. Which Bash construct allows conditional branching based on multiple options?

* [ ] case
* [ ] for
* [ ] if-then-else
* [ ] do-while

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** if-then-else
💡 `if-then-else` handles conditional logic. `case` is for pattern matching, loops are for iteration.

</details>

---

### 13. In a Bash regex, what does the pattern `[^a-z]` match?

* [ ] Any lowercase letter
* [ ] Nothing
* [ ] Any character except lowercase letters
* [ ] Letters a through z

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Any character except lowercase letters
💡 `[^...]` in regex negates the character class. Here it matches anything that is not a lowercase letter.

</details>

---

### 14. You have a variable `msg="Hello World"`. How do you ensure it is treated as a single argument in a Bash command?

* [ ] Use curly braces `{}`
* [ ] Use single quotes `' '`
* [ ] Use double quotes `" "`
* [ ] Use backticks ````

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use double quotes `" "`
💡 Quoting with `" "` preserves spaces in variables, treating them as a single argument. Single quotes also work but may prevent variable expansion.

</details>

---

### 15. What is the primary role of `[[ ... ]]` in Bash?

* [ ] Arithmetic expressions
* [ ] Advanced conditional testing
* [ ] Looping
* [ ] File manipulation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Advanced conditional testing
💡 `[[ ... ]]` provides improved conditional evaluation, supporting string comparisons, regex, and logical operators.

</details>

---

### 16. Which command prints only the lines from a file that match a given pattern?

* [ ] cat
* [ ] sort
* [ ] grep
* [ ] cut

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** grep
💡 `grep` filters lines matching a pattern. `cat` prints everything, `sort` orders, and `cut` extracts columns.

</details>

---

### 17. In Bash conditionals, what does the `!` operator do?

* [ ] OR
* [ ] AND
* [ ] NOT
* [ ] EQUALS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NOT
💡 `!` negates the result of a test. For example, `[ ! -f file ]` is true if `file` does not exist.

</details>

---

### 18. What is the output of `echo ${#string}` in Bash?

* [ ] The string itself
* [ ] First character of the string
* [ ] Length of the string
* [ ] Last character of the string

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Length of the string
💡 `${#var}` expands to the number of characters in `var`.

</details>

---

### 19. Which regular expression symbol matches the beginning of a line?

* [ ] $
* [ ] ^
* [ ] *
* [ ] .

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ^
💡 `^` anchors the match to the start of a line, `$` to the end, `*` is repetition, `.` matches any character.

</details>

---

### 20. In an `if` statement, what does `elif` represent?

* [ ] End if
* [ ] Else if
* [ ] Else
* [ ] Syntax error

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Else if
💡 `elif` allows chaining multiple conditional checks after an `if`.

</details>

---

### 21. Which operator correctly compares numeric values in Bash?

* [ ] ==
* [ ] -eq
* [ ] =
* [ ] -match

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -eq
💡 `-eq`, `-lt`, `-gt`, etc., are used for numeric comparisons inside `[ ]`. `==` is for strings.

</details>

---

### 22. Which of the following regex patterns can match a basic email address in Bash?

* [ ] [a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+.[a-z]{2,}
* [ ] .*@.*..*
* [ ] \w+@\w+.\w+
* [ ] All of the above (with limitations)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above (with limitations)
💡 All patterns can match emails to varying degrees. `[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-z]{2,}` is most precise, others are simpler but may allow invalid emails.

</details>

---

### 23. If `var` is unset, what is the result of `[ "$var" != "abc" ]`?

* [ ] true
* [ ] false
* [ ] error
* [ ] undefined

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** true
💡 An unset variable expands to an empty string. `"" != "abc"` evaluates to true.

</details>

---

### 24. What does `${var:-default}` do in Bash?

* [ ] Assigns `default` to `var`
* [ ] Returns `var` if set, otherwise `default`
* [ ] Checks string length
* [ ] Exits the script

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Returns `var` if set, otherwise `default`
💡 This is parameter expansion with a default value. It does not assign unless `:=` is used.

</details>

---

### 25. What is the effect of `[[ $str =~ ^[0-9]+$ ]]` in Bash?

* [ ] Checks if string is alphabetic
* [ ] Checks if string is alphanumeric
* [ ] Checks if string contains only digits
* [ ] Syntax error

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Checks if string contains only digits
💡 `^[0-9]+$` matches a string composed entirely of digits from start to end.

</details>

---

### 26. Which is the correct way to test if a file contains a specific word in Bash?

* [ ] grep word filename
* [ ] if grep -q word filename; then
* [ ] if find word in filename
* [ ] if [ word in filename ]

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** if grep -q word filename; then
💡 `grep -q` checks silently for a match. Using `if` with it allows conditional execution.

</details>

---

### 27. Which Bash construct allows matching multiple regex patterns efficiently?

* [ ] if-else
* [ ] case-esac
* [ ] for-loop
* [ ] select-case

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** case-esac
💡 `case` can handle multiple pattern matches cleanly without writing multiple `if` statements.

</details>

---

### 28. What does `[[ $str =~ [A-Z]{2,5} ]]` match?

* [ ] Any uppercase string of 2 to 5 letters
* [ ] Only lowercase letters
* [ ] Numbers
* [ ] Nothing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Any uppercase string of 2 to 5 letters
💡 `[A-Z]{2,5}` matches sequences of 2 to 5 uppercase letters.

</details>

---

### 29. When does `[ "$var" -gt 10 ]` evaluate to true?

* [ ] If `var` is a string
* [ ] If `var` is a number greater than 10
* [ ] Always true
* [ ] On syntax error

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** If `var` is a number greater than 10
💡 `-gt` performs numeric comparison. Using it with a non-numeric string triggers an error.

</details>

---

### 30. How can you substitute a substring in a Bash variable?

* [ ] ${var/pattern/replacement}
* [ ] replace var pattern replacement
* [ ] echo var | sed pattern
* [ ] ${replace(var, pattern, replacement)}

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ${var/pattern/replacement}
💡 Bash supports parameter expansion for string substitution. `sed` can also do it externally, but this is the built-in way.

</details>

---
