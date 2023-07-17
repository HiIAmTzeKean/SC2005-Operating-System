---
tags: 🌱
date: 17--Jul--2022
---

# Dining philosophers problem

[[Classical synchronisation problem]] where philosophers either eat or think. There are 5 philosophers and 5 chopsticks, but 2 chopsticks are needed to eat.

Rice represents the dataset and chopsticks represent the resources needed to access the dataset.

![[Pasted image 20220717193135.png]]

## Shared data

```C
// Initialise variables
Dataset rice;
semaphore chopsticks[5];
```

## Code

Here each $P_i$ will try to obtain the left and right chopsticks as $chopsticks[i]$ and $chopsticks[(i+1)\mod 5]$.

```C
while(true){
    wait(chopsticks[left]);
    wait(chopsticks[right]);
    // eat
    signal(chopsticks[left]);
    signal(chopsticks[right]);
    // think
}
```

## Limitations

Deadlock can occur causing [[Liveness failure]]. Assuming each $P_i$ were to run the first line of the code and pick up the left, then each $P$ is waiting the right chopstick.

## Constraints

The fix for the [[Deadlock problem]] need not be a recursive loop but a sequence that allows all [[Process]] to complete execution.

1. Allow only 4 philosophers on the table with 5 chopsticks. Then, there will always be 2 chopsticks available to 1 philosopher, allowing all 4 to eat
2. Asymmetric approach. Even philosophers pick up left then right. Odd picks up right then left.
3. Picking in critical section. When in critical section, if both chopsticks are available, philosopher will eat
4. First 4 philosopher will pick up left while $P_5$ will pick up right. Since $P_5$ right chopstick taken by $P_4$ then $P_5$ will be stuck waiting. $P_1$ can pick up the right and execute, the chain follows till $P_5$ has both chopsticks and terminates.

---
Links: 