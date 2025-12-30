# 2H : 50m
**Operating System (OS)**

Basically, two things want to communicate with the hardware:

1. The **user (human)**
2. **Applications** like YouTube, browsers, or games.

Directly using hardware (like hard disk, memory, or CPU) is very difficult. People couldn’t easily tell the computer how to run a program or show “Hello World”.

That’s why the **Operating System (OS)** was introduced.

Examples of operating systems:

* Linux
* Unix
* Windows
* macOS

First, **Unix** was created.
Later, **Linux** was developed based on Unix.

At that time, it was still difficult for users and applications to communicate with the system because everything was text-based.

So, **Microsoft introduced Windows**, which provided a **GUI (Graphical User Interface)**, making computers easy to use with a mouse, icons, and windows.

---

### ✅ Even Shorter Simple Version (Very Easy)

An **Operating System** helps:

* The **user** talk to the computer
* The **applications** use hardware

Without an OS, using hardware is very hard.

Unix came first,
then Linux,
and later Windows came with a **GUI** to make computers easy for everyone.



We talked about what an operating system is. Now let’s talk about which operating system is famous.
Basically, Linux is a very famous operating system because it is open source and free. Most companies prefer it because it is secure, and the community continuously improves it.
Now let’s talk about Linux contributions. Many companies contribute to Linux, such as Ubuntu, Red Hat, and Debian. These companies add extra features on top of Linux. Among them, Ubuntu is the most popular.


---

**Using Linux on Windows**
We usually use **Ubuntu**. If we want to use Linux on Windows, we have **two options**:

1. **WSL (Windows Subsystem for Linux)**
2. **Docker**

---

**What is a Package Manager in Ubuntu?**
A **package manager** is used in Ubuntu to **install, upgrade, maintain, and remove software**.

* In Ubuntu, we use **`apt`** as the package manager.
* For example, when we run `apt install python`, it reads the **stored package information** and installs Python from a **trusted source/website**.
* If the software is not available via `apt`, we can install it **manually** or using other tools like **WGL**.

---
============================================================================================================
Now let’s talk about the **main path** in Linux.

When you see something like this:

```
root@hostname:~$
```

There are two important parts here:

1. **root** → this is the *user* (the account currently logged in)
2. **~ (tilde)** → this represents the *home directory*

The **home directory** is basically the user’s personal folder, for example:

```
/home/userName
```

Every user gets their own home directory.

You can check your current location using the `pwd` command, which shows your **path**.

Think of it like **Google Drive**:
When you create a new account, it starts with a root folder. After that, you create your own folders and organize things the way you want.

---

========================================================================================================================
Apart from the **CLI shell**, the folders we see—especially the **main system folders**—are part of the **Operating System**, not the home directory.

The **home directory** is only for **user files**, while **system libraries and system utilities** are stored in **system directories**, not inside the home directory.

When we run:

```bash
cd /
```

it takes us directly to the **root directory** (`/`), which is the top-level directory of Linux.

---

### Important System Directories

#### 1. `/sbin`

* `/sbin` stands for **system binaries**
* It contains commands and binary files used to **manage the system**
* These commands are mostly for the **administrator (root user)**
* Example:

  * `adduser`
  * `reboot`
  * `shutdown`

✔️ Your understanding here is correct.

---

#### 2. `/boot`

* `/boot` is used during **system startup and restart**
* It contains files required to **boot the operating system**
* Examples:

  * kernel files
  * bootloader files

✔️ Correct.

---

#### 3. `/bin`

* `/bin` contains **essential user commands**
* These commands are available to **all users**
* Examples:

  * `ls`
  * `cp`
  * `mv`
  * `cat`

👉 Difference between `/bin` and `/sbin`:

* `/bin` → commands for **all users**
* `/sbin` → commands mainly for **system administration**

✔️ Concept is correct, just wording improved.
