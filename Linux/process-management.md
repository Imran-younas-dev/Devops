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


In Linux, a pipe ( | ) takes the output of the first command
and passes it as input to the second command.

Killing a process:
kill <PID>        → gracefully stops a process
kill -9 <PID>     → forcefully terminates a process

CPU scheduling concept:
If a process is taking more CPU time, the scheduler may treat it
as a high-priority process, similar to how doctors prioritize
critical patients in a hospital.

Sandbox environment:
A sandbox is an isolated environment used to test applications
without affecting the main system.

Service vs Process:
A process is a running program.
A service is a special type of background process that starts
automatically at system boot.

Examples of services:
- Web servers like Apache or Nginx
- Database services
- System daemons

Unlike normal applications (e.g., YouTube in a browser),
services automatically start again after a system restart.

List all running services:
systemctl list-units --type=service
