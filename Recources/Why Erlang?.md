##Why Erlang?

#### High-Level Constructs 

Erlang is a **declarative** language. 

which means it represents **what** should be computed, not **how** this computation is calculated. 



#### Concurrent Processes and Message Passing 

One of main reasons that make Erlang a very powerful programming language is its **support for Concurrency**.

Each Erlang **process** executes in its own memory space and have its own heap and stack instead of using threads that share memory.

Processes can’t conflict with each other ,so no race condition and other problems of concurrency .

Processes communicate with each other via **message passing**.

*Note* : message can be any kind of Erlang data type. 

Message passing is **asynchronous**, so once a message is sent, the process is not blocked . it can continue processing. 

What makes the concurrency more powerful is that :

Messages are retrieved from the process mailbox **selectively**. 

It is not obligatory to process messages in the order they are came to the mailbox.


####Scalable, Safe, and Efficient Concurrency 

Erlang concurrency is **fast and scalable**. 

The processes are **lightweight**. Its even lighter than thread.

processes are created, scheduled, and handled in the **VM**, separate from the operating system. 

Therfore, process creation time is so small . 

Erlang processes communicate with each other through message passing. Regardless of the number of concurrent processes in your system, exchanging messages within the system takes *microseconds*.

Copying  data from the memory space of one process to the memory space of the other is all within the same virtual machine. 


#### Soft Real-Time Properties 

Erlang can be used  for tasks with **soft real-time constraints**. 

Erlang can handle high loads with no declination in throughput , and the reason is 

Storage management in Erlang is *automated*, with garbage collection implemented on a perprocess basis. 



#### Robustness 

• Erlang processes can be **linked together** so that if one crashes, the other will be knowing about the crash, and then can either handle the  crash or choose to crash itself.

• OTP provides a number of collective behaviors, such as servers, finite state machines, and event handlers. 

• These  behaviors are linked to a **supervisor** behavior.

The task of this supervisor is to monitor and handle process termination.

• Using this *supervision* and *linking*, Erlang programmers can concentrate on programming for the correct case, and can let the process fail in any other circumstances. 


#### Distributed Computation 

Erlang has **distribution incorporated** into the language’s syntax and semantics.

The default distribution mode is based on **TCP/IP** , allowing a node to connect to any other node running on any operating system. 

As long as these *nodes* are **connected** through a **TCP/IP network** , the result is a  meshed network of nodes, where all the nodes can communicate with each other.

Because distribution built into the language ,you can simply distribute your processes across **a cluster of computers** because the  syntax of sending a message within a local node is the same as sending it to a remote node.


#### Integration and Openness

Erlang is an **open language** allowing you to integrate legacy code or new code .
 
Therfore, there are mechanisms for interworking with C, Java, Ruby, and other programming languages, including Python, Perl, and Lisp.

**External languages** can be added using drivers that are linked into the Erlang runtime system .

**High-level libraries** allow Erlang nodes to communicate with nodes executing Java or C, 

making them appear and behave like  distributed Erlang nodes. 

[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 
