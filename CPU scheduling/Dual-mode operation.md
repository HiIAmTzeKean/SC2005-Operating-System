---
tags: 🌱
date: 10--Aug--2022
---

# Dual-mode operation

OS runs dual mode that alternates between [[User mode]] and [[Kernel mode]].

## Purpose

- [[Memory protection]]
- [[IO protection]]

## Architecture

- Mode bit
    - Computer hardware to indicate the current mode
    - [[Interrupt]] or [[Trap]] causes the mode bit to switch to [[Kernel data]]

## Example

During run time in executing [[User process]], CPU will be in [[User mode]]. On [[Interrupt]] or [[System call]], the CPU will change to [[Kernel mode]] allowing it to access [[Privileged instruction]].

---
Links: 