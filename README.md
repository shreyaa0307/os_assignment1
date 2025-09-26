
# OS Lab Assignment 1 - Process Creation and Management  

**Course Code & Name:** ENCS351 - Operating Systems  
**Program/Class:** B.Tech CSE (Data Science)  
**Student Name:** jai  
**Student Roll No.:** 2301420045

---

## 📌 Project Overview  
This project demonstrates **Linux process management concepts** using Python.  
The assignment simulates the behavior of:  
- `fork()`  
- `exec()`  
- Process inspection via `/proc`  
- Zombie and orphan processes  
- Priority scheduling with `nice()`  

It provides hands-on practice with **process creation, execution, and scheduling** in an OS environment.  

---

## 🎯 Learning Outcomes  
- Understand the **lifecycle of processes** in Linux.  
- Create and manage **child processes**.  
- Simulate **zombie** and **orphan** processes.  
- Inspect process details from the **/proc filesystem**.  
- Demonstrate **priority scheduling** using `nice` values.  

---

## 📝 Tasks Implemented  

### **Task 1: Process Creation Utility**  
- Created **N child processes** using `os.fork()`.  
- Each child prints PID, PPID, and a custom message.  
- Parent waits for all children with `os.wait()`.  

### **Task 2: Command Execution using exec()**  
- Each child process executes Linux commands (`ls`, `date`, `ps`).  
- Implemented using `os.execvp()` and `subprocess.run()`.  

### **Task 3: Zombie & Orphan Processes**  
- **Zombie:** Child exits, parent doesn’t wait. Verified with `ps -el | grep defunct`.  
- **Orphan:** Parent exits before child finishes, child is adopted by `init`.  

### **Task 4: Inspecting Process Info from /proc**  
- Read from `/proc/[pid]/status` → process name, state, memory usage.  
- Read `/proc/[pid]/exe` → executable path.  
- Read `/proc/[pid]/fd` → open file descriptors.  

### **Task 5: Process Prioritization**  
- Created CPU-intensive child processes.  
- Assigned different `nice` values.  
- Observed execution differences due to scheduling.  

--- 
