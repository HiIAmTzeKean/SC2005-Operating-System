---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 15--Jul--2022
---

# acquire()


```C
void acquire() {
    while (!available)
    {
        // Busy waiting
    }
    available = false;
}
```

---
Links: [[Busy waiting]]