---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: Monitor mode
date: 10--Aug--2022
---

# Kernel mode

Also known as monitor mode, or supervisor mode.

## Purpose

For execution of OS process which is a [[Privileged instruction]] type.

## Difference between root/admin

Kernel mode is a hardware operation mode (there is a hardware bit in CPU that keeps track of the current mode)

Root/admin mode is a user account in the OS. Jobs are done in [[User mode]] even in root mode. But root users are able to **indirectly execute code in kernel mode**.

---
Links: 