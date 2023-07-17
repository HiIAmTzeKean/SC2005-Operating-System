---
tags: 🌱
date: 15--Jul--2022
---

# Counting semaphore

Can be used to control access to resources consisting of a finite number of instances.

$S$ will be initialised to number of resources available and each time a [[Process]] requests for the resource it will call [[wait()]] and decrement count if resource is available. When a process releases the resource, it calls [[signal()]] and increments $S$. If $S$ is 0, the process will be blocked till $S$ is greater than 0.

---
Links: 