---
tags: 🌱
date: 04--Jul--2022
---

# Threading issues

1. [[Fork()]] and [[Exec()]]
    1. Semantics of fork and exec calls change in [[Multithread]] program since a decision must be made to either duplicate all threads or just the thread involved
2. [[Signal]] handling
    1. On multiprocessing, a process much be chosen to receive the signal
    2. For processes with multiple threads, following options can be used
    3. Deliver signal to thread which signal applies
    4. Deliver signal to every thread
    5. Deliver signal to certain threads
    6. Assign specific thread to receive all signals
3. Thread cancellation
4. Thread-local storage

---
Links: [[Multithread]]