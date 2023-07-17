---
tags: 🌱
date: 09--Jul--2022
---

# Peterson's solution

> [!note]
> Approach is a [[Software based solution]]

## Requirements

1. 2 processes that alternate execution between critical section and remainder section
2. Shares 2 data items
    1. *turn* that indicates which process turn to enter
    2. *flag* array that indicate if the process is ready to enter

## Algorithm

![[peterson's algorithm.png]]

## Proof

We prove that the solution satisfies [[Critical section solution criteria]].

###  [[Critical section solution criteria#Mutual exclusion|Mutual exclusion]] 

If $P_1$ enters critical section, then either $P_0$ is not ready or it is not $P_0$ *turn*. Since *turn* can only equal 1 or 0, and $P_1$ is in critical section, $P_0$ can only enter once $P_1$ exits.

### [[Critical section solution criteria#Progress]]

1. $P_1$ prevented from critical section in while loop iff $flag[0]$ == 1 and *turn* == 0. Else, if $P_0$ is not ready, $P_1$ can enter critical section.
2. If both $P_1$ and $P_0$ are ready, then *turn* will decide which will be selected.
3. When $P_0$ is done, it will reset its flag, and $P_1$ will be able to enter critical section.

[[Critical section solution criteria#Bounded waiting]]

Once $P_0$ exit critical section, it will reset its *flag*, allowing $P_1$ to enter. If $P_0$ loops back to start of program to set its *flag*, it will still set turn to 1.

Since $P_1$ does not change the value of *turn* during while loop, $P_1$ guaranteed to enter after one entry by $P_0$

> [!note]
> Current architecture of load and store may not guarantee solution to work. Refer [[Peterson's solution limitations]]

---
Links: [[Process]] - [[Critical section problem]]