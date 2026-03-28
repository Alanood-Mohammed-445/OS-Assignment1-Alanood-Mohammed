# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
 A process is an independent program with its own memory space, while a thread is a smaller unit of execution within a process that shares the same memory.
Threads are more lightweight and faster to create compared to processes, which require more system resources.
Communication between threads is easier because they share memory, whereas processes need more complex methods like inter-process communication.
In this assignment, threads were used because they allow efficient multitasking without the overhead of creating multiple processes.
This made the program faster and more responsive while using fewer resource
---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
In Round-Robin scheduling, if a process does not finish within its assigned time quantum, it is paused and moved to the end of the ready queue.
The CPU then gives the next process in the queue a chance to execute.
This cycle continues until all processes complete their execution.
For example, if Process P1 was given 2 milliseconds but needed more time, it would run for 2 ms, then be placed at the back of the queue while another process like P2 gets the CPU.
Later, P1 will get another turn and continue execution from where it stopped.

Example from my output:

  ظئـ P17(priority:4)added to ready queue ظ¤é Burst time: 6372ms
```

**Explanation of example:**
the process dosnt finish in spisfic time
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

1-New: P1 is in the New state when it is first created in the program but has not started execution yet. At this point, the thread object exists but has not been scheduled by the CPU.
2-Runnable: P1 becomes Runnable after it is started and placed in the ready queue. In this state, it is ready to run and waiting for its turn to be assigned CPU time.
3-Running: P1 is in the Running state when the scheduler selects it and it is actively executing on the CPU during its time quantum.
4-Waiting: P1 enters the Waiting state if it needs to wait for a resource or if it is paused after its time quantum expires in Round-Robin scheduling, waiting for its next turn.
5-Terminated: P1 reaches the Terminated state after it has completed its execution and no longer needs CPU time. The thread is finished and removed from the system

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

Example 1: Web Server Handling User Requests

Description:
A web server receives many requests from users at the same time, like loading web pages or API requests. Each request can be handled by a separate thread.

Why Round-Robin works well here:
Round-Robin scheduling gives each request an equal amount of CPU time. This prevents a single request from taking over the processor for too long. It also makes responses faster for all users because each request gets a chance to run regularly, even under heavy server load.

### Example 2: [Name of application/scenario]

Example 2: Multi-User Operating Systems

Description:
In a multi-user operating system, multiple users can work on the same machine or server at the same time, and each program runs in its own thread or process.

Why Round-Robin works well here:
Round-Robin ensures fairness by giving each user’s program a turn on the CPU. It also provides predictable response times, making the system feel fast and interactive for all users simultaneously.

## Summary

**Key concepts I understood through these questions:**
1. multithreading
2. round-robin
3. contextswitch

**Concepts I need to study more:**
1. git push
2. readyqueue
