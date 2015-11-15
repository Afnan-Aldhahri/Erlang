## What kind of applications is Erlang particularly suitable for ?

##### Distributed, reliable, soft real-time concurrent systems.

* Telecommunication systems, e.g. controlling a switch or converting protocols.

* Servers for Internet applications, e.g. a mail transfer agent, an IMAP-4 server, an HTTP server or a WAP Stack.

* Telecommunication applications, e.g. handling mobility in a mobile network or providing unified messaging.

* Database applications which require soft realtime behaviour.

Erlang is very powerful at solving these kinds of problems because this is the  domain it was originally designed for 

because Erlang has these characteristics:

* Erlang provides a simple and powerful model for error containment and fault tolerance (supervised processes).

* Concurrency and message passing are a fundamental to the language. Applications written in Erlang are often composed of hundreds or thousands of lightweight processes. Context switching between Erlang processes is typically one or two orders of magnitude cheaper than switching between threads in a C program.

* Writing applications which are made of parts which execute on different machines (i.e. distributed applications) is easy. Erlang's distribution mechanisms are transparent: programs need not be aware that they are distributed.

* The OTP libraries provide support for many common problems in networking and telecommunications systems.

* The Erlang runtime environment (a virtual machine, much like the Java virtual machine) means that code compiled on one architecture runs anywhere. The runtime system also allows code in a running system to be updated without interrupting the program.


[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 
