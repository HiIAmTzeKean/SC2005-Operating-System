---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: memory fence
date: 10--Jul--2022
---

# Memory barrier

> [!note]
> Memory barrier is a very low-level operation and only used by kernel developers

[[Memory model]] vary by processor types, thus memory barriers are needed to ensure visibility of modifications to memory to processors.

They are a class of instructions that can **force any changes in memory** to propagate to all other processors to make modifications **visible to [[Thread]] on other processors**.

## Key concept

When memory barrier performed, OS ensures all load and store completed first. Even if there is instruction reorder, memory barrier ensures store operation completed in memory and visible to other processer before future load and store performed.

## Example

```C
// Thread 1
while (!flag)
    memory_barrier();
printf(x);

// Thread 2
x = 100;
memory_barrier();
flag = true;
```

In this example, the memory barrier ensures all variables are stored into memory before further execution.

---
Links: 