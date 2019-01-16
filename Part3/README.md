# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 Concurrent, perceived to run at the same time. parallelism is actually at the same time, but needs multicore system. 
 
 ### Why have machines become increasingly multicore in the past decade?
 Because we have reached a limit in computing power with regards to energy usage.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 Concurrency lets you do things at the same time. 
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 It is more complicated, but you gain better functionality. Easier to run when they are separate.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 Threads communicate through shared memory, whilst processes do not.
 Green threads are threads scheduled by a runtime library or VM.
 Coroutines are scheduled using cooperative multitasking.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
  green threads
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > Only one thread can operate on python objects and Python/C APi functions at one time.
 Works great for single core computers, but not multicore.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Eventlet is capable of concurrency.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > GOMAXPROCS sets the maximum number of CPUs that can be executing
 simultaneously and returns the previous setting. If n < 1, it does not change the current setting.
 This call will go away when the scheduler improves.
