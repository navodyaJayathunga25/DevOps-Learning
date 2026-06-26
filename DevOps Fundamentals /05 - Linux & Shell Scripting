# 🐧 Linux & Shell Scripting Notes

> Basic Linux concepts, architecture, shell scripting fundamentals, and commonly used commands.

---

# What is Linux?

Linux is an **open-source operating system** that acts as a bridge between the user, applications, and computer hardware.

## Why Linux?

- ✅ Free and open source
- ✅ Secure
- ✅ Fast and lightweight
- ✅ Stable and reliable
- ✅ Widely used in servers and cloud computing

### Popular Linux Distributions

- Ubuntu
- CentOS
- Debian
- Fedora
- Red Hat Enterprise Linux (RHEL)
- Amazon Linux

---

# Linux Architecture

```text
                User
                  │
        Applications / Software
                  │
        System Libraries
                  │
               Kernel
                  │
    CPU | Memory (RAM) | Disk | I/O
```

---

# What is the Kernel?

The **Kernel** is the core of the Linux operating system.

It connects software with computer hardware.

### Main Responsibilities

- Process Management
- Memory Management
- Device Management
- System Calls

---

# Shell

The **Shell** is a command-line interface that allows users to communicate with the Linux operating system.

```text
User
   │
Shell
   │
Linux Kernel
   │
Hardware
```

Examples of shells:

- Bash (Most common)
- Zsh
- Sh

---

# What is Shell Scripting?

A **Shell Script** is a file that contains multiple Linux commands.

Instead of executing commands one by one, the script runs them automatically.

### Benefits

- Automation
- Saves time
- Reduces manual work
- Minimizes human errors

---

# Create Files

Using `touch`

```bash
touch filename
```

Example

```bash
touch notes.txt
```

---

# Create and Edit Files Using vi

Open file

```bash
vi filename
```

Example

```bash
vi notes.txt
```

### Insert Mode

Press

```text
i
```

### Exit Insert Mode

Press

```text
Esc
```

### Save

```text
:w
```

### Save and Quit

```text
:wq
```

or

```text
ZZ
```

### Quit Without Saving

```text
:q!
```

---

# Display File Content

```bash
cat filename
```

Example

```bash
cat notes.txt
```

---

# Create Directory

```bash
mkdir foldername
```

Example

```bash
mkdir projects
```

---

# Remove File

```bash
rm filename
```

---

# Remove Directory

```bash
rm -rf foldername
```

> ⚠️ Use `rm -rf` carefully. It permanently deletes files and folders.

---

# Print Text

```bash
echo "Hello World"
```

---

# Check Current Directory

```bash
pwd
```

Example Output

```text
/home/ubuntu
```

---

# Change Directory

Move into a folder

```bash
cd foldername
```

Go back one directory

```bash
cd ..
```

Go back two directories

```bash
cd ../..
```

Go to home directory

```bash
cd ~
```

---

# List Files

```bash
ls
```

Detailed view

```bash
ls -ltr
```

Shows:

- Permissions
- Owner
- Group
- File Size
- Modified Time
- File Name

Example

```text
-rw-r--r-- 1 ubuntu ubuntu 4096 Jun 5 20:00 notes.txt
```

---

# Linux File Permissions

Example

```text
-rw-r--r--
```

Meaning

| Permission | Description |
|------------|-------------|
| r | Read |
| w | Write |
| x | Execute |

---

# Performance Commands

## Memory Usage

```bash
free -g
```

---

## Number of CPUs

```bash
nproc
```

---

## Disk Usage

```bash
df -h
```

---

## Monitor System

```bash
top
```

Displays:

- CPU Usage
- Memory Usage
- Running Processes

---

# SSH into a Linux Server

Example

```bash
ssh -i mykey.pem ubuntu@3.92.207.193
```

### Explanation

| Part | Description |
|------|-------------|
| ssh | Secure Shell command |
| -i | Identity file (Private Key) |
| mykey.pem | Private Key |
| ubuntu | Username |
| 3.92.207.193 | Server IP Address |

---

# Linux vs Shell Scripting

| Linux | Shell Scripting |
|--------|-----------------|
| Operating System | Automation using Linux commands |
| Manages hardware and software | Executes multiple commands automatically |
| Used to run applications | Used to automate repetitive tasks |

---

# Key Takeaways

- Linux is a powerful operating system widely used in cloud computing.
- The Kernel manages hardware resources.
- The Shell provides a command-line interface to Linux.
- Shell Scripts automate repetitive Linux tasks.
- Common Linux commands include `pwd`, `cd`, `ls`, `mkdir`, `rm`, `cat`, and `echo`.
- Monitoring commands such as `top`, `df -h`, `free -g`, and `nproc` help inspect system performance.
- SSH allows secure remote access to Linux servers.

---

# Interview Questions

## What is Linux?

Linux is an open-source operating system that manages computer hardware and software resources.

---

## What is the Kernel?

The Kernel is the core component of Linux that manages CPU, memory, devices, and system calls.

---

## What is the Shell?

The Shell is a command-line interface that allows users to interact with the Linux operating system.

---

## What is Shell Scripting?

Shell Scripting is the process of writing a sequence of Linux commands in a file to automate tasks.

---

## What is the difference between Linux and Shell Scripting?

Linux is an operating system, while Shell Scripting is a way to automate tasks by executing multiple Linux commands stored in a script.
