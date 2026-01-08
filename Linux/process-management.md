### Process Management in Linux

A **process** is a running instance of a program.

For example, in the background:

1. A **Python program** (e.g., an LLM model doing heavy calculations)
2. A **cron job**
3. A **script**

If one process is **CPU-intensive** (for example, an LLM using **90% CPU**), the remaining CPU resources are shared among other processes.

---

### Types of Process Management

1. **View / Check processes**
   Used to see running processes.

   ```bash
   ps
   ps aux
   ```

2. **Kill / Stop processes**
   Used to stop or terminate a process that is taking too much time or resources.

3. **Priority / De-priority processes**
   The CPU can prioritize processes using **nice values**, similar to how hospitals prioritize ICU patients.

---

### One-line summary

👉 Process management helps monitor, control, and prioritize running programs to efficiently use CPU resources.
