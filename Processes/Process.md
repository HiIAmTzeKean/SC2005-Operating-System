---
tags: 🌱
date: 14--Jul--2022
---

# Process

An **active entity** where the status is represented by the **program counter** specifying next instruction to execute and a set of associated resources.

> [!note]
> A [[Program]] itself is not a process. [[Program vs Process]]

## Process in memory

![[process layout.png]]

- Text section
    - Executable code
- Data section
    - Global variables
- Heap section
    - Memory for dynamic memory allocation
- Stack section
    - Temporary data storage
    - When function is called, an **activation record** containing all **local variables** and return address pushed to stack
    - Activation record popped from stack when control is returned

Size of text and data section are statically fixed while heap and stack can shrink and grow dynamically during execution.

---
Links: 