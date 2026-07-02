# 🛠 Linux Basics Troubleshooting Guide

This document contains common Linux issues that beginners and system administrators encounter while learning Linux.

Each scenario explains the problem, possible causes, diagnosis steps, solution, prevention, and interview tips.

---

## 📚 Estimated Completion Time

**45 Minutes**

---

# 🚨 Scenario 1 – Command Not Found

## ❌ Problem

You execute a command, but Linux displays:

```text
command not found
```

---

## 🔍 Possible Causes

- Command is typed incorrectly.
- Software is not installed.
- PATH environment variable is incorrect.

---

## 🛠 Diagnosis

Verify the command spelling.

Example:

```bash
pwd
```

instead of

```bash
pdw
```

Check whether the command exists:

```bash
which <command>
```

Example:

```bash
which git
```

---

## ✅ Solution

- Correct the spelling.
- Install the required package if missing.
- Verify the PATH variable if necessary.

---

## 🛡 Prevention

- Use **Tab Completion** whenever possible.
- Double-check command names before executing them.

---

## 🎯 Interview Tip

Always explain **how you diagnosed the issue**, not just how you fixed it.

---

# 🚨 Scenario 2 – No Such File or Directory

## ❌ Problem

Linux displays:

```text
No such file or directory
```

---

## 🔍 Possible Causes

- Incorrect file name.
- Incorrect directory.
- Typographical error.
- File does not exist.

---

## 🛠 Diagnosis

Check your current directory:

```bash
pwd
```

List files:

```bash
ls
```

---

## ✅ Solution

- Navigate to the correct directory.
- Correct the file or directory name.
- Create the file if required.

---

## 🛡 Prevention

Verify the directory using:

```bash
pwd
```

before accessing files.

---

## 🎯 Interview Tip

Many production issues are caused by incorrect file paths.

Always verify the current directory first.

---

# 🚨 Scenario 3 – Permission Denied

## ❌ Problem

Linux displays:

```text
Permission denied
```

---

## 🔍 Possible Causes

- Insufficient permissions.
- File ownership issue.
- Command requires elevated privileges.

---

## 🛠 Diagnosis

Check file permissions:

```bash
ls -l
```

Verify the current user:

```bash
whoami
```

---

## ✅ Solution

- Use the correct user account.
- Modify file permissions if appropriate.
- Use administrative privileges when required.

---

## 🛡 Prevention

Avoid granting excessive permissions.

Follow the **Principle of Least Privilege**.

---

## 🎯 Interview Tip

Do not immediately suggest changing permissions.

First identify **why** the permission issue occurred.

---

# 🚨 Scenario 4 – Wrong Directory

## ❌ Problem

Commands execute successfully but affect the wrong files.

---

## 🔍 Possible Causes

- Working in the wrong directory.
- Forgot to verify the current location.

---

## 🛠 Diagnosis

Run:

```bash
pwd
```

Then:

```bash
ls
```

---

## ✅ Solution

Navigate to the correct directory using:

```bash
cd
```

---

## 🛡 Prevention

Always verify your location before executing commands such as:

- rm
- mv
- cp

---

## 🎯 Interview Tip

Experienced Linux engineers verify their working directory before modifying production files.

---

# 🚨 Scenario 5 – Wrong User Logged In

## ❌ Problem

Administrative commands fail unexpectedly.

---

## 🔍 Possible Causes

- Logged in using the wrong account.
- Missing required privileges.

---

## 🛠 Diagnosis

Verify the current user:

```bash
whoami
```

Verify the hostname:

```bash
hostname
```

---

## ✅ Solution

Log in using the correct account or use appropriate administrative privileges.

---

## 🛡 Prevention

Always verify both the current user and the hostname before making system changes.

---

## 🎯 Interview Tip

Checking both **whoami** and **hostname** is a common production habit, especially when managing multiple servers.

---

# 🏁 Troubleshooting Checklist

Before making changes to any Linux system, verify:

- Current user
- Current directory
- Hostname
- File permissions
- Correct command syntax
- File or directory exists

Following this checklist helps prevent many common operational mistakes.