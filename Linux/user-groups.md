### Groups in Linux

Today, we are exploring **groups in Linux**.
A group is a collection of users used to **manage permissions** efficiently.

For example, in a company with **500 employees**:

* 300 Developers
* 50 QA
* 50 Product Managers
* 100 DevOps

Managing permissions **user by user is not practical**, so we use **groups** to assign access based on roles.

---

### Group Commands

**Create a group**

```bash
addgroup <group_name>
```

**View groups**

```bash
cat /etc/group
```

**Add a user to a group**

```bash
usermod -aG <group_name> <username>
```

---

### How does a user access the environment?

In **AWS**, we use **EC2**, which provides a Linux instance.
Users access the instance using:

* The **IP address** of the EC2 instance
* Their **username and password** (or SSH key)

Once logged in, users can access resources based on **group permissions**.

---

### One-line summary

👉 Groups help manage permissions **role-wise instead of user-wise**, especially in large organizations.


# ====================================================================================================

### SSH (Secure Shell)

An **SSH client** is a process through which we can access a **Linux virtual environment remotely** as a user.
It allows us to connect to a Linux server **live**, just like working on the system directly.

By default, a Linux server runs the **SSHD (SSH daemon)** service.

To access the server, we use an **SSH client** from the command line.

**Command:**

```bash
ssh <username>@<ip-address>
```

After running the command, it asks for a **password**, and once authenticated, you are logged in to the **Linux instance**.

---

### One-line summary

👉 SSH lets you securely log in to a remote Linux server using the command line.