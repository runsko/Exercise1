# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Both is a form of executing tasks at the same time. Parallelism uses multiple processes, creating true parallell executions. Concurrency "imitates" parallelism in such a way that it uses only one processor. Concurrency uses threads to running multiple processes at the same-ish time.
 
 ### Why have machines become increasingly multicore in the past decade?
 > To accomplish parallelism. Historically, decreasing the size of the chip has sped up the executions. However, as the transistors currently reside at near the minimal boundary, the increase in processing power does not increase as fast. Therefore, multiple processors can be used to emply parallelism and increase performance.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Any problem requiring multiple sub-problems to be solved at the same time. Concurrent solutions can also be more readable, scaleable and malleable.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Your answer here*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Process - program or large problem consisting of multible things.
 Thread - One independent sequence of actions. Process can use multiple threads. Threads within the same process can share memory.
 Green thread - Not a "real" thread. Not supplied by OS, can be supplied by the program.
 Coroutines - Similar to threads, however, coroutines only provide concurrency, not parallelism
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > thread, thread, coroutine
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The GIL prevents multiple python threads from accessing the same python object at the same time. This means the threads need to wait for the object to become available before it can be accessed. The need for the GIL is a result of python's memory management not being thread-safe. The GIL effectively limits python bytecode execution to a single core, regardless of how many python threads it is spread out on.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > multiprocessing library instead of threads
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The number of processors that can execute the program code simultaneously
