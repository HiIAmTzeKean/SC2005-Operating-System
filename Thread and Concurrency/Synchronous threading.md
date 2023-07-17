---
tags: 🌱
date: 04--Jul--2022
---

# Synchronous threading

Children [[Thread]] can execute concurrently, and joins with its parents on terminate. Parent resumes execution once all children terminates.

Synchronous threading requires significant data sharing among threads, and parent thread combines data calculated by children.

> [!summary]
> Parent thread creates one or more children and waits for all of its children to terminate before resuming.

---
Links: [[Multithread]]