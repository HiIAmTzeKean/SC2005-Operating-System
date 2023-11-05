---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 09--Jul--2022
---

# [[Peterson's solution]] limitations

**Modern processors** or compliers may **reorder RW** to improve operation that have no dependencies.

## Impact

### Single threaded

Reordering has no effect as the end state of the variables will still be consistent as expected.

### [[Multithread]] application

When there is shared data, reordering can cause inconsistent results.

```C
boolean flag = false;
int x = 0;

// Tread 1
while (!flag);
printf(x);

// Tread 2
x = 100;
flag = true;
```

2 scenarios that can occur in this example

1. Thread 2 is reordered
    1. flag is set first and when Thread 1 is executed, x will still be 0
2. Thread 1 is reordered
    1. x is printed first before the while loop

Extension of the problem to reordering of entry section can cause [[Process]] to run their [[Critical section]] concurrently.

---
Links: 