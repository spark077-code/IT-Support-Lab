# 📜 Bash Scripting

> A beginner-friendly guide to Bash scripting for Linux automation, IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document introduces Bash scripting and explains how to automate repetitive tasks using shell scripts. It covers script creation, variables, user input, conditions, loops, functions, and practical examples.

---

# 📚 Table of Contents

1. What is Bash?
2. What is a Bash Script?
3. Creating Your First Script
4. Variables
5. User Input
6. Conditional Statements
7. Loops
8. Functions
9. Useful Bash Commands
10. Practical Lab
11. Best Practices
12. Common Mistakes
13. Interview Questions

---

# 🧠 What is Bash?

Bash (Bourne Again Shell) is the default command-line shell on many Linux distributions.

It allows users to:

- Execute commands
- Automate tasks
- Manage files
- Control processes
- Write shell scripts

---

# 📜 What is a Bash Script?

A Bash script is a text file containing Linux commands that are executed one after another.

Scripts help automate repetitive tasks and save time.

Example:

```bash
#!/bin/bash

echo "Hello, Linux!"
```

---

# 📝 Creating Your First Script

Create a new file.

```bash
nano hello.sh
```

Add the following content:

```bash
#!/bin/bash

echo "Welcome to Linux!"
```

Save the file.

Give execute permission.

```bash
chmod +x hello.sh
```

Run the script.

```bash
./hello.sh
```

---

# 📦 Variables

Create a variable.

```bash
name="Faisal"
```

Display the variable.

```bash
echo $name
```

Example:

```bash
#!/bin/bash

name="Faisal"

echo "Welcome $name"
```

---

# ⌨ User Input

Read input from the keyboard.

```bash
#!/bin/bash

echo "Enter your name"

read name

echo "Hello $name"
```

---

# 🔀 Conditional Statements

## if Statement

```bash
#!/bin/bash

number=10

if [ $number -gt 5 ]
then
    echo "Greater than 5"
fi
```

---

## if...else Statement

```bash
#!/bin/bash

number=3

if [ $number -gt 5 ]
then
    echo "Greater"
else
    echo "Smaller"
fi
```

---

# 🔁 Loops

## For Loop

```bash
for i in 1 2 3 4 5
do
    echo $i
done
```

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    ((count++))
done
```

---

# ⚙ Functions

Create a function.

```bash
greet() {
    echo "Welcome to Linux"
}

greet
```

---

# 💻 Useful Bash Commands

| Command | Purpose |
|----------|----------|
| echo | Display text |
| read | Accept user input |
| chmod | Change file permissions |
| date | Display current date |
| pwd | Show current directory |
| whoami | Show current user |
| hostname | Display system hostname |
| clear | Clear terminal |
| exit | Exit shell |

---

# 🛠 Practical Lab

## Task 1

Create a script named:

```bash
hello.sh
```

Print:

```text
Hello World
```

---

## Task 2

Create a variable named:

```text
course
```

Display:

```text
Linux Administration
```

---

## Task 3

Create a script that asks the user for their name.

Example Output

```text
Enter your name:

Faisal

Hello Faisal
```

---

## Task 4

Create a script that displays the current date.

```bash
date
```

---

## Task 5

Create a loop that prints numbers from 1 to 10.

---

## Task 6

Create a function that displays:

```text
Welcome to Bash Scripting
```

---

# 💡 Best Practices

- Always start scripts with the correct shebang (`#!/bin/bash`).
- Use meaningful variable names.
- Add comments to explain complex logic.
- Test scripts before using them in production.
- Keep scripts simple and readable.

---

# ⚠ Common Mistakes

❌ Forgetting to make the script executable.

```bash
chmod +x script.sh
```

❌ Running the script without `./`

```bash
./script.sh
```

❌ Missing spaces in `if` conditions.

❌ Using unclear variable names.



---

# 📖 References

- Bash Manual (`man bash`)
- GNU Bash Documentation
- Ubuntu Documentation
- Red Hat Documentation

---

## 🔗 Related Documents

- [Linux README](README.md)
- [Basic Commands](Basic-Commands.md)
- [File System](File-System.md)
- [Users and Groups](Users-and-Groups.md)
- [File Permissions](File-Permissions.md)
- [Package Management](Package-Management.md)
- [Process Management](Process-Management.md)
- [Networking](Networking.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
