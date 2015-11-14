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


###Built-in Functions
###Recursion
