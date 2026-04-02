# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:I discovered how Java's Runnable interface is used to create and run threads. I realized that time slicing allows several threads to mimic concurrent execution even on a single CPU. Additionally, I learnt about the stages of the thread lifecycle, including New, Runnable, Running, Waiting, and Terminated. The way Thread.sleep() simulates execution latency was one key idea. I gained a better understanding of how operating systems effectively handle several jobs thanks to this assignment. Additionally, I became aware of how context switching enables equitable CPU sharing between programs.**

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:The hardest aspect was figuring out how the scheduler uses the ready queue internally. Understanding how processes transition between execution and waiting was first challenging. Because the waiting time feature required accurate timing calculations, its implementation was similarly difficult. I had to think hard about where to put the code within the run procedure. It was also difficult to debug timing-related problems. More consideration and testing were needed for this section.**

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:By carefully reading the code and thoroughly examining the program's output, I was able to overcome the difficulties. I made an effort to align the output with the code. Before integrating them, I also evaluated each feature independently. I tracked execution using basic debugging methods like printing values. I was able to grasp the topics better by going over the lecture notes and textbook explanations. Repetition and practice make things simpler.**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:Numerous real-world systems, including operating systems, games, and web browsers, use multithreading. A browser, for instance, uses threads to load several tabs simultaneously. Threads are used in games to manage physics, graphics, and input all at once. Scheduling algorithms are used by operating systems to effectively manage operations. Round-Robin scheduling contributes to responsiveness and fairness. This assignment demonstrated how these ideas are used in actual systems.**


[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

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
