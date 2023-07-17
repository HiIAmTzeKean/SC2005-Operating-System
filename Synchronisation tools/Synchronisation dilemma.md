---
tags: 🌱
date: 09--Jul--2022
---

# Synchronisation dilemma

Access to shared data may result in [[Data inconsistency]]. Once such event is when there is a [[Race condition]]. To maintain consistency of data, there must be **causal ordering** (sequential) of RW to shared data.

## Solution
[[Critical section problem]] aims to solve this [[Concurrency|Concurrent]] access. 

---
Links: 