---
tags: 🌱
date: 16--Jul--2022
---

# Race condition

When 2 [[Thread]] are working on separate variables, [[Race condition]] will not occur.

There can be race conditions when 2 treads work on the same variable. Where the end state of the variable is not deterministic - depends on the order of execution of the treads.

## Example

```C
// Thread A

x = 1;
x = y + 1;

// Thread B

y = 2;
y = y * 2; 
```

Variable x in this case can take on 2 possible values depending on the execution.

## Bounded buffer problem example

In [[Bounded buffer problem]] both producer and consumer modifies "count" variable. The modification on machine language is to add 1 to the register, but since each process has its own context, the contents of "count" may not be consistent for both process.

![[synchronisation race condition.png]]

---
Links: 