 # 💻 Linux Commands Reference

This document contains all Linux commands covered in the **Linux Basics** module.

Each command includes its purpose, syntax, practical examples, expected output, real-world usage, interview questions, common mistakes, and Sensei tips.

---

## 📚 Estimated Reading Time

**30–40 Minutes**

---

## 📋 Command Index

1. pwd
2. ls
3. cd
4. mkdir
5. touch
6. clear
7. whoami
8. hostname
9. date
10. cal

---

## 1. pwd

### 📖 Purpose

Displays the absolute path of the current working directory.

---

### 📝 Syntax

```bash
pwd
```

---

### 💻 Example

```bash
pwd
```

---

### 📤 Example Output

```text
/home/vijay/linux-for-devops
```

---

### 🔍 Explanation

The `pwd` command prints the full path of the directory you are currently working in.

---

### 🌍 Real-World Usage

Before creating, deleting, copying, or modifying files, DevOps engineers often run `pwd` to verify they are working in the correct directory.

---

### ⚠️ Common Mistakes

Many beginners confuse:

```bash
pwd
```

with

```bash
ls
```

Remember:

- `pwd` → Where am I?
- `ls` → What is inside this directory?

---

### 🎯 Interview Question

**What is the difference between `pwd` and `ls`?**

**Answer:**

- `pwd` displays the current working directory.
- `ls` displays the contents of the current directory.

---

### 🧠 Sensei Tip

Always verify your location using `pwd` before running commands such as `rm`, `mv`, or `cp` to avoid accidental changes in the wrong directory.

---

## 2. ls

### 📖 Purpose

Lists the contents of the current directory.

---

### 📝 Syntax

```bash
ls
```

---

### 💻 Example

```bash
ls
```

---

### 📤 Example Output

```text
README.md
01-linux-basics
02-file-system
03-file-permissions
```

---

### 🔍 Explanation

The `ls` command displays files and directories in your current location.

Common options include:

- `ls -l` → Long listing format
- `ls -a` → Show hidden files
- `ls -la` → Long listing including hidden files
- `ls -lh` → Human-readable file sizes

---

### 🌍 Real-World Usage

Engineers use `ls` constantly to verify files before editing, copying, deploying, or deleting them.

---

### ⚠️ Common Mistakes

Running `ls` without checking the current directory.

Use:

```bash
pwd
```

first if you are unsure of your location.

---

### 🎯 Interview Question

**What is the difference between `ls` and `ls -la`?**

---

### 🧠 Sensei Tip

`ls -la` is one of the most frequently used commands in Linux administration because it shows permissions, ownership, and hidden files.

---

## 3. cd

### 📖 Purpose

Changes the current working directory.

---

### 📝 Syntax

```bash
cd <directory_name>
```

---

### 💻 Example

```bash
cd linux-for-devops
```

---

### 📤 Example Output

No output is displayed if the command executes successfully.

---

### 🔍 Explanation

The `cd` command allows you to move between directories.

Useful variations:

```bash
cd ..
```

Move one directory up.

```bash
cd ~
```

Go to the home directory.

```bash
cd -
```

Return to the previous directory.

---

### 🌍 Real-World Usage

Engineers frequently navigate between project directories, configuration files, log folders, and deployment scripts.

---

### ⚠️ Common Mistakes

Trying to enter a directory that does not exist.

Always verify directory names using:

```bash
ls
```

---

### 🎯 Interview Question

**What does `cd ..` do?**

---

### 🧠 Sensei Tip

Use **Tab Completion** while typing directory names to improve speed and reduce typing mistakes.

---
## 4. mkdir

### 📖 Purpose

Creates one or more new directories (folders).

---

### 📝 Syntax

```bash
mkdir <directory_name>
```

---

### 💻 Example

```bash
mkdir linux-project
```

Create multiple directories:

```bash
mkdir project1 project2 project3
```

Create nested directories:

```bash
mkdir -p projects/devops/linux
```

---

### 📤 Example Output

No output is displayed if the command executes successfully.

---

### 🔍 Explanation

The `mkdir` command creates new directories in the current location.

The `-p` option creates parent directories automatically if they do not already exist.

---

### 🌍 Real-World Usage

DevOps Engineers use `mkdir` to organize:

- Project folders
- Log directories
- Backup folders
- Application directories
- Configuration directories

---

### ⚠️ Common Mistakes

Trying to create a directory that already exists.

Example:

```bash
mkdir logs
```

If `logs` already exists, Linux displays an error.

---

### 🎯 Interview Question

**What is the purpose of the `-p` option in `mkdir`?**

**Answer:**

It creates parent directories automatically and does not return an error if intermediate directories do not exist.

---

### 🧠 Sensei Tip

Use:

```bash
mkdir -p
```

instead of creating each directory one by one.

It saves time and is commonly used in shell scripts.

---

## 5. touch

### 📖 Purpose

Creates an empty file or updates the timestamp of an existing file.

---

### 📝 Syntax

```bash
touch <file_name>
```

---

### 💻 Example

Create one file:

```bash
touch notes.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

### 📤 Example Output

No output is displayed if the command executes successfully.

---

### 🔍 Explanation

If the file does not exist, `touch` creates it.

If the file already exists, it updates the file's access and modification timestamps.

---

### 🌍 Real-World Usage

Engineers use `touch` to create:

- Configuration files
- Log files
- Documentation
- Placeholder files

---

### ⚠️ Common Mistakes

Many beginners expect `touch` to open a file for editing.

It only creates the file.

Use editors like:

- nano
- vim
- vi

to edit file contents.

---

### 🎯 Interview Question

**Does `touch` always create a new file?**

**Answer:**

No.

If the file already exists, it only updates its timestamps.

---

### 🧠 Sensei Tip

Creating multiple files with a single command saves time:

```bash
touch app.log error.log access.log
```

---

## 6. clear

### 📖 Purpose

Clears the terminal screen.

---

### 📝 Syntax

```bash
clear
```

---

### 💻 Example

```bash
clear
```

---

### 📤 Example Output

The terminal screen is cleared, but previous commands remain in the terminal history.

---

### 🔍 Explanation

The `clear` command removes visible text from the terminal window, making it easier to continue working.

It does **not** delete command history.

---

### 🌍 Real-World Usage

System Administrators and DevOps Engineers frequently use `clear` during troubleshooting or demonstrations to keep the terminal clean and readable.

---

### ⚠️ Common Mistakes

Many beginners think `clear` deletes command history.

It only clears the visible screen.

Use:

```bash
history
```

to view previous commands.

---

### 🎯 Interview Question

**Does the `clear` command remove terminal history?**

**Answer:**

No.

It only clears the visible terminal screen.

---

### 🧠 Sensei Tip

Instead of typing:

```bash
clear
```

you can usually press:

```text
Ctrl + L
```

This is faster and commonly used by Linux professionals.

---
## 7. whoami

### 📖 Purpose

Displays the username of the currently logged-in user.

---

### 📝 Syntax

```bash
whoami
```

---

### 💻 Example

```bash
whoami
```

---

### 📤 Example Output

```text
vijay
```

---

### 🔍 Explanation

The `whoami` command displays the effective username of the current user.

It is useful for confirming which account is executing commands, especially after switching users using commands like `su` or `sudo`.

---

### 🌍 Real-World Usage

System Administrators and DevOps Engineers often use `whoami` before performing administrative tasks to verify they are using the correct account.

---

### ⚠️ Common Mistakes

Many beginners think `whoami` shows all logged-in users.

It only displays the current user.

To see all logged-in users, commands such as `who` or `w` are used.

---

### 🎯 Interview Question

**What is the difference between `whoami` and `who`?**

**Answer:**

- `whoami` displays the current user.
- `who` displays all users currently logged into the system.

---

### 🧠 Sensei Tip

Before making system changes, always verify the current user with:

```bash
whoami
```

This helps prevent accidental actions using the wrong account.

---

## 8. hostname

### 📖 Purpose

Displays or sets the system's hostname.

---

### 📝 Syntax

```bash
hostname
```

---

### 💻 Example

```bash
hostname
```

---

### 📤 Example Output

```text
devops-server
```

---

### 🔍 Explanation

A hostname is the unique name assigned to a computer or server on a network.

It helps identify systems during administration, monitoring, and troubleshooting.

---

### 🌍 Real-World Usage

Cloud Engineers use the hostname to identify Linux servers running in environments such as AWS, Azure, or Google Cloud.

For example:

- web-server-01
- database-server
- jenkins-master
- monitoring-node

---

### ⚠️ Common Mistakes

Many beginners confuse the hostname with an IP address.

A hostname is a readable system name.

An IP address identifies the network location.

---

### 🎯 Interview Question

**What is a hostname?**

**Answer:**

A hostname is the unique name assigned to a computer or server that helps identify it on a network.

---

### 🧠 Sensei Tip

Use meaningful hostnames in production.

Example:

```
web-prod-01
db-prod-01
jenkins-master
```

Avoid names like:

```
server1
linux
test
```

Meaningful hostnames make troubleshooting much easier.

---

## 9. date

### 📖 Purpose

Displays or sets the current system date and time.

---

### 📝 Syntax

```bash
date
```

---

### 💻 Example

```bash
date
```

---

### 📤 Example Output

```text
Wed Jul 02 10:30:15 IST 2026
```

---

### 🔍 Explanation

The `date` command displays the current system date, time, and time zone.

It is useful for verifying timestamps, checking server time, and troubleshooting time-related issues.

---

### 🌍 Real-World Usage

Engineers use `date` when:

- Checking server time
- Investigating log timestamps
- Verifying scheduled jobs
- Troubleshooting time synchronization

---

### ⚠️ Common Mistakes

Many beginners assume the displayed time is always correct.

If the server time is incorrect, logs, backups, and scheduled jobs can be affected.

---

### 🎯 Interview Question

**Why is the `date` command important in production?**

**Answer:**

It helps verify system time, which is essential for accurate logs, monitoring, scheduling, and troubleshooting.

---

### 🧠 Sensei Tip

When troubleshooting application issues, always compare log timestamps with the output of:

```bash
date
```

Incorrect system time can cause misleading logs.

---

## 10. cal

### 📖 Purpose

Displays a calendar in the terminal.

---

### 📝 Syntax

```bash
cal
```

---

### 💻 Example

```bash
cal
```

---

### 📤 Example Output

```text
     July 2026
Su Mo Tu We Th Fr Sa
          1  2  3  4
5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31
```

---

### 🔍 Explanation

The `cal` command displays the current month's calendar.

It can also display calendars for specific months or years.

---

### 🌍 Real-World Usage

Administrators use `cal` to quickly check dates while planning maintenance windows, deployments, or scheduled activities.

---

### ⚠️ Common Mistakes

Some minimal Linux distributions may not include the `cal` command by default.

In such cases, it can usually be installed through the package manager.

---

### 🎯 Interview Question

**Does every Linux distribution include the `cal` command by default?**

**Answer:**

No.

Some minimal distributions do not install it by default.

---

### 🧠 Sensei Tip

Although `cal` is a simple utility, it is still useful during maintenance planning and scheduling activities.

---