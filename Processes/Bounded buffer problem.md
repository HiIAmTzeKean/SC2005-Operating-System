---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Process
alias: Producer consumer problem
date: 14--Jul--2022
---

# Bounded buffer problem

## Bounded buffer without counter
The shared buffer implemented as circular array with 2 pointers in and out. The solution does not incur [[Race condition]] but suffers from wasting one slot in the array. *in* must always be one slot behind *out*.
### Variables
Both producer and consumer will have the shared data.
```C
#define BUFFER_SIZE 10
typedef struct {...}item;
item buffer[BUFFER_SIZE];
int in = 0;
int out = 0;
```
### Producer process
```C
#define BUFFER_SIZE;
while(true) {
    // produce an item in next_produced
    while (((in+1) % BUFFER_SIZE) == out);
    // while loop is true, we busy wait

    buffer[in] = next_produced;
    in = (in+1) % BUFFER_SIZE;
}
```
### Consumer process
```C
#define BUFFER_SIZE;
while(true) {    
    while (in == out);
    // while loop is true, we busy wait
    // There is nothing in the buffer to consume
    
    next_consumed = buffer[out];
    out = (out+1) % BUFFER_SIZE;
    //consume the next item
}
```

## Bounded buffer with [[Race condition]] 
The [[Race condition]] occurs when we introduce a shared counter, where both process can modify the counter. Without any synchronisation, *counter* suffers from [[Data inconsistency]].
```c
void producer(){
    // produce some item
    while (counter == BUFFER_SIZE);
    // while the buffer is full, we busy wait
    buffer[in] = next_produced;
    in = (in+1) % BUFFER_SIZE;
    counter++;
}

void consumer(){
    // check if the buffer is empty
    while (counter == 0);
    // while buffer is empty, we busy wait
    next_consumed = buffer[out]
    out = (out+1) % BUFFER_SIZE;
    counter--;
    // consume the item
}
```

## Modified problem with synchronisation
[[Synchronisation tools summary]] such as [[Semaphore]] used to protect shared data in [[Classical synchronisation problem]]

### Producer
```C
while (true){
    // produce item first
    // indicate to other processes that
    // one slot has been consumed.
    // atomic operation performed to
    // update empty
    wait(empty);
    // lock buffer as a shared variable
    wait(mutex);
    // add item to buffer
    // Once done release lock on buffer
    signal(mutex);
    // update full
    signal(full);
}
```

### Consumer
```C
while (true)
{
    // Decrement full to indicate slot consumed
    wait(full);
    // lock shared buffer
    wait(mutex);
    // remove item from buffer
    // release lock on buffer
    signal(mutex);
    // update empty
    signal(empty);
    // consumer item
}
```

### Order of wait() operations

Important as swapping will cause a [[Deadlock problem]]. Assuming buffer is empty and consumer locks mutex, no other producer can add to buffer. Assuming if buffer is now filled, and producer locks mutex, no other consumer can consume.

## Order of signal() operations

Affects scheduling efficiency.