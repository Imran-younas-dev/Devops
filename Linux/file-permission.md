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

