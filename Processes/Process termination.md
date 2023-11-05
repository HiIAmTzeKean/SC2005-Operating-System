---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Process
date: 21--Jul--2022
---

# Process termination
Once process finishes, it runs [[Exit()]] to inform OS to delete it. Child process can also return status value to parent process. 

Another scenario is when the parent calls [[Abort()]] to terminate the execution of child processes. This occurs when child exceeded resource allocated or task assigned no longer needed. Note that this is only possible if parent and child are running concurrently (else parent will be in waiting queue and not be able to execute).

All resources of process (physical and virtual memory, files, buffers) are deallocated and reclaimed by OS -> prevent [[Deadlock problem]] where process holds resources it is not using

## Termination reasons
1. Child exceed usage of allocated resources
2. Task assigned to child no longer required
3. Parent exiting and OS does not allow child to continue if parent terminates
    1. Cascading termination of child process when parent terminated

---
Links: 