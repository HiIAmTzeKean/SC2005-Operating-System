---
tags: 🌱
alias: Multithreading
date: 03--Jul--2022
---

# Multithread

Multiple [[Thread]] in a process are able to service CPU intensive task in [[Parallelism|parallel]].

![[multithread.png]]

## Thread vs Process
When a server receives a request, and is [[Single threaded]], it can only service one client at one time.

Creation of threads are more efficient than [[Process creation]] . Thus, when new request are made, threads can be created and server can resume listening.

|          | Thread         | Process                                                               |
|:--------|:---------------|:----------------------------------------------------------------------|
| Creation | More efficient | Requires more time and resource intensive                             |
| Overhead |                | New processes will perform same task as existing processes |

## Benefits
1. Responsive
    - Interactive applications can continue to run even though part of it might be blocked
2. Resource sharing
    - Processes can only share resources through [[Shared memory]] and [[Message passing]]. Threads share memory and resources to the process they belong to.
3. Economy
    - Less creation time and [[Context switch]] is faster
4. Scalability

---
Links: