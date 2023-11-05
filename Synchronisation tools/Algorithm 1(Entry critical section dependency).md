---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 03--Sep--2022
---

# Algorithm 1(Entry critical section dependency)

```C
void process1(){
while(1)
{
    while (turn!=1); // busy wait while it is not process turn
    criticalSection();
    // pass turn to other process
    turn = 0;
    remainderSection();
}
}
void process0(){
while(1)
{
    while (turn!=0); // busy wait while it is not process turn
    criticalSection();
    // pass turn to other process
    turn = 1;
    remainderSection();
}
}
```

## Analysis of [[Critical section solution criteria]]
1. Mutual exclusion :✔️
    1. When P1 is in the critical section, P0 cannot enter critical section, vice versa.
2. Progress ❌
    1. When P1 is done executing, it passes on turn to P0, and executes remainder section
    2. If P0 wants to enter critical section again, it has to wait for P1 to
3. Bounded waiting ✔️
    1. 

---
Links: 