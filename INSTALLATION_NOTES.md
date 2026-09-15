# Installation Notes

## Unit I — Navigating a Linux Environment

Before starting Unit I, everyone should have access to an Ubuntu/Linux terminal.

There are two common options.

---

## Option 1: Ubuntu / Linux

If you already use Ubuntu or another Linux distribution, you can use your existing terminal.

Open the **Terminal** application and run:

```bash
uname -a
```

Then check your home directory:

```bash
pwd
```

If these commands work, you are ready to begin.

---

## Option 2: Windows + WSL

If you are using Windows, we recommend using **Windows Subsystem for Linux (WSL)** with Ubuntu.

Open **PowerShell as Administrator** and run:

```powershell
wsl --install
```

Restart your computer if Windows asks you to do so.

After restarting:

1. Open **Ubuntu** from the Windows Start Menu.
2. Complete the Ubuntu username and password setup.
3. Open the Ubuntu terminal.

Check that WSL/Ubuntu is working:

```bash
uname -a
```

Then:

```bash
pwd
```

---

## Quick Test

Run the following commands one by one:

```bash
pwd
ls
mkdir unit1_test
cd unit1_test
touch test.txt
ls
cd ..
rm -r unit1_test
```

If these commands run without problems, your basic Linux environment is ready.

---

## Important

### Linux commands are case-sensitive

For example:

```bash
ls
```

is different from:

```bash
LS
```

### Be careful with `rm`

The command:

```bash
rm
```

removes files. Always check what you are deleting before pressing Enter.

---

## Ready? 🚀

Once Ubuntu/Linux or WSL is working, move on to:

**`README.md` → Unit I: Navigating a Linux Environment**
