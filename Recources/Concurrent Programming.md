
##Concurrent Programming

 
One of main reasons that make Erlang a very powerful programming language is its support or Concurrency.

Each concurrent activity in Erlang is called a process. 

Each Erlang process executes in its own memory space and owns its own heap and stack instead of using threads that share memory.

Processes communicate with each other via message passing.

Note : message can be any kind of Erlang data type.

Message passing is asynchronous, so once a message is sent, the process is not blocked . it can continue processing.

What makes the concurrency more powerful is that :

Messages are retrieved from the process mailbox selectively.

It is not obligatory to process messages in the order they are came to the mailbox.

#### Creating Processes

 To run concurrent code, we have to create **more than one process**. 
 
 we create process by spawning a process using the spawn(Module, Function, Arguments) BIF(built in function).
 
 The spawn BIF returns a process identifier as a **pid**.
 
Once spawned, a process will continue executing and remain alive until it terminates.

**Two way the proccess can be tirminated :**

1- Terminate normally : if there is no more code to execute .

2- Terminate abnormally : if a runtime error such as a bad match or a case failure occurs.

To find out what the currently executing processes in the runtime system are doing , we can use the shell command ' i() ' . 

It will print the process identifier, the function used to spawn the process,

and the function in which the process is currently executing.


#### Message Passing

Processes communicate with each other using **message passing**. 

Messages are sent using the Pid ! Message construct, where :

**Pid** : is a valid process identifier and

**Message** : is a value from any Erlang data type .

Each Erlang process has a **mailbox** in which incoming messages are saved.

When a message is sent, it is copied from the sending process into the recipient’s mailbox for retrieval.

Messages are saved in the mailbox in **the order in which they are delivered*.

If two messages are sent from one process to another, the messages are guaranteed to be received in the same order in which they are sent.

Sending a message will *never fail*.

Message passing is **asynchronous** : a sending process will not be suspended after sending a message; 

it will instead immediately continue executing the next expression in its code.


#### Receiving Messages

Messages are retrieved from the process mailbox using the *receive clause*. 

The **receive clause** is a construct bounded by the reserved words **receive** and **end**, and contains a number of **clauses**.

On executing the receive statement, the oldest message in the mailbox is pattern-matched against each pattern in the receive expression in turn:

• If a successful match occurs, the message is retrieved from the mailbox, 

  the variables in the pattern are bound to the matching parts of the message, and the body of the clause is executed.
  
• If none of the clauses matches, the subsequent messages in the mailbox are pattern- matched one by one against all of 

 the clauses until either a message matches a clause or all of the messages have failed all of the possible pattern matches.
 
 A receive statement will return the **last evaluated expression** in the body of the matched clause.
 
 When none of the clauses in a case statement match, a runtime error occurs.
 
 Each pattern consists of any valid Erlang term, including bound and unbound variables as well as optional guards.

To ensure that the receive statement always retrieves the first message in the mailbox you could use an unbound variable.

[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 
