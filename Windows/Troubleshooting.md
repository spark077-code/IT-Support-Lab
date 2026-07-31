# 🛠 Windows Troubleshooting Guide

> A practical guide for diagnosing and resolving common Windows issues faced by IT Support Engineers.

---

# 📌 Objective

This document provides practical Windows troubleshooting techniques commonly used by IT Support Engineers to diagnose and resolve common Windows problems. It includes troubleshooting steps, useful commands, best practices, and interview-focused notes.

---

# 📚 Table of Contents

1. Troubleshooting Methodology
2. Slow Computer
3. No Internet Connection
4. Windows Update Issues
5. Blue Screen (BSOD)
6. Printer Problems
7. Disk Space Issues
8. High CPU / Memory Usage
9. Driver Issues
10. Startup Problems
11. Useful Troubleshooting Commands
12. Best Practices
13. Interview Questions

---

# 🧠 Troubleshooting Methodology

A professional IT Support Engineer never guesses.

Follow this process every time.

```
Identify the Problem
        │
        ▼
Gather Information
        │
        ▼
Identify Possible Causes
        │
        ▼
Test the Solution
        │
        ▼
Implement the Fix
        │
        ▼
Verify the Issue is Resolved
        │
        ▼
Document the Resolution
```

---

# 🐢 1. Slow Computer

## Possible Causes

- Too many startup applications
- Low disk space
- High CPU usage
- Low available RAM
- Malware infection
- Windows updates running
- Background applications

## Troubleshooting Steps

### Step 1

Restart the computer.

---

### Step 2

Open Task Manager.

```
Ctrl + Shift + Esc
```

Check

- CPU Usage
- Memory Usage
- Disk Usage

---

### Step 3

Disable unnecessary Startup Applications.

Task Manager

↓

Startup Apps

↓

Disable unnecessary programs.

---

### Step 4

Check available storage.

```
This PC
```

Ensure sufficient free space on the system drive.

---

### Step 5

Run System File Checker.

```cmd
sfc /scannow
```

---

### Step 6

Repair Windows Image.

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

---

### Step 7

Restart the computer.

---

# 🌐 2. No Internet Connection

## Check Physical Connection

✔ Ethernet cable

✔ Wi-Fi Enabled

✔ Router Power

✔ Airplane Mode Disabled

---

## Verify IP Address

```cmd
ipconfig
```

---

## Renew IP Address

```cmd
ipconfig /release

ipconfig /renew
```

---

## Flush DNS Cache

```cmd
ipconfig /flushdns
```

---

## Test Network Connectivity

```cmd
ping 8.8.8.8
```

---

## Test DNS

```cmd
nslookup google.com
```

---

## Trace Route

```cmd
tracert google.com
```

---

## Display Routing Table

```cmd
route print
```

---

# 💻 3. Windows Update Issues

## Common Problems

- Update Stuck
- Download Failed
- Installation Failed

## Solutions

Restart Windows.

Run Windows Update Troubleshooter.

Restart Windows Update Service.

Check Internet Connection.

---

# 🔵 4. Blue Screen (BSOD)

## Possible Causes

- Driver Failure
- RAM Issues
- Corrupted System Files
- Hardware Failure

## Troubleshooting

Run

```cmd
sfc /scannow
```

Repair Windows

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

Open Event Viewer

```
eventvwr.msc
```

Check Device Manager.

```
devmgmt.msc
```

---

# 🖨 5. Printer Problems

## Checklist

✔ Printer Powered On

✔ Connected to Network

✔ Default Printer Selected

✔ Print Queue Cleared

Restart Print Spooler

```
services.msc
```

Restart

```
Print Spooler
```

---

# 💾 6. Disk Space Issues

## Check Storage

Settings

↓

Storage

Run Disk Cleanup

```cmd
cleanmgr
```

Delete

- Temporary Files
- Recycle Bin
- Old Downloads

---

# ⚡ 7. High CPU / Memory Usage

Open

```
Task Manager
```

Sort Processes by

- CPU
- Memory

Close unnecessary applications.

Disable unwanted Startup Apps.

---

# 🔧 8. Driver Problems

Open

```
devmgmt.msc
```

Look for

⚠ Yellow Warning Icons

Options

- Update Driver
- Roll Back Driver
- Uninstall Device
- Scan for Hardware Changes

---

# 🚀 9. Startup Problems

Run

```cmd
msconfig
```

Check

- Startup Programs
- Boot Options

Use Startup Repair if Windows fails to boot.

---

# 💻 Useful Troubleshooting Commands

| Command | Description |
|----------|-------------|
| ipconfig | Display IP configuration |
| ping | Test connectivity |
| tracert | Trace network route |
| nslookup | Test DNS |
| route print | View routing table |
| netstat | Display network connections |
| tasklist | View running processes |
| taskkill | End a process |
| systeminfo | Display system information |
| hostname | Display computer name |
| whoami | Display current user |
| sfc /scannow | Repair system files |
| DISM | Repair Windows image |
| chkdsk | Check disk errors |
| cleanmgr | Disk Cleanup |
| eventvwr.msc | Open Event Viewer |
| devmgmt.msc | Open Device Manager |
| services.msc | Open Services |
| msconfig | System Configuration |

---

# ✅ Best Practices

- Restart before troubleshooting.
- Check physical connections.
- Read error messages carefully.
- Verify recent changes.
- Test after every fix.
- Keep Windows updated.
- Create restore points before major changes.
- Document every issue and solution.

---

# 🎯 Interview Questions

### What is troubleshooting?

### How do you troubleshoot a slow Windows computer?

### How do you troubleshoot internet connectivity issues?

### Difference between Ping and Tracert?

### What is the purpose of SFC?

### What is DISM?

### What is Event Viewer?

### What is Device Manager?

### How do you restart the Print Spooler service?

### Which command displays IP configuration?

### Which command checks disk errors?

### Which command repairs corrupted Windows system files?

---

# 📖 References

- Microsoft Learn
- Microsoft Windows Documentation
- Windows Command Line Documentation

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
