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
