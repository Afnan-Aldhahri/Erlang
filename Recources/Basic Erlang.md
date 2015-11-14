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
  
+ and – can be used as unary operators in front of expressions of the format Op Expression, such as –18 or +18.5.
 
Operations on integers alone always result in an integer.
  
Using div will result in an integer without a remainder, which has to be computed separately using the rem operator. 

All mathematical operators are left-associative. 

The unary + and − have the highest precedence; multiplication, division, and remainder have the next highest precedence; 

and addition and subtraction have the lowest precedence.

