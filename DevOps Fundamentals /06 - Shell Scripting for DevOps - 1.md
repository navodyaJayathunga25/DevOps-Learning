# 🐚 Shell Scripting for DevOps

> Learn the fundamentals of Shell Scripting, file permissions, script execution, and automation in Linux.

---

# What is Shell Scripting?

Shell Scripting is the process of writing multiple Linux commands into a single file so they can be executed automatically.

Instead of typing commands one by one, a script performs the tasks for you.

## Benefits

- Automates repetitive tasks
- Reduces manual work
- Saves time
- Minimizes human errors
- Improves consistency

---

# Creating a Shell Script

Create a new file.

```bash
touch first-script.sh
```

or

```bash
vi first-script.sh
```

---

# View Command Documentation

To see the manual page of a command:

```bash
man ls
```

Example:

```bash
man chmod
```

---

# Default Permission of a New File

When a file is created, the default permission is usually:

```text
-rw-r--r--
```

Numeric representation:

```text
644
```

Meaning:

| User | Permission |
|------|------------|
| Owner | Read + Write |
| Group | Read |
| Others | Read |

---

# The Shebang

Every shell script should start with a **Shebang**.

Example:

```bash
#!/bin/bash
```

The shebang tells Linux which interpreter should execute the script.

Common interpreters:

```text
#!/bin/bash
#!/bin/sh
#!/bin/dash
#!/bin/ksh
```

The most commonly used interpreter is:

```text
#!/bin/bash
```

---

# Sample Shell Script

```bash
#!/bin/bash

echo "Hello DevOps"

mkdir Demo

touch file1.txt

touch file2.txt
```

---

# File Permissions

Linux does **not** execute files by default.

You must grant execute permission.

Example:

```bash
chmod +x first-script.sh
```

or

```bash
chmod 777 first-script.sh
```

---

# chmod

The `chmod` command changes file permissions.

Syntax

```bash
chmod permission filename
```

Example

```bash
chmod 755 script.sh
```

---

# Permission Numbers

| Number | Permission |
|---------|------------|
| 4 | Read (r) |
| 2 | Write (w) |
| 1 | Execute (x) |

Examples

| Value | Meaning |
|-------|---------|
| 7 | Read + Write + Execute |
| 6 | Read + Write |
| 5 | Read + Execute |
| 4 | Read Only |

---

# Permission Groups

Linux permissions are divided into three groups.

```text
Owner
Group
Others
```

Example:

```text
755
```

Means

```text
Owner  -> 7 (rwx)

Group  -> 5 (r-x)

Others -> 5 (r-x)
```

---

# Execute a Script

Method 1

```bash
./first-script.sh
```

Method 2

```bash
sh first-script.sh
```

Method 3

```bash
bash first-script.sh
```

---

# Shell Script Example

```bash
#!/bin/bash

echo "Creating Project"

mkdir DevOps

touch README.md

echo "Project Created Successfully"
```

---

# Common DevOps Uses

Shell scripting is commonly used for:

- Infrastructure maintenance
- Server administration
- Software installation
- Backup automation
- Log collection
- Health checks
- Deployment automation
- Configuration management

---

# Example DevOps Scenario

Imagine a DevOps engineer manages **1000 Linux servers**.

Instead of manually logging into every server,

they can write one shell script to:

- Check disk usage
- Check memory usage
- Restart services
- Install packages
- Collect logs

The same script can run on every server automatically.

---

# Shell Script + Git

A common practice is to store shell scripts inside a Git repository.

Benefits

- Version Control
- Easy Collaboration
- Backup
- Reusable Automation

---

# Why Use Shell Scripting if Automation Tools Exist?

Tools like:

- Ansible
- Terraform
- Jenkins

can automate many tasks.

However, shell scripting is still important because:

- Many automation tools execute shell commands internally.
- Quick administrative tasks are easier with shell scripts.
- Existing systems often rely on shell scripts.
- Understanding shell scripting helps troubleshoot automation failures.

---

# Stop a Running Script

Press

```text
Ctrl + C
```

This sends an interrupt signal and terminates the running script.

---

# Best Practices

- Always begin scripts with a shebang (`#!/bin/bash`)
- Use meaningful file names
- Add comments to explain your code
- Test scripts before running them in production
- Grant only the permissions required

---

# Interview Questions

## What is Shell Scripting?

Shell scripting is the process of writing multiple Linux commands into a file and executing them automatically.

---

## What is a Shebang?

A shebang (`#!/bin/bash`) specifies which interpreter should execute the script.

---

## Why is `chmod +x` required?

Linux does not execute files by default. The execute permission must be granted before a script can be run directly.

---

## What does `chmod 755 script.sh` mean?

- Owner: Read, Write, Execute
- Group: Read, Execute
- Others: Read, Execute

---

## Why do DevOps Engineers use Shell Scripts?

Shell scripts automate repetitive tasks such as deployments, server configuration, monitoring, backups, and system administration.
