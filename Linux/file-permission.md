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

