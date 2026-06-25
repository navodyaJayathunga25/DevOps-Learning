# 📘 Virtual Machines (Part 1)

> **Topic:** Introduction to Virtual Machines & Virtualization

---

# What is a Virtual Machine (VM)?

A **Virtual Machine (VM)** is a software-based computer that behaves like a physical computer.

Each virtual machine has its own:

- CPU
- Memory (RAM)
- Storage
- Operating System
- Network

A VM runs independently, even though multiple VMs share the same physical server.

---

# Why Do We Need Virtual Machines?

Imagine a company buys a server with:

- 10 GB RAM

But one application only needs:

- 4 GB RAM

The remaining 6 GB of RAM is wasted.

Instead of buying another server, we can create multiple virtual machines on the same physical server and share its resources.

This process is called **Virtualization**.

### Benefits

- Better resource utilization
- Lower hardware cost
- Easier management
- Run multiple operating systems on one server

---

# What is Virtualization?

**Virtualization** is the process of dividing one physical server into multiple virtual machines.

Each virtual machine works like an independent computer.

```text
Physical Server
        │
        ▼
+--------------------+
|     Hypervisor     |
+--------------------+
│      │      │
▼      ▼      ▼
VM1    VM2    VM3
```

---

# What is a Hypervisor?

A **Hypervisor** is software that creates and manages Virtual Machines.

It allocates resources such as:

- CPU
- Memory
- Storage
- Network

to each VM.

Without a hypervisor, virtual machines cannot be created.

---

# Popular Hypervisors

- VMware
- Xen
- Microsoft Hyper-V
- KVM

---

# Characteristics of a Virtual Machine

Each VM has its own:

- Operating System
- CPU allocation
- RAM allocation
- Storage
- Network settings

Although VMs share the same physical hardware, they operate independently.

---

# Virtual Machine Workflow

```text
Physical Server
        │
        ▼
Hypervisor Installed
        │
        ▼
Create Virtual Machines
        │
        ▼
Install Operating System
        │
        ▼
Run Applications
```

---

# Virtual Machines in Cloud Computing

Cloud providers like AWS, Azure, and Google Cloud use virtualization in their data centers.

Example:

When you launch an **AWS EC2 Instance**, AWS creates a Virtual Machine for you using a hypervisor.

You don't need to buy or manage the physical server.

---

# Advantages of Virtual Machines

- Better hardware utilization
- Lower infrastructure cost
- Easy to create and delete
- Isolation between applications
- Supports multiple operating systems
- Easy backup and recovery
- Scalable

---

# Real-World Example

Suppose a physical server has:

- 16 GB RAM
- 8 CPU cores

Instead of running only one application, you can create:

| VM | RAM | CPU |
|----|-----|-----|
| VM 1 | 4 GB | 2 Cores |
| VM 2 | 4 GB | 2 Cores |
| VM 3 | 4 GB | 2 Cores |
| VM 4 | 4 GB | 2 Cores |

Each VM behaves like a separate computer while sharing the same physical hardware.

---

# Key Terms

| Term | Meaning |
|------|---------|
| Physical Server | The actual hardware machine |
| Virtual Machine (VM) | A software-based computer |
| Virtualization | Creating multiple VMs from one physical server |
| Hypervisor | Software that creates and manages VMs |
| EC2 | AWS Virtual Machine service |

---

# Interview Questions

### What is a Virtual Machine?

A Virtual Machine is a software-based computer that runs on a physical server using a hypervisor.

---

### What is Virtualization?

Virtualization is the process of creating multiple virtual machines from a single physical server.

---

### What is a Hypervisor?

A hypervisor is software that creates, manages, and allocates resources to virtual machines.

---

### Name some popular Hypervisors.

- VMware
- Xen
- Hyper-V
- KVM

---

# Summary

- A Virtual Machine is a software-based computer.
- Virtualization allows multiple VMs to share one physical server.
- A Hypervisor manages virtual machines.
- Cloud platforms like AWS use virtualization to provide services such as EC2.
- Virtual machines improve resource utilization and reduce hardware costs.
