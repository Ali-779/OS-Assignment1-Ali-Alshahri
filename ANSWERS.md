# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:A thread is a smaller unit of execution within a process that shares memory with other threads, whereas a process is an independent program with its own memory space and system resources. Because they need less overhead to construct and manage than processes, threads are regarded as lightweight, according to Operating System Concepts. Since every process in this assignment is a member of the same scheduling simulation and shares the same ready queue and data structures, we employed threads. Separate processes would necessitate more complicated inter-process communication. The simulation is more effective and manageable thanks to threads.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved back to the end of the ready queue so other processes can run. This behavior is clearly shown in my output.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:▶ P1 executing quantum [5000ms] Remaining time: 383ms ↻ P1 yields CPU for context switch ➕ P1 added to ready queue
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
In this instance, process P1 utilized the entire time quantum (5000 ms) yet had 383 ms left over. As a result, it was returned to the ready queue after failing to complete. Additionally, we can observe that the queue changes as follows after P1 is added again:

[P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P11 → P1].

P1 was positioned near the back of the line, as this indicates. Afterwards, it receives CPU time once again and completes when the remaining time is reduced. This conduct adheres to the Round-Robin algorithm, which guarantees process fairness.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [P1 is in the New state when it is first created in the code using:
new Thread(process)

This happens before it is added to the ready queue.]

2. **Runnable**: [After P1 is added to the queue and start() is called, it becomes Runnable. This means it is ready to run and waiting for CPU scheduling.]

3. **Running**: [P1 enters Running state when the scheduler selects it and we see:
▶ P1 executing quantum [5000ms]

This means the CPU is currently executing P1.]

4. **Waiting**: [During execution, P1 uses Thread.sleep() to simulate running time. At this moment, the thread goes into Waiting state temporarily. This happens during:
⚡ Quantum progress: [███████████████] 100%]

5. **Terminated**: [Finally, P1 enters Terminated state when it finishes execution completely, as shown in the output:
▶ P1 executing quantum [383ms]
Remaining time: 0ms
✓ P1 finished execution!

This means the process has no remaining time and the thread is finished.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Internet server]

**Description**: 
[Several user requests are handled concurrently by a web server.]

**Why Round-Robin works well here**: 
[No request has to wait too long because it allots a reasonable amount of time to each one.]

### Example 2: [Operating System]

**Description**: 
[Numerous programs are simultaneously run by the operating system.]

**Why Round-Robin works well here**: 
[It maintains system responsiveness by distributing CPU time equally among apps.]

---

## Summary

**Key concepts I understood through these questions:**
1. The operation of threads
2. The operation of Round-Robin scheduling
3. How CPU time is shared by processes

**Concepts I need to study more:**
1. Alternative algorithms for scheduling
2. Synchronization of threads
