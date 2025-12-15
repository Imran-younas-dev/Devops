As discussed above, **`/bin`** is for **all users**, and **`/sbin`** is mainly for the **administrator (root)**.

In modern Linux systems:

* `/bin` → actually points to `/usr/bin`
* `/sbin` → actually points to `/usr/sbin`

So:

```
/bin  → /usr/bin
/sbin → /usr/sbin
```

These are **not shortcuts like Windows shortcuts**.
They are **symbolic links (symlinks)** used by Linux to keep compatibility with older systems.

👉 In Windows:

```
C:\abc\folder\game\file
```

This is a normal path, not a symlink by default.

👉 In Linux:

* `/bin` and `/sbin` are **linked directories**, not real separate folders anymore.

⚠️ Important correction:
❌ *“both are part of user”*
✅ **Correction:**
They are part of the **system**, not the user’s home directory.

---

## 📁 Other Important Directories

### `/srv`

* `/srv` stands for **service**
* It is used to store data for **servers**
* Example:

  * web server data
  * FTP server files

✔️ Correct.

---

### `/usr`

* `/usr` contains **user-level programs and utilities**
* Most commands, libraries, and applications live here
* Examples:

  * `/usr/bin`
  * `/usr/lib`
  * `/usr/sbin`

⚠️ Note:
`/usr` does **not** mean home user.
Home users live in:

```
/home/username
```

---

### `/opt`

* `/opt` is used for **optional or third-party software**
* Common in organizations and enterprises
* Example:

  * Java
  * Oracle
  * Custom company software

✔️ Your understanding is **correct** here.

---

## ⭐ Simple Summary (Easy to Remember)

* `/bin` → essential user commands (now linked to `/usr/bin`)
* `/sbin` → system/admin commands (linked to `/usr/sbin`)
* `/usr` → system programs & utilities
* `/srv` → server-related data
* `/opt` → third-party or enterprise software
* `/home` → user personal files

---

**mnt (Mount)**
`/mnt` is used to mount and manage storage volumes (disks). It is mainly used by system administrators. All external or additional storage devices can be mounted and accessed from this directory.

**var (Variable)**
`/var` is used for log files. It contains logs from different services and servers, such as Apache server logs, system logs, and other application logs.

**proc, dev, tmp**

* `/proc`, `/dev`, and `/tmp` contain **temporary or virtual files**.
* These files are created at runtime and do not exist permanently on disk.
* In Ubuntu, temporary files (especially in `/tmp`) may be deleted automatically.

**run**
`/run` stores **runtime data**. If any process needs to store temporary runtime information while the system is running, it is stored in this directory.

**etc**
`/etc` contains **system configuration files**.
It is similar to the **Settings** of a mobile phone or computer.
All system and application configuration files are stored here, and system behavior can be configured or updated from these files.

---

### How Linux knows which command to run

When we run a command using `ls`, Linux knows where to find it because the command’s binary location is already stored in the **PATH environment variable**.

If you run:

```bash
echo $PATH
```

You will see a list of directories where Linux searches for commands.

If a command is **not present in any directory listed in PATH**, Linux shows:

```
command not found
```

We can also **add new directories to the PATH variable** to run custom commands from anywhere.
