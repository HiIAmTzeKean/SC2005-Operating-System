---
tags:
  - 🌱
  - OS
  - ComputerScience
date: 11--Aug--2022
modified: 29--Oct--2023
---

# Interrupt

Interrupts are usually caused by external hardware component (Either I/O devices or CPU) to notify the CPU that an event requires servicing.

## Relation to [[System call]]

When an interrupt occurs, the interrupt line to the CPU is pulled low (interrupt line is active low) and CPU will switch from [[User mode]] to [[Kernel mode]].

The following actions are then taken
1. CPU will save current state by storing registers and PC then [[Context switch]]
2. CPU will locate the correct [[Interrupt service routine|ISR]] type from the [[Interrupt vector table]]
3. Run the ISR to service the interrupt
4. Switch back to User mode and continue executing

During the handling of an interrupt, we assume that all incoming interrupts are disabled to prevent loss of interrupts.

## Relation to OS

OS are interrupt driven, because if an interrupt does not occur, then the OS will not need to take over -> no interrupt means no event.

If OS is not interrupt driven then it will have to poll for event which takes up CPU computation time -> inefficient

---
Links: 