---
tags: 🌱
date: 14--Jul--2022
---

# Mutex locks

Software based approach [[Peterson's solution]] and [[Hardware support for synchronisation]] are typically not accessible to programmers. Higher level **software** tools are designed such as mutex locks ([[Critical section solution criteria#Mutual exclusion]] locks)

## Code

```c
while (true){
    acquire(lock);
    // critical section
    release(lock);
    // remainder section
}
```

## Usage

Boolean variable indicates if lock is available. [[acquire()]] returns if lock is available and [[release()]] to reset the lock.

Both functions are performed [[Atomically]] such that other processes are blocked when lock is not available.

## Disadvantage

[[Process]] is [[Busy waiting]]. Which is detrimental when CPU only has a single core since all other processes must wait for a context switch before actual work is done.

## Advantage

Since context switch takes up a considerable amount of time, [[Spinlock]] can be advantages if the lock is held for a [[Spinlock short duration]]. Allowing for time savings by avoiding time loss from context switches.

---
Links: 