---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 19--Jul--2022
---

# Banker's algorithm

Less efficient than [[Resource graph allocation algorithm]]. Known as Banker's algorithm because it can be used in a banking system to ensure bank can satisfy needs of all customers.

## Data structure needed

Where $n$ is the number of threads and $m$ is number of resource types

1. $Available[m]$
    1. Array indicating available resources for each type
2. $Max[n][m]$
    1. Matrix defining maxing number of instances needed by [[Thread]] of each resource type
3. $Allocation[n][m]$
4. $Need[n][m]$

## Safety Algorithm

Check if system is in a safe state. Algorithm requires $O(m \times n^2)$ operations to complete.

1. Initialise $Work[m]$ and $Finish[n]$
    1. $Work = Available[m]$
    2. $Finish[i] = false$ for $i=0;i=n$
2. Find the next i to allocate
    1. $Finish[i] = false \land Need[i] \le Work$
    2. If no $i$ exist then go step 4
3. Release resource to pool
    1. $Work[i] = Work[i] + Allocation[i][j]$
    2. $Finish[i] = true$
4. If $Finish[i]==true$ for all $i$
    1. System is [[Deadlock safe state]]
    2. Else [[Deadlock unsafe state]]

### Proof

Worse case scenario:
1. $T_n$ requires resources and for loop runs $n$ times
2. Followed by $T_{n-1}$ and loop runs $n-1$ times
3. Overall $(m\times n)(m\times (n-1))...(m \times 1)$
4. $m \times (n+(n-1)+...+1)$
5. Simplify with arithmetic summation -> $O(m \times n^2)$

```C
exist_i = true;

// Worse case scenario while loop will run n times
while(exist_i){
    exist_i = false;
    // Traverse the n times
    for (i = 1 to N){ 
        // Need[i] <= Work
        // repeats m times to check the vector of Work[m]
        if ((not FINISH[i]) && Need[i] <= Work){
            // also O(m) operation, vectors addition
            Work = Work + Allocation[i];
            exist_i = true;
        } 
    }
}

check_if_safe(Finish)
```

## Resource request algorithm

Let $Request[i][m]$ be the vector of a thread denoting the number of resource type needed.

1. if $Request[i] \le Need[i]$
    1. Go to step 2
    2. Else raise error since exceed maximum claim

---
Links: 