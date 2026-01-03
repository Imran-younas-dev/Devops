### **File Permissions in Linux**

File permissions are a **major feature of Linux**.

Let’s say **two users** are working on the same Linux instance:

* One user is a **Developer**
* The other user is **QA**

If the **Developer creates a script in the `/tmp` directory**, the QA user **cannot delete or modify that file** unless permission is given.

Similarly, normal users **cannot delete system files** like **`/usr/sbin`**, because if anyone could delete them, **user management and system security would have no meaning**.

That’s why Linux uses **file permissions**:

* To control **who can access a file**
* To define **who can read, write, or execute a file**
* Permissions depend on the **user and their role**

In short, **file permissions protect files and the system by controlling access based on users**.


# ===================================================================================================

### **Linux File Permissions (Simple Explanation)**

We discussed **what file permissions are** and **why they are important**.

Now, we discussed **how a Developer and a QA user can be given or denied access** to a file for **reading, writing, and executing**.

When we run the **`ls -ltr`** command, we can see the **details of files**, including their permissions.

**Example:**
If `test.txt` is a file, its permission might look like this:

```
-rw-rw-r--
```

### **Breaking it down:**

* The **first character**:

  * `-` → file
  * `d` → directory

* The next **9 characters** are divided into **3 groups**:

  1. **User (owner)**
  2. **Group**
  3. **Others**

Each group has **3 permissions**:

* **r** = read
* **w** = write
* **x** = execute

So:

* **rw-** → user can read and write
* **rw-** → group can read and write
* **r--** → others can only read

### **Summary**

Linux file permissions control **who can read, write, or execute a file**, ensuring **security and proper user access**.

---


### ==========================================================================================================

### **Linux File Permissions (Simple Explanation)**

As discussed, there are **three permission types** for every file:

1. **User (Owner)**
   → The user who created the file

2. **Group**
   → A group of users who can be given specific permissions

3. **Others**
   → All other users (for example, QA users)

---

### **Changing Permissions using `chmod`**

The command to change file permissions is:

```
chmod <permissions> <filename>
```

We often use **numbers** because they are easier and faster.

#### **Permission values**

* **r (read)** = 4
* **w (write)** = 2
* **x (execute)** = 1

---

### **Examples**

#### **Read + Write permission**

If you want to give **read and write (rw-)** permission to **user, group, and others**:

```
chmod 666 filename
```

(4 + 2 = 6)

#### **Read-only permission**

If you want to give **read-only** permission to the **user only**:

```
chmod 400 filename
```

---

### **Quick reminder**

* The **first digit** → user
* The **second digit** → group
* The **third digit** → others

This system helps control **who can read, write, or execute a file**, keeping the system secure.



# ===================================================
### **`chmod` vs `chown` in Linux**

We have already learned about **`chmod`**, which is used to **manage file permissions**
(read, write, execute).

Now we are learning about **`chown`**, which is used to **change ownership** of a file or folder.

---

### **What is `chown`?**

**`chown` = change owner**

Example scenario:

* A **QA user is leaving the organization**
* The QA user wants to **transfer ownership** of a file to the **Developer**

Command:

```
chown dev:dev test.sh
```

This means:

* **Owner** of `test.sh` becomes `dev`
* **Group** also becomes `dev`

---

### **File permission vs Folder permission**

* **File permissions** control:

  * Who can **read**, **write**, or **execute** a file

* **Folder (directory) permissions** control:

  * Who can **enter the folder**
  * Who can **list files**
  * Who can **create or delete files** inside it

---

### **Easy real-life example (Bank example)**

Think of it like a **bank**:

* First, you need **permission to enter the bank**
  → This is like **folder permission**

* Then, you need **separate permission to access a locker**
  → This is like **file permission**

If you don’t have permission to **enter the bank (folder)**,
you can never access the **locker (file)** inside it.

---

### **Final takeaway**

* **`chmod`** → controls **what you can do** (read/write/execute)
* **`chown`** → controls **who owns** the file or folder
* **Folder permission is required before file permission**

