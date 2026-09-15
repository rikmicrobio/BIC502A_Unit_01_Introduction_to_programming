<img width="400" height="300" alt="Image" src="https://github.com/user-attachments/assets/79525595-6240-436b-a831-2ddfcef53df8" />

# Unit I: Navigating a Linux Environment

## BTE608A — Programming / Bioinformatics Practical

This practical introduces the basic Linux environment needed for bioinformatics work.

The goal is simple: by the end of this unit, you should be comfortable using the terminal to navigate folders, create and manage files, and execute basic commands.

---

## Learning Objectives

By the end of this unit, you should be able to:

- Open and use an Ubuntu/Linux terminal
- Navigate between directories
- Find your current location
- List files and directories
- Create new files and directories
- Copy files and directories
- Move and rename files and directories
- Remove files and directories
- Execute basic programs from the terminal

---
# Typpe this command:
```text
tree -d -L 3 /
```
or
```text
find / -maxdepth 1 -type d -not -path '*/.*' | sort
```

<img width="1123" height="611" alt="Image" src="https://github.com/user-attachments/assets/f420b083-e242-4525-9ad2-41d916c4e4b3" />


# Linux File System Hierarchy

The **Linux file system hierarchy** provides a standardized way of organizing files, programs, configuration files, libraries, and system data. Understanding this structure is essential for navigating Linux, installing software, managing files, configuring applications, and troubleshooting system problems.

Unlike Windows, where different drives such as `C:` and `D:` are commonly used, Linux organizes everything under a single **root directory** `/`. All other directories branch from this root.

---

## Key Linux Directories

### 1. `/bin` — Essential User Commands

The `/bin` directory contains essential executable programs required for basic Linux operations.

Examples:

```text
/bin/ls
/bin/cp
/bin/mv
/bin/cat
```

These commands are commonly used for navigating and manipulating files.

> **Think:** `/bin` → Essential commands

---

### 2. `/sbin` — System Administration Commands

The `/sbin` directory contains programs mainly used for **system administration and maintenance**.

Examples include commands for managing disks, filesystems, networking, and system services.

```text
/sbin/reboot
/sbin/mount
/sbin/fsck
```

Many of these commands require administrator (`root`) privileges.

> **Think:** `/sbin` → System administration

---

### 3. `/etc` — System Configuration

The `/etc` directory contains **system-wide configuration files**.

Important examples include:

```text
/etc/passwd     → User account information
/etc/hosts      → Hostname and IP mapping
/etc/fstab      → Filesystem mount configuration
```

System administrators frequently work with files in `/etc` when configuring Linux services and applications.

> **Think:** `/etc` → Configuration

---

### 4. `/home` — User Files

The `/home` directory contains the personal directories of regular users.

For example:

```text
/home/student1
/home/student2
/home/researcher
```

Each user can store their own documents, scripts, datasets, projects, and configuration files here.

For a bioinformatics workstation, a user's directory might contain:

```text
/home/student/
├── projects/
├── scripts/
├── data/
└── results/
```

> **Think:** `/home` → User's personal workspace

---

### 5. `/lib` and `/lib64` — System Libraries

These directories contain **shared libraries** required by system programs and applications.

Linux libraries are similar in concept to `.dll` files in Windows.

Examples:

```text
/lib
/lib64
```

On modern Linux distributions, the exact organization can differ because many systems use a unified `/usr` layout.

> **Think:** `/lib` → Libraries required by programs

---

### 6. `/opt` — Optional and Third-Party Software

The `/opt` directory is commonly used for **optional or third-party software** that is installed separately from the main operating system.

For example:

```text
/opt/bioinformatics/
/opt/tools/
/opt/software/
```

A bioinformatics workstation might therefore have:

```text
/opt/bioinformatics/
├── bin/
├── tools/
├── databases/
└── software/
```

This makes `/opt` particularly useful for organizing manually installed scientific and bioinformatics software.

> **Think:** `/opt` → Optional/third-party software

---

### 7. `/tmp` — Temporary Files

The `/tmp` directory is used by users and applications to store **temporary files**.

For example:

```text
/tmp/analysis.txt
/tmp/program_output
```

Files in `/tmp` should not be considered permanent storage. Depending on the Linux distribution and configuration, temporary files may be removed automatically, including during or after a reboot.

> **Think:** `/tmp` → Temporary workspace

---

### 8. `/usr` — System Software and Shared Resources

The `/usr` directory contains a large portion of the operating system's **applications, programs, libraries, and shared data**.

Important subdirectories include:

```text
/usr/bin       → Programs and commands
/usr/lib       → Libraries
/usr/share     → Architecture-independent shared data
```

Many applications installed through the Linux package manager are placed under `/usr`.

> **Think:** `/usr` → Installed system software

---

### 9. `/var` — Changing Data and Logs

The `/var` directory contains data that **changes while the system is running**.

Important examples include:

```text
/var/log       → System and application logs
/var/cache     → Cached data
/var/spool     → Queues and scheduled data
```

System administrators often inspect `/var/log` when troubleshooting problems.

> **Think:** `/var` → Variable/changing data

---

# Quick Revision Table

| Directory | Main Purpose | Remember It As |
|---|---|---|
| `/bin` | Essential commands | **Commands** |
| `/sbin` | System administration commands | **Administration** |
| `/etc` | Configuration files | **Configuration** |
| `/home` | User files and projects | **Users** |
| `/lib`, `/lib64` | Shared libraries | **Libraries** |
| `/opt` | Optional/third-party software | **Software** |
| `/tmp` | Temporary files | **Temporary** |
| `/usr` | Programs, libraries, shared resources | **System software** |
| `/var` | Logs and changing data | **Variable data** |

---

# The Big Picture

A simple way to remember the Linux filesystem is:

```text
/
├── etc/       → Configuration
├── bin/       → Essential commands
├── sbin/      → Administration
├── usr/       → Installed software
├── lib/       → Libraries
├── opt/       → Third-party software
├── home/      → User files
├── tmp/       → Temporary files
└── var/       → Logs and changing data
```

---

## Key Takeaway

**Linux organizes everything under `/`, the root directory.**

Each major directory has a specific role, making it easier to locate:

- Configuration files
- Programs and commands
- Shared libraries
- User data
- Third-party software
- Temporary files
- System logs

For **bioinformatics users**, understanding `/home`, `/opt`, `/usr`, `/etc`, and `/var` is especially useful because these locations frequently appear when:

- Installing software
- Setting environment variables
- Managing permissions
- Running analysis pipelines
- Working with databases
- Troubleshooting computational tools

## 1. The Linux Terminal

The terminal allows us to interact with the operating system using commands.

A typical command looks like:

```bash
command
```

For example:

```bash
pwd
```

The terminal will execute the command and display the result.

> **Important:** Linux commands are case-sensitive.  
> `ls` and `LS` are different commands.

---

## 2. Navigating the File System

### `pwd` — Where am I?

```bash
pwd
```

Displays your current working directory.

### `ls` — What is here?

```bash
ls
```

Lists the files and directories in the current location.

Useful variations:

```bash
ls -l
ls -a
```

### `cd` — Move between directories

```bash
cd directory_name
```

Move into a directory.

Go to the parent directory:

```bash
cd ..
```

Return to your home directory:

```bash
cd ~
```

---

## 3. Creating Files and Directories

### `mkdir` — Create a directory

```bash
mkdir bioinformatics
```

Create a directory inside another directory:

```bash
mkdir bioinformatics/practical
```

### `touch` — Create an empty file

```bash
touch notes.txt
```

Check that it was created:

```bash
ls
```

---

## 4. Copying Files and Directories

### `cp` — Copy a file

```bash
cp notes.txt notes_backup.txt
```

Copy a file into another directory:

```bash
cp notes.txt bioinformatics/
```

To copy a directory and its contents:

```bash
cp -r bioinformatics backup
```

---

## 5. Moving and Renaming

### `mv` — Rename a file

```bash
mv notes.txt linux_notes.txt
```

Move a file to another directory:

```bash
mv linux_notes.txt bioinformatics/
```

The same command is used for both **moving** and **renaming**.

---

## 6. Removing Files and Directories

### `rm` — Remove a file

```bash
rm notes.txt
```

Remove a directory and its contents:

```bash
rm -r old_folder
```

> ⚠️ **Be careful with `rm`.** Deleted files are generally not moved to a recycle bin.

---

## 7. Mini Practical

Create the following directory structure:

```text
BTE608A_Unit1/
├── notes/
├── data/
└── backup/
```

Use the terminal to create it.

Then create these files:

```text
notes/linux_commands.txt
data/sample.txt
```

Copy `sample.txt` into `backup/`.

Rename:

```text
sample.txt
```

to:

```text
sample_data.txt
```

Finally, remove the original empty directory or file when instructed by your instructor.

---

## 8. Practice Questions

### Exercise 1

Find your current directory.

```bash
pwd
```

### Exercise 2

List all files, including hidden files.

```bash
ls -a
```

### Exercise 3

Create a directory called:

```text
unit1
```

### Exercise 4

Inside `unit1`, create:

```text
data
scripts
results
```

### Exercise 5

Create an empty file called:

```text
student_notes.txt
```

### Exercise 6

Copy `student_notes.txt` into the `data` directory.

### Exercise 7

Rename `student_notes.txt` to:

```text
linux_notes.txt
```

### Exercise 8

Move `linux_notes.txt` into the `notes` directory.

---

## 9. Final Check ✅

Before completing Unit I, you should be comfortable with:

```text
☑ pwd
☑ ls
☑ cd
☑ mkdir
☑ touch
☑ cp
☑ mv
☑ rm
```

These commands form the basic foundation for working with Linux in bioinformatics.

---

## What Comes Next?

In **Unit II**, we will learn how to view and manipulate the contents of files using commands such as:

```text
cat
less
more
head
tail
grep
cut
paste
sed
awk
```

We will also learn about **piping and writing files using Bash**.



----
try solving this problem:
As a question for students

### Q. Write a single Linux command to create a directory bioinformatics containing a subdirectory practical, and create an empty file file.txt inside practical.
### Q: how && is different from |?
