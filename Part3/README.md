# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is that a single processor jumps between different threads so that it seems that two things are happening at the same time. Parallellism is that multiple cores work on different things at the same time. The difference is that with concurrency, it does not acutally happen at the same time. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Increased demand from programs. The increase of clock speed has slowed, so in order to keep up with the demands of programs we introduce multiple cores to share the work load. 
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Problems that require multiple things to happen at the same time. For eksample reading inputs while executing a program. Or doing something periodically, while also doing something else. Communication between devices running separate programs. 
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Depends on the problem about to be solved. Many problems will be very complicated without concurrency, while others do not require concurrency, and introducing concurrency will only complicate things. 
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Processes are the whole program that is solved. Threads are a concurrent way of solving multiple things in a program. Runs in OS. Green threads are threads which are run from software, and not OS. Coroutines are very similar to threads, although coroutines delegate recources and time recources back and forth voluentarily when they are ready to give it up. Threads are interrupted, and the recources are given to the other thread. 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Creates thread. 
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The Interpreter lock stops the different threads from using the Python interpreter simoultaneously. This hinders threads from running in parallell in Python. So that Python threads run sequentially instead of parallell. 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Threaded extensions in C. Cython. 
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > Changes the maximum number of active threads allowed. 
 
