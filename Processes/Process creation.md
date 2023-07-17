---
tags: 🌱
date: 21--Jul--2022
---

# Process creation

[[Process]] creating other processes. Where the parent process will create children processes, eventually forming a tree of processes.

Each process identified by a process identifier (pid). New processes are created with [[Fork()]] and [[Exec()]] to replace process memory space.

## Resource allocation
1. Obtain resources directly from OS
2. Constrained to subset of resources of parent process
    1. Can be done by partitioning resources or sharing resources amongst children

Scenario 2 prevents event where process overloads system by creating too many child process.

## Execution order
1. Parent continues to execute [[Concurrency]] with children
2. Parent waits until some or all of children to terminate

## Address space
1. Child process is a duplicate of parent process (same program and data)
2. Child process has new program loaded

---
Links: 