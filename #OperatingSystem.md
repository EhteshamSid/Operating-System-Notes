What is concurrency ?<br><br>
Concurrency is the execution of the multiple instruction sequences at the same
time. It happens in the operating system when there are several process threads
running in parallel.<br><br>
Explain the principles of concurrency ?<br><br>
Interleaved and overlapped processes can be viewed as examples of concurrent
processes, they both present the same problems.
The relative speed of execution cannot be predicted. It depends on the following:<br>
 The activities of other processes
 The way operating system handles interrupts
 The scheduling policies of the operating system<br><br>
What is interprocess communication ?<br><br>
Interprocess communication is the mechanism provided by the operating system
that allows processes to communicate with each other. This communication could
involve a process letting another process know that some event has occurred or
the transferring of data from one process to another.<br><br>
Explain process synchronization?<br><br>
Process Synchronization means coordinating the execution of processes such that
no two processes access the same shared resources and data. It is required in a
multi-process system where multiple processes run together, and more than one
process tries to gain access to the same shared resource or data at the same time.<br><br>
What is mutual exclusion?<br><br>
If a process is executing in its critical section, then no other process is allowed to
execute in the critical section.<br><br>
Give requirement of mutual exclusion?<br>
Requirements of Mutual exclusion Algorithm:<br>
No Deadlock:<br>
Two or more site should not endlessly wait for any message that will never arrive.<br>
No Starvation:<br>
Every site who wants to execute critical section should get an opportunity to
execute it in finite time. Any site should not wait indefinitely to execute critical
section while other site are repeatedly executing critical section<br>
Fairness:<br>
Each site should get a fair chance to execute critical section. Any request to
execute critical section must be executed in the order they are made i.e Critical
section execution requests should be executed in the order of their arrival in the
system.<br>
Fault Tolerance:<br>
In case of failure, it should be able to recognize it by itself in order to continue
functioning without any disruption.<br><br>
Explain the concept of semaphores?<br><br>
Semaphores are integer variables that are used to solve the critical section
problem by using two atomic operations, wait and signal that are used for process
synchronization.<br><br>
Explain the producer consumer problem?<br><br>
 The Producer-Consumer problem is a classical multi-process
synchronization problem, that is we are trying to achieve synchronization
between more than one process.<br>
 There is one Producer in the producer-consumer problem, Producer is
producing some items, whereas there is one Consumer that is consuming
the items produced by the Producer. The same memory buffer is shared by
both producers and consumers which is of fixed-size.<br>
 The task of the Producer is to produce the item, put it into the memory
buffer, and again start producing items. Whereas the task of the Consumer
is to consume the item from the memory buffer.<br><br>
What is a Deadlock ?<br><br>
 We know that processes need different resources in order to complete the
execution.<br>
 So in a multiprogramming environment, many processes may compete for a
multiple Number of resources.<br>
 In a system, resources are finite. So with finite number of resources, it is not
possible to fulfill the resource request of all processes.<br>
 When a process requests a resource and if the resource is not available at
that time. The process enters a wait state.<br>
 In multiprogramming environment, it may happen with many processes.<br>
 There is chance that waiting processes will remain in same state and will
never Again change state.<br>
 It is because the resource they have requested are held by other waiting
processes. When such type of situation occurs then it is called as Deadlock.<br><br>
What are the conditions for deadlock?<br><br>
1) Mutual Exclusion:<br>
 Two or more resources are non-shareable (Only one process can use at a
time)<br><br>
2) Hold and Wait:<br>
 A process is holding at least one resource and waiting for resources.<br><br>
3) No Pre-emption:<br>
 A resource cannot be taken from a process unless the process releases the
resource.<br><br>
4) Circular wait:<br>
 A set of processes are waiting for each other in circular form.<br><br>
What are resource allocation graphs ?<br><br>
The resource allocation graph is the pictorial representation of the state of a
system. As its name suggests, the resource allocation graph is the complete
information about all the processes which are holding some resources or waiting
for some resources.<br><br>
What are various stages of deadlock?<br><br>
What is deadlock detection and recovery?<br><br>
Deadlock Detection :<br>
 1. If resources have a single instance –<br>
In this case for Deadlock detection, we can run an algorithm to check for the cycle
in the Resource Allocation Graph. The presence of a cycle in the graph is a
sufficient condition for deadlock. <br>
2. In the above diagram, resource 1 and resource 2 have single instances. There is
a cycle R1 → P1 → R2 → P2. So, Deadlock is Confirmed.<br>
3. If there are multiple instances of resources –<br>
Detection of the cycle is necessary but not sufficient condition for deadlock
detection, in this case, the system may or may not be in deadlock varies according
to different situations.<br>
Deadlock Recovery :<br>
A traditional operating system such as Windows doesn’t deal with deadlock
recovery as it is a time and space-consuming process. Real-time operating systems
use Deadlock recovery.<br>
Killing the process –<br>
Killing all the processes involved in the deadlock. Killing process one by one. After
killing each process check for deadlock again keep repeating the process till the
system recovers from deadlock. Killing all the processes one by one helps a system
to break circular wait condition.<br>
Resource Preemption –<br>
Resources are preempted from the processes involved in the deadlock, preempted
resources are allocated to other processes so that there is a possibility of
recovering the system from deadlock. In this case, the system goes into starvation.<br><br>
Explain Dining Philosophers Problem in detail?<br><br>
The dining philosopher's problem is the classical problem of synchronization
which says that Five philosophers are sitting around a circular table and their
job is to think and eat alternatively. A bowl of noodles is placed at the center of
the table along with five chopsticks for each of the philosophers. To eat a
philosopher needs both their right and a left chopstick. A philosopher can only
eat if both immediate left and right chopsticks of the philosopher is available.
In case if both immediate left and right chopsticks of the philosopher are not
available then the philosopher puts down their (either left or right) chopstick
and starts thinking again.<br><br>
Give the memory management requirements?<br><br>
Memory management keeps track of the status of each memory location,
whether it is allocated or free. It allocates the memory dynamically to the
programs at their request and frees it for reuse when it is no longer needed. <br>
These Requirements of memory management are:<br>
 Relocation<br>
 Protection<br>
 Sharing<br>
 Logical organization<br>
 Physical organization<br><br>
What is memory partitioning explain in detail ?<br><br>
Memory partitioning means dividing the main memory into chunks of the same or
different sizes so that they can be assigned to processes in the main memory.<br>
There are two types of memory partitioning techniques:<br>
 Fixed-sized memory partitioning: In fixed-sized memory partitioning, the
main memory is divided into blocks of the same or different sizes. Fixed-size
memory partitioning can take place before executing any processes or
during the configuration of the system.<br>
 Variable-sized memory partitioning: It is used to alleviate the problem
faced by Fixed Partitioning. In contrast with fixed partitioning, partitions are
not made before the execution or during system configure.<br><br>
What are different memory allocation strategies ?<br><br>
 Static Memory Allocation: Static memory allocation is performed when the
compiler compiles the program and generate object files, linker merges all
these object files and creates a single executable file, and loader loads this
single executable file in main memory, for execution. In static memory
allocation, the size of the data required by the process must be known
before the execution of the process initiates.<br>
 Dynamic Memory Allocation: Dynamic memory allocation is performed
while the program is in execution. Here, the memory is allocated to the
entities of the program when they are to be used for the first time while the
program is running.<br><br>
What is virtual memory ?<br><br>
Virtual Memory is a storage allocation scheme in which secondary memory can be
addressed as though it were part of the main memory.<br><br>
What is demand paging ?<br><br>
Demand paging is a process of swapping in the Virtual Memory system. In this
process, all data is not moved from hard drive to main memory because while
using this demand paging, when some programs are getting demand then data
will be transferred.<br><br>
What are the differenty page replacemenmt policies?<br><br>
First In First Out (FIFO) –<br>
This is the simplest page replacement algorithm. In this algorithm, the operating
system keeps track of all pages in the memory in a queue, the oldest page is in the
front of the queue.<br>
 Optimal Page replacement –<br>
In this algorithm, pages are replaced which would not be used for the longest
duration of time in the future.<br>
Least Recently Used –<br>
In this algorithm, page will be replaced which is least recently used.<br><br>
What is thrashing?<br><br>
Thrashing occurs when a computer's virtual memory resources are overused,
leading to a constant state of paging and page faults, inhibiting most
application-level processing. It causes the performance of the computer to
degrade or collapse.<br><br>
What is file organization?<br><br>
File organization refers to the way data is stored in a file. File organization is very
important because it determines the methods of access, efficiency, flexibility and
storage devices to use. <br><br>
