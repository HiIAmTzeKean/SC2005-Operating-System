---
tags: 🌱
alias: SJF, SRTF
date: 04--Jul--2022
---

# Shortest job first

CPU prioritize [[Process]] based on CPU burst length. If there is a tie, [[First come first serve|FCFS]] is used to determine.

## Difficulty in predicting CPU burst
In reality, there is not way of knowing the next CPU burst cycle, but we can approximate the next burst length as an **exponential average**.

$\tau$ being the prediction, $t$ being the actual burst time, and $\alpha$ the weight adjustment for each component. This way, we use historical data to estimate the next burst length.
$$\tau_{n+1} = \alpha t_n + (1-\alpha) \tau_n$$

## Types of SJF
- For [[Non-preemptive scheduling]]
    - When core is given to process, it cannot be pre-empted until completed
    - Scheme is known as SJF
- For [[Preemptive scheduling]]
    - When a newly created process in ready queue has shorter CPU burst length than running process, process will be preempted
    - This requires the scheduler to check the ready queue each time a process is added to the ready queue
    - Scheme is known as SRTF

## Advantage
- Most optimal in minimising [[Waiting time]]
    - Longer processes execute last, shorter processes are not held up

## Disadvantage
- Starvation
    - Long process will not have the chance to run
- Impossible to estimate CPU burst time
    - For the same given process running in the same hardware, the hardware state is not consistent and thus, the burst time is not consistent, making the implementation tough.

---
Links: 