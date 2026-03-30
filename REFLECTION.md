# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:** 

[From this assignment, I learned how multithreading works in a more practical way. Before this, I knew that threads allow multiple tasks to run, but I didn’t fully understand how scheduling actually happens. By using the Runnable interface and creating threads for each process, I saw how each process gets CPU time in parts using a time quantum. I also understood how join() is used to control execution order and simulate CPU scheduling instead of running everything randomly. Another important thing I learned is how context switching happens when one thread stops and another starts. Overall, this assignment helped me connect concepts like threads, scheduling, and CPU execution in a more realistic way.
]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[The most challenging part for me was integrating the new features (priority, context switch counter, and waiting time tracking) into the existing code. The code was already large, so it was difficult to figure out exactly where to place my changes without breaking the logic. I especially struggled with making sure the waiting time was calculated correctly because it depends on timing and when the process enters and leaves the queue. Also, I had some syntax errors at the beginning when adding new variables and methods. Another challenge was understanding how the process moves between the queue and execution, so I could update values at the correct time. Overall, it was a great challenge and i am glad to have done it.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[To overcome these challenges, I first tried to understand the flow of the program step by step, especially how threads are created and executed. I used print statements and the existing output to track what was happening during execution. For the waiting time feature, I carefully followed the logic of when a process enters the queue and when it starts running, and then updated the timing based on that. I also fixed syntax issues by checking errors and comparing with examples of the rest of the code. Sometimes I had to test small changes and run the program multiple times to make sure everything worked correctly. In general, breaking the problem into smaller parts helped me a lot.]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Multithreading is used in many real-world applications where multiple tasks need to run at the same time. For example, in operating systems, CPU scheduling works in a similar way to this assignment, where processes share CPU time using time slices. It is also used in applications like web servers, where multiple users can send requests at the same time and each request is handled by a different thread. Another example is in games or apps where background tasks (like loading or animations) run while the user is interacting with the interface. The concept of context switching is important in making systems efficient and responsive. This assignment helped me understand how these concepts are actually implemented in code.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
