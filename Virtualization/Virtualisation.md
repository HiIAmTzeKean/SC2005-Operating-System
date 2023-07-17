---
tags: 🌱
date: 30--Oct--2022
---

# Virtualisation

Uses software called [[Hypervisor]] to create abstraction of hardware.
- Hardware is divided into [[Virtual machines]]

## Benefits
- Allows efficient utilisation of hardware through cost-effective sharing
- Technology that supports cloud computing where hardware can be rented when needed

## Challenges
- Virtual management layer is needed which is additional overhead
- [[Real time operating system|RTOS]] cloud computing systems require bounded worse case time predictability which is not easily achieved with the overhead

## Types
The type of virtualisation determines if the hypervisor interacts directly or indirectly with hardware
- [[Type 1 virtualisation]]
- [[Type 2 virtualisation]]

## Virtualisation level
- Full virtualisation
    - Guest OS runs unmodified on [[Hypervisor]] → does not know of hypervisor existence
    - Full abstraction of hardware
- Para-virtualisation
    - Guest OS is modified and uses an API provided by hypervisor to interact with hardware
    - In this case, Guest OS is aware of hypervisor existence and there is less cost in abstracting hardware instructions allowing for a more efficient system

---
Links: 