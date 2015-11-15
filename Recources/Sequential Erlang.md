##Sequential Erlang

###Conditional Evaluations

The if construct looks like a case without the conditional-expression and the of keyword:

    if
     Guard1 -> expression11, expression12, .. ; Guard2 -> expression21, expression22, .. ; ... ;
     Guardn -> expressionn1, expressionn2, ..
    end
    
The guard expressions  are evaluated in turn **one after another** until one evaluates to **true**. 

The result of the complete if expression is the result of this sequence.

**A runtime error** is generated if none of the guards evaluates to the atom true, .

###Guards

Guards are additional constraints that can be placed in a function clause—either a case or a receive clause . 

Guards are placed before the -> separating the clause head from the body.

A guard consists of a when keyword followed by a guard expression.

The clause will be selected only if the pattern matches and the guard expression evaluate to the atom true.

The individual guard expressions can be built using the following constructs:

* Bound variables
* Literal Erlang terms denoting data values including numbers, atoms, tuples, lists, and so forth
* Type tests, such as is_binary, is_atom, is_boolean, is_tuple, and so on
* Term comparisons using ==, =/=, <, >, and so on, as listed in Chapter 2
* Arithmetic expressions built using the arithmetical operators given in Chapter 2
* Boolean expressions as described in Chapter 2
* Guard built-in functions

Guard subexpressions resulting in a runtime error are treated as returning false. 

Erlang allows simple logical combinations of guards to be written in a different way:

• Separating individual guard expressions with a comma (,) gives their conjunction, 

so that such a sequence evaluates to true only if all expressions in the sequence evaluate to true.

• Separating individual expressions (or indeed, comma-separated conjunctions) with a semicolon (;) 

gives their disjunction, where the sequence evaluates to true if any expression evaluates to true.


###Input and Output

The io module provides input and output from an Erlang program.

To read a line from standard input, use 'io:get_line/1', which takes a prompt string (or atom) as its input:

    1> io:get_line("gissa line>"). gissa line>lkdsjfljasdkjflkajsdf. "lkdsjfljasdkjflkajsdf.\n"
    
It is also possible to read a specified number of characters:

    2> io:get_chars("tell me> ",2). tell me> er
    "er"
    
The most useful input function is 'io:read/1', which reads an Erlang term from standard input:

    3> io:read("ok, then>>").
    ok, then>>atom.
    {ok,atom}
    4> io:read("ok, then>>").
    ok, then>>{2,tue,{mon,"weds"}}. {ok,{2,tue,{mon,"weds"}}}
    5> io:read("ok, then>>").
    ok, then>>2+3. {error,{1,erl_parse,"bad term"}}
    
io:format takes the following:

• A formatting string (or binary) that controls the formatting of the arguments

• A list of values to be printed

The formatting string contains characters that are printed as they are with control se- quences for formatting.
Control sequences begin with a tilde (~), and the simplest form is a single character, indicating the following:

~c : 
An ASCII code to be printed as a character.

~f : 
A float to be printed with six decimal places.


~e : 
A float to be printed in scientific notation, showing six digits in all.

~w : 
Writes any term in standard syntax.

~p : 
Writes data as ~w, but in “pretty printing” mode, breaking lines in appropriate places, indenting sensibly, and outputting lists as strings where possible.


~W, ~P : 
Behave as ~w, ~p, but eliding structure at a depth of 3. These take an extra argument in the data list indicating the maximum depth for printing terms.

~B : 
Shows an integer to base 10.

[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 
