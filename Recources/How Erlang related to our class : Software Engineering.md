##How Erlang related to our class : Software Engineering?


As we studied at the beginning of the Software Engineering class ,

Software life cycle in general consist of these main steps: 

* Feasibility; Development of a Business Plan

* Requirements Analysis and Specification

* Design

* Implementation and Integration

* Operation and Maintenance

The software engineers start writing the code according to the client's requirements in the **Implementation** step .

and here comes the importance of  **programming languages** .

There is no **one perfect** programming language that guarantee to solve any problem.

The software developer has to choose the right programming language for that specific problem.

There are a lot of programming languages out there .However , I chose Erlang for [these]  (https://github.com/Afnan-Aldhahri/Erlang/blob/master/Recources/Why%20Erlang%3F.md) reasons ,

And to make the topic even related to what we were studying in our class, I tried to focus on [Concurrency](https://github.com/Afnan-Aldhahri/GO/blob/master/Resources/Concurrency.md) feature of Erlang.

As we study in the class, Concurrent programming is always difficult since it require to implement correct access to shared variables .

Moreover , Concurrent programming can leads to many problems like race condition, memory barrier and dead lock. 
However , in Erlang , the only problem that could occur is dead lock and that’s because the only way for process to communicate is by passing and receiving massages so there is no chance for race condition to happen.

The **dead lock** can happen when the process loops and **blocks** waiting for receiving a massage .

You will notice there are many **common concepts** between **Erlang** and **Elixr** (the language that we studied in class)

like : Creating Processes , Passing and Receiving Messages .

This is expected because Elixr is build on Erlang VM ,exactly as how clojure built on Java VM.



[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 

