# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:A thread is a smaller unit of execution that operates inside a process and shares memory, whereas a process is an independent program with its own memory and system resources. Threads are quicker and lighter than processes, which are heavy and need more time to make.

Since every task in this assignment shares the same ready queue and scheduling logic, threads were used in place of processes. Faster communication and reduced overhead are made possible by using threads.

Performance in this CPU scheduling simulation is also enhanced by the fact that context switching between threads is quicker than between processes.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:A process is paused and put back at the end of the ready queue in Round-Robin scheduling if it does not complete within its time quantum. This guarantees that every process has an equal opportunity to run.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
P1 completed quantum 3000ms
Remaining time: 4267ms
P1 yields CPU for context switch
P1 added to ready queue │ Burst time: 7267ms │ Priority: 3
```

**Explanation of example:**
This example shows that process P1 did not finish execution within the given time quantum, so it yielded the CPU and was re-added to the queue. It will run again later when its turn comes. This behavior ensures fairness and prevents any process from monopolizing the CPU.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: When the thread is formed using new Thread (process) prior to execution starting, P1 is in the New state. [When is P1 in New state?]

2. **Runnable**: The thread enters the Runnable state after using start(), which indicates that it is prepared to run but is awaiting CPU allocation. [When does P1 become Runnable?]

3. **Running**: When P1 is given time by the CPU and runs inside the run() method, it enters the Running state. [When is P1 Running?]

4. **Waiting**: When Thread.sleep() is used to mimic execution time, P1 goes into the Waiting state. [When/why would P1 be Waiting?]

5. **Terminated**: As can be seen in the output when it prints that the process has completed execution, P1 enters the Terminated state when its execution is complete and its remaining time is zero. [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer: Real-World Applications**

### Example 1: Web Server

**Description**: 
A web server handles multiple client requests simultaneously.

**Why Round-Robin works well here**: 
Round-Robin scheduling ensures fairness by giving each request a time slice, which improves responsiveness and prevents any single request from blocking others.

### Example 2: Operating System Scheduling

**Description**: 
Operating systems manage multiple processes running at the same time.

**Why Round-Robin works well here**: 
It ensures that each process gets equal CPU time, which improves system responsiveness and prevents starvation, similar to the behavior observed in the simulation.

---

## Summary

**Key concepts I understood through these questions:**
1. Difference between threads and processes
2. Round-Robin scheduling behavior
3. Thread lifecycle and execution

**Concepts I need to study more:**
1. Thread synchronization
2. Deadlocks
