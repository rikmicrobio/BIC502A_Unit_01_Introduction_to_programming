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
<img width="1123" height="611" alt="Image" src="https://github.com/user-attachments/assets/f420b083-e242-4525-9ad2-41d916c4e4b3" />
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
