---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Thread
date: 04--Jul--2022
---

# Multithreading model

[[User threads]] and [[Kernel threads]] can have some defined mapping.

## Relationship between models
### One-to-many
No such implementation since it is wastage of OS resources to map a single [[Thread]] to many kernel thread.

### Many-to-one model
Maps multiple [[User threads]] to one [[Kernel threads]]. Thread management handled by [[Thread library]] in [[User space]].

#### Advantage
1. Less kernel threads need to be set up for this model
#### Disadvantage
1. Entire process is blocked if single thread makes blocking call.
2. Only one thread can access kernel, multiple threads cannot run in parallel

### One-to-one model

![[one to one model.png]]

Each user thread maps to one kernel thread. Most common approach as the increasing number of cores in a system allows for greater number of kernel threads.

#### Advantage
1. More [[Concurrency]] by allowing another thread to run when another thread is blocked by [[System call]].
2. Multiple threads can run parallel on multiprocessors

#### Disadvantage
1. Each user thread creation requires kernel thread creation -> thread creation overhead
2. Too many kernel threads can overload system

### Many-to-Many model

Multiple user threads to a smaller or equal number of kernel threads.

#### Advantage
- OS can create a sufficient number of [[Kernel threads]] to support the [[User threads]] where the threads are efficiently utilised.
- Avoids the disadvantage from the other mapping and allows the [[User program]] to create as many [[User threads]] and [[Kernel threads]] can run in parallel.

#### Disadvantage

- Mapping in practice is tough since it is difficult to determine how many kernel threads should be mapped.

---
Links: [[Multithread]]