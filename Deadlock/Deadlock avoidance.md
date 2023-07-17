---
tags: 🌱
date: 19--Jul--2022
---

# Deadlock avoidance

Each thread declares the **maximum** number of resources of each type that it may need. OS will allocate resources if system stays in [[Deadlock safe state]] after allocation, else the request will be denied.

## [[Deadlock problem]] condition

1. OS is in [[Deadlock safe state]]
    1. No deadlocks
2. OS in [[Deadlock unsafe state]]
    1. Possibility of a deadlock

## Algorithms to enforce avoidance

1. [[Resource graph allocation algorithm]]
2. [[Banker's algorithm]]

---
Links: 