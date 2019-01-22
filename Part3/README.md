# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is that a computer program multitasks by jumping between the tasks. Parallelism is that a computer program multitasks by performing both tasks at the same time. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > The rate of computer speed increase has decreased in the last couple years, and therefore it is a solution to add more cores to increase overall speed. 
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Problems that are independent and need to be run at the same time. For example checking inputs at the same time as calculating output. 
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It depends on the computer program. Concurrency increases complexity if it is not a problem that will be easier with concurrency. Creating redundent concurrency will not make your life easier. But some problems become significantly easier with concurrency.  
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Process is a instance of a computer program that needs to be solved. A thread is what the program is executing. You may have multiple threads. A thread is run from the OS while a green thread is run from software. A coroutine is similar to a thread, although the coroutines vouluentarily gives up control to each other when they are ready, while control is taken from threads and given to the others. 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Creates a thread. 
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > It does not interpret concurrently for different threads. It forces one thread to run for a while, then interprets the code, and then gives control to another thread. It makes threads work in serial in stead of parallell. 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Cython. Using threads from C but using Python code. 
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The maximum number of allowed threads. 
