---
tags: 🌱
date: 17--Jul--2022
---

# Reader writer problem

Shared database with 2 classes of uses. Reader that reads and writer that writes. The problem is to allow multiple readers to read but single writer to write at a time.

[[Binary semaphore]] are used to lock shared data in this [[Classical synchronisation problem]].

## Shared data

```C
// integer to keep track of number
// of readers
int readcount = 0;
// mutex to lock readcount
binary_semaphore mutex;
// rw_mutex to lock database
binary_semaphore rw_mutex;
```

## Writer

```C
while(true){
    // acquire the database lock
    wait(rw_mutex);
    // perform write operations
    signal(rw_mutex);
}
```

## Reader

Note that $rw\_mutex$ is placed within $mutex$ lock. If $rw\_mutex$ was the first statement, then there can only be one reader reading at a time.

$rw\_mutex$ on first line will lock the entire database, and no other readers or writers can access. The current construct allows for multiple readers but a single writer.

```C
while(true){
    // lock readcount then
    // increment readcount
    wait(mutex);
    readcount++;
    // Check if this is the first reader
    // If first reader we check if writer is
    // accessing database
    if (readcount==1)
        wait(rw_mutex);
    // database is now open to readers
    signal(mutex);
    // perform read operations
    read();
    // lock readcount and decrement
    wait(mutex);
    readcount--;
    // check if this is the last reader
    // if this is the last reader
    // release database for writing
    if (readcount==0)
        signal(rw_mutex);
    signal(mutex);
}
```

---
Links: 