# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when multiple computations are happening out of order. Which means it any part of the program can e executed at any time without affecting the final outcome. Parallelism means that two processes or computations are happening at the same time or overlapping.

 The difference is that concurrency can be done on a single processor core as it doesn't need to run in parallell, while parallelism literally means that they run in parallell and needs more than one core.
 
 ### Why have machines become increasingly multicore in the past decade?
 > Because it is faster. To have more cores that can handle more streams of data means we don't have to make the single core much faster. This makes it more economic, power efficient and technologically easier to increase power of cpus.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > With more cores, you need good ways of utilizing all the performance given to you, concurrent execution is a technique that simplifies this.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It makes it a little bit of both. Its easier because you can divide the computations over several cores and gives you more options for effiency, but harder because its harder to make different threads "talk to" eachother.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > A process is an instance of a program that is being executed. A thread is two sub parts of the same program. A green thread is a thread created by a runtime library instead of the OS kernel. Coroutine are components that enable pausing and resuming of unfinshed tasks in a program.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > `pthread_create()` - Creates a thread
 > `threading.Thread()` - Creates a thread
 > `go` - Creates a coroutine
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > GIL locks python to using only one thread
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Use multiprocessing module
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > It changes the number of threads go can use
