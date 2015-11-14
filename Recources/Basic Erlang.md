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
'January' 'a space' 'Anything inside quotes{}#@ \n\012' 'node@ramone.erlang-consulting.com'


#####  Booleans
There are no separate types of Boolean values or characters in Erlang. Instead of a Boolean type, the atoms true and false are used together with Boolean operators. They play the role of Booleans in being the results of tests, and in particular, comparisons:
1> 1==2. false
2> 1<2. true
3> a>z.
false
4> less<more. true
Atoms are ordered in lexicographical order. We give more details of these comparisons later in this chapter. Erlang has a wide variety of built-in functions, usually called BIFs in the Erlang community, which can be used in your programs and in the shell. The built-in function is_boolean gives a test of whether an Erlang value is a Boolean:
5> is_boolean(9+6). false
6> is_boolean(true). true
