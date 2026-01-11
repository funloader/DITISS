> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 20

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

## **Session 23 : Linux OS**

---

### 1. A system administrator writes a Bash script for automating log rotation. Which command is **mandatory** to allow the script to be executed directly from the shell?

* [ ] chmod +r script.sh
* [ ] chmod +x script.sh
* [ ] make executable script.sh
* [ ] exec chmod script.sh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chmod +x script.sh
💡 The execute (`+x`) permission is required to run a script directly using `./script.sh` in Unix/Linux systems.

</details>

---

### 2. In a Bash script used for patch automation, the first line is `#!/bin/bash`. What is the **primary purpose** of this line?

* [ ] It marks the beginning of a function
* [ ] It is treated as a comment
* [ ] It specifies the interpreter to execute the script
* [ ] It terminates script execution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It specifies the interpreter to execute the script
💡 The shebang tells the kernel which interpreter should be used to run the script.

</details>

---

### 3. A script lacks execute permissions but must still be run for testing. Which command correctly executes it?

* [ ] run script.sh
* [ ] bash script.sh
* [ ] execute script.sh
* [ ] launch script.sh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** bash script.sh
💡 Invoking the interpreter directly bypasses the need for execute permissions.

</details>

---

### 4. Which symbol is used to add comments in Bash scripts for documentation or code clarity?

* [ ] //
* [ ] #
* [ ] --
* [ ] **

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** #
💡 Anything following `#` (except shebang) is ignored by the shell.

</details>

---

### 5. Which loop syntax is **valid and commonly used** in Bash for iterating over a numeric range?

* [ ] for i=1 to 10
* [ ] loop i in range
* [ ] for i in {1..10}
* [ ] repeat 10 times

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** for i in {1..10}
💡 Brace expansion is a standard Bash feature for numeric iteration.

</details>

---

### 6. On a Debian-based system, which command is used to **refresh the local package index** before applying security patches?

* [ ] yum update
* [ ] dnf upgrade
* [ ] apt-get update
* [ ] update-security

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt-get update
💡 It synchronizes the package index with configured repositories.

</details>

---

### 7. Which command is typically used in Bash scripts to display output or status messages?

* [ ] print()
* [ ] echo
* [ ] write
* [ ] display

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** echo
💡 `echo` is the standard command for outputting text to stdout in shell scripts.

</details>

---

### 8. What is the **primary role** of `cron` in Linux system administration?

* [ ] Log deletion
* [ ] Email notification
* [ ] Scheduling recurring jobs
* [ ] CPU monitoring

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Scheduling recurring jobs
💡 Cron executes commands or scripts automatically at defined times.

</details>

---

### 9. Where are **user-specific cron jobs** stored on most Linux systems?

* [ ] /etc/crontab
* [ ] /var/spool/cron/crontabs
* [ ] ~/.bashrc
* [ ] ~/.cronjob

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/spool/cron/crontabs
💡 Each user has an individual crontab file managed by the cron daemon.

</details>

---

### 10. What does `apt-get upgrade` primarily do?

* [ ] Installs new packages
* [ ] Removes obsolete packages
* [ ] Updates package lists
* [ ] Installs latest versions of installed packages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Installs latest versions of installed packages
💡 It upgrades existing packages without removing or adding dependencies.

</details>

---

### 11. What is the effect of using `set -e` in a Bash script handling system updates?

* [ ] Exits on syntax error only
* [ ] Continues after command failure
* [ ] Exits immediately if any command fails
* [ ] Enables verbose output

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Exits immediately if any command fails
💡 Prevents cascading failures in automation scripts.

</details>

---

### 12. Which cron entry correctly schedules a script to run **daily at 6:00 AM**?

* [ ] 0 6 * * * /path/script.sh
* [ ] 6 0 * * * /path/script.sh
* [ ] * 6 0 0 * /script.sh
* [ ] 0 0 6 * * /script.sh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 0 6 * * * /path/script.sh
💡 Cron format: minute hour day month weekday.

</details>

---

### 13. Which Ubuntu tool is recommended for **automatic unattended security updates**?

* [ ] apt-cron
* [ ] unattended-upgrades
* [ ] yum-cron
* [ ] security-updater

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** unattended-upgrades
💡 Official Ubuntu package for secure, automatic updates.

</details>

---

### 14. What does the `&&` operator ensure in Bash scripts?

* [ ] Executes command regardless of result
* [ ] Executes next command only if previous succeeds
* [ ] Terminates execution
* [ ] Redirects output

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Executes next command only if previous succeeds
💡 Used for safe command chaining.

</details>

---

### 15. Which is the **correct syntax** for a conditional expression in Bash?

* [ ] if ($a == $b)
* [ ] if [$a == $b]
* [ ] if [ $a == $b ]
* [ ] if $a eq $b

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** if [ $a == $b ]
💡 Proper spacing is mandatory in Bash conditionals.

</details>

---

### 16. Which command shows packages that have available upgrades?

* [ ] dpkg -l
* [ ] apt list --upgradable
* [ ] apt-get changelog
* [ ] apt-show-versions -u -a

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt list --upgradable
💡 Lists all installed packages with newer versions available.

</details>

---

### 17. What is the effect of using `#!/bin/bash -x` in a script?

* [ ] Silent execution
* [ ] Enables execution trace for debugging
* [ ] Runs script as root
* [ ] Disables logging

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enables execution trace for debugging
💡 Displays each command before execution.

</details>

---

### 18. Which Bash test condition checks whether a file exists?

* [ ] [ -e filename ]
* [ ] check file
* [ ] exists(filename)
* [ ] file?

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** [ -e filename ]
💡 `-e` tests for existence of files or directories.

</details>

---

### 19. Which command applies **security updates only** on Red Hat–based systems?

* [ ] apt upgrade
* [ ] yum update --security
* [ ] yum patch
* [ ] rpm patch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** yum update --security
💡 Filters updates marked as security fixes.

</details>

---

### 20. Which redirection operator sends **both stdout and stderr** to a file?

* [ ] 2> file
* [ ] > file
* [ ] &> file
* [ ] #> file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** &> file
💡 Bash-specific operator for combined output redirection.

</details>

---

### 21. Which is considered a **best practice** in automation scripts?

* [ ] Hard-code credentials
* [ ] Use absolute paths
* [ ] Avoid logs
* [ ] Ignore exit codes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use absolute paths
💡 Ensures predictable behavior in non-interactive environments.

</details>

---

### 22. What is the correct way to trap runtime errors in a Bash script?

* [ ] trap 'echo Error'
* [ ] trap 'exit 1' ERR
* [ ] catch error
* [ ] trap error

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** trap 'exit 1' ERR
💡 `ERR` signal catches command failures.

</details>

---

### 23. Which service enables **scheduled automatic patching** on RHEL 8+ systems?

* [ ] yum-patch
* [ ] dnf auto
* [ ] dnf-automatic
* [ ] patch-now

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dnf-automatic
💡 Official Red Hat solution for automated updates.

</details>

---

### 24. What is the function of `/etc/cron.allow`?

* [ ] Blocks cron usage
* [ ] Grants root-only access
* [ ] Lists users allowed to use cron
* [ ] Enables cron logging

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lists users allowed to use cron
💡 Access control mechanism for cron usage.

</details>

---

### 25. How can a script ensure **only one instance runs at a time**?

* [ ] Temporary file
* [ ] ps command
* [ ] Lock file using flock
* [ ] Scripts always run independently

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lock file using flock
💡 Prevents race conditions in automation.

</details>

---

### 26. How do you log **all script output including errors**?

* [ ] script.sh > logfile
* [ ] script.sh 2> logfile
* [ ] script.sh &> logfile
* [ ] script.sh log >

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** script.sh &> logfile
💡 Captures both stdout and stderr.

</details>

---

### 27. How can you ensure a scheduled patch script runs **only once**, even if retried?

* [ ] Set delay
* [ ] Use a mutex
* [ ] Use systemd timers
* [ ] Check timestamp or lock file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Check timestamp or lock file
💡 Prevents duplicate execution after failure.

</details>

---

### 28. Which command verifies the **cryptographic signature** of a patch file?

* [ ] sha256sum
* [ ] gpg --verify
* [ ] md5sum
* [ ] ls -l

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gpg --verify
💡 Ensures authenticity and integrity of signed files.

</details>

---

### 29. What does `set -uo pipefail` enforce in a Bash script?

* [ ] Ignores pipeline errors
* [ ] Fails on unset variables and pipeline errors
* [ ] Enables debugging
* [ ] Breaks pipelines

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fails on unset variables and pipeline errors
💡 Improves script robustness and reliability.

</details>

---

### 30. What is the **most secure method** to update patches on a headless Ubuntu server without prompts?

* [ ] apt update
* [ ] yum patch -y
* [ ] unattended-upgrades
* [ ] dnf install --no-prompt

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** unattended-upgrades
💡 Designed for non-interactive, secure environments.

</details>

---

## **Session 24 : Linux OS**

---

### 1. In a Bash script designed for operational monitoring, which command is most commonly used to write status or debug messages to standard output (and optionally redirect them to logs)?

* [ ] print
* [ ] write
* [ ] printf
* [ ] echo

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** echo
💡 `echo` is the most widely used and portable Bash built-in command for printing messages, making it ideal for logging and debugging output in scripts.

</details>

---

### 2. A system administrator wants to inspect authentication, kernel, and service logs on a Linux system. Which directory conventionally stores such log files?

* [ ] /etc/logs
* [ ] /bin/logs
* [ ] /home/log
* [ ] /var/log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log
💡 `/var/log` follows the Filesystem Hierarchy Standard (FHS) and is used for variable log data generated by system services and applications.

</details>

---

### 3. While maintaining historical logs, a script must add new entries without overwriting existing data. Which Bash redirection operator should be used?

* [ ] >
* [ ] <
* [ ] |
* [ ] >>

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** >>
💡 The `>>` operator appends output to an existing file, ensuring log continuity without data loss.

</details>

---

### 4. A Bash script records timestamps for audit purposes. What does the `date` command return by default when executed inside a script?

* [ ] File creation timestamp
* [ ] Process start time
* [ ] System uptime
* [ ] Current system date and time

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Current system date and time
💡 The `date` command outputs the current system date and time, commonly used for timestamping log entries.

</details>

---

### 5. On modern Linux distributions using systemd, which command is primarily used to query centralized system logs?

* [ ] log
* [ ] dmesg
* [ ] journal
* [ ] journalctl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** journalctl
💡 `journalctl` interfaces with the systemd journal and allows structured, filtered access to system logs.

</details>

---

### 6. An administrator runs `tail -f /var/log/syslog` while troubleshooting a live issue. What is the primary effect of this command?

* [ ] Deletes old log entries
* [ ] Opens the file for editing
* [ ] Displays new log entries in real time
* [ ] Filters logs permanently

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Displays new log entries in real time
💡 The `-f` (follow) option streams new lines as they are written, useful for real-time monitoring.

</details>

---

### 7. From a security and compliance perspective, what is the primary purpose of implementing logging within scripts?

* [ ] Printing user output
* [ ] Delaying execution
* [ ] Maintaining an audit trail of activities
* [ ] Compiling source code

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Maintaining an audit trail of activities
💡 Logging supports auditing, troubleshooting, incident response, and regulatory compliance.

</details>

---

### 8. A SOC analyst needs to monitor CPU and memory usage of processes in real time. Which command best fulfills this requirement?

* [ ] df
* [ ] ls
* [ ] chmod
* [ ] top

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** top
💡 `top` provides a dynamic, real-time view of process-level CPU and memory utilization.

</details>

---

### 9. While debugging a script, an administrator wants to redirect both standard output and standard error to the same log file. Which syntax achieves this?

* [ ] > file 2>&1
* [ ] 2> file | 1>
* [ ] >> file 1 2
* [ ] &file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** > file 2>&1
💡 This redirects stdout to `file` and then redirects stderr to the same destination.

</details>

---

### 10. Which command provides a snapshot view of currently running processes suitable for scripting and reporting?

* [ ] proc
* [ ] ls
* [ ] pid
* [ ] ps

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ps
💡 `ps` displays process status and is commonly used in scripts for process inspection.

</details>

---

### 11. In log analysis, what does the command `awk '{print $1}' logfile` typically do?

* [ ] Replaces matched patterns
* [ ] Adds line numbers
* [ ] Prints the first whitespace-delimited field
* [ ] Searches for keywords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prints the first whitespace-delimited field
💡 `awk` splits input into fields; `$1` refers to the first field.

</details>

---

### 12. What is the primary role of `cron` when used with monitoring or logging scripts?

* [ ] Viewing process trees
* [ ] Logging script errors
* [ ] Automating scheduled script execution
* [ ] Triggering syslog manually

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automating scheduled script execution
💡 `cron` enables time-based automation, critical for periodic monitoring tasks.

</details>

---

### 13. Which service is responsible for aggregating, processing, and forwarding logs in many Linux systems?

* [ ] cron
* [ ] tar
* [ ] logrotate
* [ ] rsyslog

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rsyslog
💡 `rsyslog` handles centralized logging, filtering, and remote log forwarding.

</details>

---

### 14. What information does the `uptime` command provide that is relevant for performance monitoring?

* [ ] CPU temperature
* [ ] Network bandwidth
* [ ] System run time and load averages
* [ ] Logged-in users only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System run time and load averages
💡 Load averages indicate system demand over time, useful for capacity analysis.

</details>

---

### 15. A script must log only error messages without cluttering standard output. Which redirection is most appropriate?

* [ ] echo error > log
* [ ] echo > stderr
* [ ] error.log > 2
* [ ] 2>> error.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2>> error.log
💡 File descriptor `2` represents stderr; appending preserves existing error logs.

</details>

---

### 16. Which utility is primarily used to archive, compress, and manage old log files automatically?

* [ ] grep
* [ ] logger
* [ ] ziplog
* [ ] logrotate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** logrotate
💡 `logrotate` prevents uncontrolled log growth by rotating and compressing logs.

</details>

---

### 17. A disk usage alert script needs human-readable filesystem statistics. Which command is most suitable?

* [ ] ls -lh
* [ ] disk -u
* [ ] du -show
* [ ] df -h

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** df -h
💡 `df -h` reports filesystem space usage in a readable format.

</details>

---

### 18. How can a script efficiently count the number of occurrences of a keyword in a log file?

* [ ] grep word logfile | count
* [ ] find word logfile
* [ ] awk word logfile
* [ ] grep -c word logfile

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** grep -c word logfile
💡 The `-c` option outputs the count of matching lines.

</details>

---

### 19. Which command is most appropriate for identifying failed SSH login attempts?

* [ ] whoami
* [ ] top login
* [ ] cat /etc/passwd
* [ ] grep fail /var/log/auth.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** grep fail /var/log/auth.log
💡 Authentication failures are logged in `auth.log` on Debian-based systems.

</details>

---

### 20. Which utility allows periodic execution of a command to observe changes in file size or system output?

* [ ] ps
* [ ] diff
* [ ] find
* [ ] watch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** watch
💡 `watch` repeatedly runs a command and displays output changes over time.

</details>

---

### 21. What is the primary function of the `logger` command in Linux?

* [ ] Restart logging services
* [ ] Create log users
* [ ] Write custom messages to syslog
* [ ] View existing log files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Write custom messages to syslog
💡 `logger` integrates script output directly into the system logging framework.

</details>

---

### 22. A production script generates high-volume logs daily. What is the most reliable way to ensure logs are rotated safely?

* [ ] rm logfile periodically
* [ ] truncate logfile manually
* [ ] logflush
* [ ] Configure logrotate policies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configure logrotate policies
💡 `logrotate` ensures safe rotation, compression, and retention without data loss.

</details>

---

### 23. What is the effect of `trap 'cleanup' EXIT` in a Bash script?

* [ ] Terminates the script immediately
* [ ] Redirects exit logs
* [ ] Executes cleanup function upon script exit
* [ ] Captures system logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Executes cleanup function upon script exit
💡 `trap` ensures resource cleanup even during unexpected termination.

</details>

---

### 24. A script must continuously detect new log entries as they occur. Which approach is most effective?

* [ ] cat logfile
* [ ] ps | grep log
* [ ] while read logfile
* [ ] tail -f logfile within controlled logic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** tail -f logfile within controlled logic
💡 `tail -f` streams new entries, making it suitable for real-time monitoring.

</details>

---

### 25. To measure how long a script takes to execute for performance tuning, which method is preferred?

* [ ] uptime
* [ ] watch script
* [ ] count seconds manually
* [ ] time ./script.sh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** time ./script.sh
💡 `time` provides accurate execution duration and resource usage metrics.

</details>

---

### 26. Which practice best mitigates log injection attacks in scripts that log user-supplied input?

* [ ] Encrypting all logs
* [ ] Disabling stdout
* [ ] Using administrative privileges
* [ ] Validating and sanitizing input

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Validating and sanitizing input
💡 Input sanitization prevents attackers from injecting forged log entries.

</details>

---

### 27. Which command is most suitable for observing CPU usage trends of individual processes over time?

* [ ] uptime
* [ ] du -cpu
* [ ] loadmon
* [ ] top

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** top
💡 `top` dynamically tracks per-process CPU usage.

</details>

---

### 28. On most Debian-based Linux systems, which file records authentication-related events?

* [ ] /var/log/boot.log
* [ ] /var/log/cron
* [ ] /etc/log/users.log
* [ ] /var/log/auth.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/auth.log
💡 Authentication attempts and privilege escalations are logged here.

</details>

---

### 29. What is the most effective strategy to prevent disk exhaustion caused by uncontrolled log growth?

* [ ] Monitor logs manually
* [ ] Increase disk space only
* [ ] Disable logging
* [ ] Implement log rotation with size thresholds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Implement log rotation with size thresholds
💡 Proactive rotation ensures system stability and compliance.

</details>

---

### 30. When a script detects a critical security event in logs, what is the most appropriate response mechanism?

* [ ] Ignore the event
* [ ] Write output to /dev/null
* [ ] Pause script execution
* [ ] Send alerts via email or notification service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Send alerts via email or notification service
💡 Immediate alerts enable timely incident response and risk mitigation.

</details>

---
