---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 18--Jul--2022
---

# [[Deadlock]] in [[Multithread]]

Given the following [[Mutex locks]].

```C
mutex first_mutex;
mutex second_mutex;
```

and 2 threads each running a function that attempts to do some work by first acquiring the lock.

```C
void func_one(){
    lock(first_mutex);
    lock(second_mutex);
    // Some work here
    unlock(first_mutex);
    unlock(second_mutex);
}
void func_two(){
    lock(second_mutex);
    lock(first_mutex);
    // Some work here
    unlock(second_mutex);
    unlock(first_mutex);
}
```

If [[Thread]] 1 obtains the first lock and [[Context switch]] to thread 2, then both threads will be in a [[Deadlock problem]].

We also see that the deadlock depends on the sequence of code run, which makes it difficult to [[Handling deadlock]] as it may occur under specific conditions.

---
Links: 