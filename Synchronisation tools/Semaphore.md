---
tags: 🌱
date: 15--Jul--2022
---

# Semaphore

More robust than [[Mutex locks]] and provides more sophisticated ways for a process to synchronise.

Semaphore $S$ is an integer variable access only through 2 [[Atomically]] operation: [[wait()]] and [[signal()]]

## Code
```C
while (true){
    wait(mutex);
    // critical section
    signal(mutex);
    // remainder section
}
```

## 2 types of semaphore

[[Counting semaphore]] and [[Binary semaphore]].

## Steps to implement semaphore

1. Identify all shared items
    1. Shared data
    2. Shared resources such as count
2. Protect shared data
    1. Identify critical section
    2. Use [[Binary semaphore]] as lock
3. Protect shared resources
    1. 1 [[Counting semaphore]] for each resource
    2. Initialise resource to number available

## Disadvantage

Like [[Mutex locks]] it suffers from [[Busy waiting]].

## Solution with no busy waiting

[[sleep()]] and [[wakeup()]] can be implemented, and a waiting queue associated with the semaphore created. List of process can be implemented by a link field in the [[Process control block|PCB]].

```C
typedef struct{
    int value;
    struct process *list;
}semaphore;
```

---
Links: 