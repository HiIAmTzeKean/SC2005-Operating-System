---
tags: 🌱
date: 15--Jul--2022
---

# signal()

## Code

```C
signal(S){
    S++;
}
```

## Modified code (No [[Busy waiting]])

Implementation with [[wakeup()]]. Note that if value is less than equal to zero, it means that there are still processes requesting resource but not yet served. If value is positive, then there are resources available but not yet requested by any process.

```C
signal(S){
    S-->value++;
    if (S-->value <= 0){
        wakeup(S-->list.head);
    }
}
```

---
Links: 