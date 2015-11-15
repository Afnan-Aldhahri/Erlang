##Basic Erlang

##### Integers

Integers in Erlang are used to denote whole numbers.

They can be positive or negative. 

The only limit on how large an integer can become depends on the physical constraints of the machine, namely the available memory.

Some examples of integers include:
−564 0 11 700000000

To express integers in a base other than 10, the Base#Value notation is used.

To express characters as ASCII values, the $Character notation is used.

$Character returns the ASCII value of Character.

$a represents the integer 97 and $A represents the integer 65. 

The ASCII value representation of a newline, $\n, is 10:
$a $A $\n

##### Floats

Floats in Erlang are used to represent real numbers. 

Some examples of floats :
17.368 −56.654 1.234E-10.

The E-10 is a conventional floating-point notation stating that the decimal point has been moved 10 positions to the left:

1.234E-10 is the same as writing 1.234×10−10, namely 0.0000000001234. 

Soft real-time aspects of telecom applications rarely rely on floats. 


##### Mathematical Operators

addition, subtraction, multiplication, and division can be implement on Ointegers and floats. 
  
(+ and – )can be used as unary operators in front of expressions of the format Op Expression, such as –18 or +18.5.
 
Operations on integers alone always result in an integer.
  
Using div will result in an integer without a remainder, which has to be computed separately using the rem operator. 

All mathematical operators are left-associative. 

The unary + and − have the highest precedence; multiplication, division, and remainder have the next highest precedence; 

and addition and subtraction have the lowest precedence.

##### Atoms

Atoms are constant literals that stand for themselves. 

To compare with other languages, the role of atoms is played by #define constants in C and C++, by “static final” values in Java, and by “enums” in Ruby.

The only operations on atoms are comparisons, which are implemented in a very efficient way in Erlang. 

The reason you use atoms in Erlang, as opposed to integers, is that they make the code clear yet efficient. 

Atoms start with a lowercase letter or are delimited by single quotes.

Letters, digits, the “at” symbol (@), the full stop (.), and underscores (_) are valid characters if the atom starts with a lowercase letter. 

Any character code is allowed within an atom if the atom is encapsulated by single quotes.

Examples of atoms starting with a lowercase letter include:
january fooBar alfa21 start_with_lower_case node@ramone true false

When using quotes, examples are :
'January' 'a space' 'Anything inside quotes{}#@ \n\012' 


#####  Booleans

There are no specific types of Boolean values in Erlang. 

Instead , the atoms true and false are used together with Boolean operators.

1> 1==2. false

2> 1<2. true

3> a>z. false

4> less<more. true

Atoms are ordered in lexicographical order.

The built-in function is_boolean gives a test of whether an Erlang value is a Boolean:

5> is_boolean(9+6). false

6> is_boolean(true). true

##### Tuples

Tuples are a composite data type used to store a collection of items.

These items can be any Erlang data values.

Tuples are bounded by curly brackets, {...}, and their elements are separated by commas.

Some examples of tuples include:
{123, bcd} {123, def, abc} {abc, {def, 123}, ghi} {} {person, 'Joe', 'Armstrong'} {person, 'Mike', 'Williams'}

The tuple {637,abcd} has two elements: the integer 637 and the atom abcd. 

The empty tuple {} has no elements. 

In a tuple, when the first element is an atom, it is called a tag. 

 This  helps in finding the reason of errors when the wrong tuple has been mistakenly passed as an argument or returned as a result of a function call. 
 
##### Lists
 
Lists are used to store collections of elements.

Lists and tuples are very different in the way that they can be processed.

Lists are bounded by square brackets, [...], and their elements are separated by commas.

Elements in lists do not have to be of the same data type and, just like tuples, can be freely mixed.

The empty list is denoted by [] .

Some examples of lists include:

[january, february, march] [123, def, abc] [a,[b,[c,d,e],f], g]

[{person, 'Joe', 'Armstrong'}, {person, 'Robert', 'Virding'}, {person, 'Mike', 'Williams'}]

[72,101,108,108,111,32,87,111,114,108,100] [$H,$e,$l,$l,$o,$ ,$W,$o,$r,$l,$d]


##### Characters and Strings

Characters are represented by integers, and strings (of characters) are represented by lists of integers.

The integer representation of a character is given by preceding the character with the $ symbol:

1> $A.
65

2> $A + 32.
97

3> $a.
97

There is no string data type in Erlang. 

The empty string "" is equivalent to the empty list [].
 
Strings are denoted by lists of ASCII values and represented using the double quotes(") notation.

So,the string "Hello World" is infact the list [72,101,108,108,111,32,87,111,114,108,100]. 


[Home] (https://github.com/Afnan-Aldhahri/Erlang/blob/master/README.md) 
