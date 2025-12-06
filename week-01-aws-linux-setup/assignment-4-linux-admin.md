# **Assignment 4 – Linux Administration Practice**

(DevOps Micro Internship – Week 1)

This assignment focuses on **post-deployment Linux administration tasks** on your Ubuntu VM where your React app is running using Nginx.
It includes networking, process monitoring, and system information commands — all essential for real-world DevOps troubleshooting.

---

## *📌 Task 1 – Networking Commands**

## **1. Check Network Interface Configuration**

> **Note:** `ifconfig` is part of the `net-tools` package. On modern Ubuntu, it may not be installed by default.  

### **Install net-tools (if not already installed)**

```bash
sudo apt install net-tools
````

**Reason:** This installs `ifconfig` and other networking utilities, allowing you to check network interface details.

![Image 1](Figures/Assignment-4/ss1.png)

---

### **Run ifconfig**

```bash
ifconfig
```

### **Command Breakdown**

| Part       | Meaning       |
| ---------- | ------------- |
| **if**     | interface     |
| **config** | configuration |

**Full Meaning:**
"Show the configuration of all network interfaces."

### **Explanation**

This command displays IP addresses, MAC addresses, and interface status.
It’s useful for checking network connectivity, verifying your server’s IP setup, and troubleshooting networking issues.

![Image 1](Figures/Assignment-4/ss2.png)

---

## **2. Test Connectivity to a Domain**

```bash
ping -c 4 thecloudadvisory.com
```

### **Command Breakdown**

| Part                     | Meaning                                     |
| ------------------------ | ------------------------------------------- |
| **ping**                 | Packet Internet Groper (sends test packets) |
| **-c 4**                 | send exactly 4 packets                      |
| **thecloudadvisory.com** | target domain                               |

**Full Meaning:**
"Send 4 ICMP packets to thecloudadvisory.com and measure response time."

### **Explanation**

This checks whether your server can reach the target website and confirms internet + DNS connectivity.

![Image 1](Figures/Assignment-4/ss3.png)

---

## **3. Check Open Ports & Listening Services**

```bash
sudo netstat -tulnp
```

### **Command Breakdown**

| Flag        | Meaning                     |
| ----------- | --------------------------- |
| **sudo**    | run with admin privileges   |
| **netstat** | network statistics          |
| **-t**      | show TCP ports              |
| **-u**      | show UDP ports              |
| **-l**      | show listening ports only   |
| **-n**      | show numeric output         |
| **-p**      | show process using the port |

**Full Meaning:**
"List all TCP/UDP listening ports and the processes behind them."

### **Explanation**

This helps verify whether services like Nginx (port 80) or SSH (port 22) are running properly.

![Image 1](Figures/Assignment-4/ss4.png)
---

## **4. DNS Lookup (Method 1 – dig)**

```bash
dig pravinmishra.in
```

### **Command Breakdown**

| Part                | Meaning                   |
| ------------------- | ------------------------- |
| **dig**             | Domain Information Groper |
| **pravinmishra.in** | domain to query           |

### **Explanation**

`dig` shows DNS records such as A record, nameservers, and TTL. It helps validate DNS configuration.

![Image 1](Figures/Assignment-4/ss5.png)

---

## **5. DNS Lookup (Method 2 – host)**

```bash
host pravinmishra.in
```

### **Command Breakdown**

* **host** → quick DNS lookup tool

### **Explanation**

This provides a simpler DNS lookup showing only key records like A/AAAA. It’s faster and used for quick checks.

![Image 1](Figures/Assignment-4/ss6.png)

---

## **6. Download a File with wget**

```bash
wget -O /tmp/Untitled-design-40.png <URL>
```

### **Command Breakdown**

| Part         | Meaning                 |
| ------------ | ----------------------- |
| **wget**     | download file via web   |
| **-O**       | specify output filename |
| **/tmp/...** | save location           |

### **Explanation**

Used to download images, scripts, or configuration files to the server — very useful in automated deployments.

![Image 1](Figures/Assignment-4/ss7.png)

---

## **📌 Task 2 – Process Monitoring & Control**

## **Understanding Processes & Services**

Before performing process monitoring, here’s a quick guide to clarify key concepts:

* **Process:** A program that is currently executing on the computer.

  * Programs exist on disk; they become processes only when executed.
  * While running, a process consumes resources such as CPU and memory.
  * When execution finishes, the process terminates (normally) or is killed (forcefully).
  * Typically started by a **user** and often require manual interaction.
  * Examples: Opening a browser, VS Code, or running a command like `ping`.

* **Service:** A special type of process that usually runs in the **background** (daemon).

  * Often started automatically by the OS at boot.
  * Managed by the system, not by manual user interaction.
  * Continues running even if no user is logged in.
  * Can be stopped, started, or restarted using service management commands.
  * If a service is not enabled, it stops when the machine shuts down.

* **Daemon:** A background process that runs independently of user sessions. Most services are daemons. Unlike normal programs, daemons usually don’t have a visible interface.

> ✅ **Summary:** Programs become processes when executed by a user. Some processes run in the background as services/daemons, which are managed by the system and provide continuous functionality.

> ⚠ **Note:** Commands like `ps`, `pstree`, and `kill` mostly show **user-started processes**, but they can also display system services if you have sufficient permissions. Stopping a user process affects only that task, whereas stopping a system service may impact other dependent processes.

---

## **7. List All Running Processes**

```bash
ps -e
```

### **Command Breakdown**

| Part   | Meaning            |
| ------ | ------------------ |
| **ps** | process status     |
| **-e** | show all processes |

### **Explanation**

Displays all running processes on the machine. Useful for identifying what is currently running, whether user-started programs or system services.

![Image 1](Figures/Assignment-4/ss8.png)

---

## **8. Search for Nginx Process**

```bash
ps aux | grep nginx
```

### **Command Breakdown**

| Part           | Meaning                              |
| -------------- | ------------------------------------ |
| **ps aux**     | show all processes with full details |
| **|**          | pipe output                          |
| **grep nginx** | search for text “nginx”              |

### **Explanation**

Checks whether the Nginx process is active. Shows PID, memory/CPU usage, and other details of processes matching “nginx”.

![Image 1](Figures/Assignment-4/ss9.png)

---

## **9. View Process Hierarchy**

```bash
pstree
```

### **Command Breakdown**

| Part     | Meaning                             |
| -------- | ----------------------------------- |
| **ps**   | process                             |
| **tree** | display in hierarchical tree format |

### **Explanation**

Shows parent–child relationships between processes. Useful when analyzing service dependencies or understanding which processes spawned others.

![Image 1](Figures/Assignment-4/ss10.png)

---

## **10. Terminate a Process**

```bash
kill <PID>
```

### **Command Breakdown**

| Part     | Meaning                   |
| -------- | ------------------------- |
| **kill** | send signals to a process |
| **PID**  | process ID to terminate   |

### **Explanation**

Stops a running process. Useful for closing unresponsive or unnecessary tasks. Note: terminating a user process is different from stopping a service; services are managed by the system and may restart automatically.

![Image 1](Figures/Assignment-4/ss11.png)

---

## *📌 Task 3 – System Information Commands**

---

## **11. Display Full System Info**

```bash
uname -a
```

### **Command Breakdown**

| Flag   | Meaning          |
| ------ | ---------------- |
| **-a** | show all details |

### **Explanation**

Displays kernel version, OS type, architecture — helpful for debugging OS issues.

![Image 1](Figures/Assignment-4/ss12.png)

---

## **12. Check System Uptime**

```bash
uptime
```

### **Explanation**

Shows how long the system has been running and its load average — useful for performance monitoring.

![Image 1](Figures/Assignment-4/ss13.png)

---

## **13. Display Logged-in Users**

```bash
who
```

### **Explanation**

Shows active logged-in users. Helps identify unauthorized access or user sessions.

![Image 1](Figures/Assignment-4/ss14.png)

---

## **14. Check Memory Usage**

```bash
free -h
```

### **Command Breakdown**

* **-h** → human-readable format

### **Explanation**

Displays total, used, and free memory in readable units. Helpful for detecting memory bottlenecks.

![Image 1](Figures/Assignment-4/ss15.png)

---

## **15. Check Disk Usage**

```bash
df -h
```

### **Command Breakdown**

* **df** → disk filesystem
* **-h** → human-readable format

### **Explanation**

Shows available disk space on mounted filesystems. Important for preventing “disk full” errors.

![Image 1](Figures/Assignment-4/ss16.png)

---

## **16. Directory Size in /var**

```bash
sudo du -sh /var/*
```

### **Command Breakdown**

| Part      | Meaning           |
| --------- | ----------------- |
| **du**    | disk usage        |
| **-s**    | summary only      |
| **-h**    | human-readable    |
| **/var/** | directory to scan |
| **/*`**   | all files and directories inside the selected directory |

### **Explanation**

Shows which directories inside `/var` are consuming the most space — useful for identifying log or cache bloat.

![Image 1](Figures/Assignment-4/ss17.png)

---


