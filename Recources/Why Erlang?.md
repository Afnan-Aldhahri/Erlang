##Why Erlang?

#### High-Level Constructs 

Erlang is a declarative language. 

which means it describes what should be computed, not how this computation is calculated. 

Another aspect of Erlang is that functionsare first-class data. 

They can be bound to a variable and can be treated just like any other data item: stored in a list, returned by a function, or communicated between processes.


#### Concurrent Processes and Message Passing 

One of main reasons that make Erlang a very powerful programming language is its support or Concurrency.

Each Erlang process executes in its own memory space and owns its own heap and stack instead of using threads that share memory.

Processes can’t conflict with each other which leads to deadlocks ,race condition and other problems of concurrency .

Processes communicate with each other via message passing.

Note : message can be any kind of Erlang data type. 

Message passing is asynchronous, so once a message is sent, the process is not blocked . it can continue processing. 

What makes the concurrency more powerful is that :

Messages are retrieved from the process mailbox selectively. 

It is not obligatory to process messages in the order they are came to the mailbox.


####Scalable, Safe, and Efficient Concurrency 

#### Soft Real-Time Properties 

#### Robustness 

#### Distributed Computation 

#### Integration and Openness
