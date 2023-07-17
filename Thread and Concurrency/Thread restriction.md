---
tags: 🌱
date: 27--Aug--2022
---

# Thread restriction

We want to allow [[User program]] to create an arbitrary number of [[Thread]] in the system but the hardware can only support a limited number of [[Thread]].

The solution is to then allow for 2 layers of abstraction with the use of [[User threads]] and [[Kernel threads]], each existing within their own space. OS will then define the mapping of the threads in [[Multithreading model]].

---
Links: 