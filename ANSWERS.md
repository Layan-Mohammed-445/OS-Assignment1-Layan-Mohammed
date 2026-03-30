# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A process is a complete program that runs independently and has its own memory space, while a thread is a smaller unit of execution within a process that shares the same memory. One key difference is that processes do not share memory, but threads do, which makes communication between threads faster. Another difference is that creating a process has higher overhead compared to creating a thread, which is lighter and more efficient. In this assignment, we used threads by creating them with new Thread(process) in SchedulerSimulation.java, which allowed us to simulate multiple processes efficiently. Threads were more suitable because all processes needed to interact with shared structures like the ready queue and context switch counter.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it is paused and added back to the end of the ready queue. This is implemented in the code where the process is re-added using addProcessToQueue() if !process.isFinished().]

Example from my output:
```
[<img width="593" height="190" alt="image" src="https://github.com/user-attachments/assets/b48f9768-c86a-462d-8c1d-54b1ce294de7" />
]
```
P1 executing quantum [4000ms]
P1 completed quantum 4000ms │ Overall progress: 92%
Remaining time: 343ms
P1 yields CPU for context switch
P1 (Priority: 3) added to ready queue

**Explanation of example:**
[In this example, P1 used its full time quantum but still had remaining execution time, so it could not finish. Because of that, a context switch happened, and the CPU moved to another process. Then P1 was added back to the ready queue to wait for its next turn. This behavior is important because it ensures fairness, meaning all processes get a chance to run instead of one process taking all CPU time.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [P1 is in the New state when the thread is created using new Thread(process) in the addProcessToQueue() method, but before start() is called.]

2. **Runnable**: [P1 enters the Runnable state after Thread.start() is called in the main scheduling loop, meaning it is ready to run and waiting for CPU time.]

3. **Running**: [P1 is in the Running state when its run() method is executing, where it performs its time quantum and prints execution progress.]

4. **Waiting**: [P1 enters a waiting state when Thread.sleep() is called inside the run() method to simulate execution time, and also when the main thread calls Thread.join() to wait for it to finish its quantum.]

5. **Terminated**: [P1 reaches the Terminated state when its remainingTime becomes 0 and it finishes execution, after which it is added to the completed processes list.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Operating System CPU Scheduling]

**Description**: 
[Operating systems manage multiple processes running at the same time, and each process needs access to the CPU.]

**Why Round-Robin works well here**: 
[Round-Robin scheduling is useful because it ensures fairness by giving each process a fixed time quantum. This prevents any single process from monopolizing the CPU and keeps the system responsive. The same concept is applied in this assignment where each thread gets a limited execution time before a context switch occurs.]

### Example 2: [Web Server Handling Multiple Requests]

**Description**: 
[A web server handles multiple client requests at the same time, and each request can be processed by a separate thread.]

**Why Round-Robin works well here**: 
[Round-Robin helps distribute CPU time evenly between threads handling different requests, which improves responsiveness for users. It ensures that no single request blocks others for too long. This is similar to the simulation where processes take turns executing using a time quantum.]

---

## Summary

**Key concepts I understood through these questions:**
1. Difference between threads and processes
2. How Round-Robin scheduling works with a ready queue
3. Thread lifecycle and state transitions

**Concepts I need to study more:**
1. More details about context switching internally in the OS
2. Advanced thread synchronization and concurrency issues
