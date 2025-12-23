### User Management

When we are hired in a company, around **90% of production work is done on Linux**.
So user management becomes very important.

If a company has **100 employees** (developers, managers, QA, etc.) and **everyone is given root (superuser) access**, a small mistake—like deleting a system binary file—can **corrupt the entire Linux system**.

That is why we **manage users separately** and assign **permissions based on roles**:

* **DevOps engineers** → get higher-level permissions required for system and infrastructure tasks
* **Developers** → get access only to logs and work-related files
* **Managers** → usually get **read-only** access
* **QA** → limited access based on testing needs

---

### Core concepts in user management

We mainly work with **two things**:

1. **Users**
2. **Groups**

---

### Common User Management Commands

**Add a new user**

```bash
adduser <username>
```

**Check users**

```bash
vim /etc/passwd
```

**Set or change a user password**

```bash
passwd <username>
```

**View encrypted passwords**

```bash
vim /etc/shadow
```

> ⚠️ Note: `/etc/shadow` is readable only by the root user for security reasons.

---

### One-line summary

👉 User management in Linux prevents system damage by ensuring **the right user has the right level of access**.

# -----------------------------------------------------------------------------------------------------------------------------------------

### Password & User Management (Short)

* Linux passwords are **one-way hashed** and **cannot be restored**, only **reset**.
* If a user leaves the organization, the account is deleted:

  ```bash
  userdel <username>
  ```
* To switch users:

  ```bash
  su - <username>
  ```

---

### Interview: `useradd` vs `adduser`

* **useradd**: Low-level command, no prompts, used in scripts.
* **adduser**: User-friendly, asks for details, used manually.

---

### Password Restore?

❌ No. Passwords are stored as **hashes** in `/etc/shadow`, so recovery is impossible.
