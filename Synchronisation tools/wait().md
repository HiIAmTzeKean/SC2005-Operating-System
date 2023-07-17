---
tags: 🌱
date: 15--Jul--2022
---

# wait()

Originally termed $P$ called *proberen*, Dutch for "to test".

## Code

```C
wait(S){
    while (S<=0); // busy wait
    S--;
}
```

## Modified code (No [[Busy waiting]])

Addition of [[sleep()]]. Since value is decremented first, if value was 1, it implies that there is still 1 more resource available. If value was 0, then the decrement will cause value to be negative, and the process will be put to sleep.

```C
wait(S){
    S->value--;
    if (S-->value<0){
        S-->list.append(process)
        sleep();
    }
}
```

---
Links: 