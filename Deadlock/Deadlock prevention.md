---
tags: 🌱
date: 19--Jul--2022
---

# Deadlock prevention

Providing set of methods to ensure that at least one of the [[Deadlock conditions]] does not hold true.

![[Deadlock conditions#Necessary conditions]]

## Mutual exclusion
### Advantage
Sharable resources such as read-only files does not require mutual exclusion

### Disadvantage
Cannot be applied to non-shareable resources

## Hold and wait

Enforce that whenever [[Thread]] request for resources, thread must not hold any resource

1. Each thread to request and be allocated all its resources before execution
    1. Application limited due to dynamic nature of requesting
2. Thread request only when it has no resources
    1. If thread requires additional resources, it must first release all resources allocated and request again

### Disadvantage

1. Resource utilisation low as resources can be allocated by unused for long period
2. Thread resource starvation. Thread can wait indefinitely for popular resources

## No Preemption

If a thread holds some resources request for additional resources that cannot be immediately allocated, all resources thread holds will be preempted. Preempted resources are added to list of resources that the thread requires. Once all resources the threads needs are available (regain old resources and new ones), thread will be restarted.

### Disadvantage

Protocol applied to resources whose state can be easily save and recovered such as [[CPU Register]]. Does not apply to [[Mutex locks]] and [[Semaphore]] which deadlocks then to occur.

## Circular wait

Negating the first 3 conditions typically impractical but circular wait can be prevented by imposing a total ordering of all resource types and require thread to request resources in increasing order of enumeration.

### Proof

Let $R=\set{}$ where each $R_i$ is assigned a unique integer which allows comparison to obtain equivalence. Let $F: R \rightarrow N$ where function returns integer order. Given the protocol that thread first requests $R_i$ and that $R_j$ requested subsequently must satisfy $F(R_j) > F(R_i)$.

We prove by contradiction. Assume that there is circular wait within $\set{T_0,T_1...}$  such that $T_i$ is waiting for $R_i$ held by $T_{i+1}$. Mod arithmetic used such that $T_n$ waits for $R_0$. $T_i$ can only request if $F(R_{i}) > F(R_{i-1})$ for all $i$. From $T_0 \rightarrow T_n$ we have $F(R_{n})<F(R_{0})...<F(R_{n-1})<F(R_{n})$. By transitivity, $F(R_{n})<F(R_{n})$ which is a contradiction.

---
Links: 