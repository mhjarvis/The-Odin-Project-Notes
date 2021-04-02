<h1 align=center>----- Links -----</h1>

<h1 align=center>----- Data Types -----</h1>

## Numbers

    1 + 1               //addition
    2 - 1               //subtraction
    2 * 2               //multiplication
    10 / 5              //division
    2 ** 2              //exponent
    8 % 3               //modulus

### Integers and Floats
Integers are whole numbers, scuh as 5 or 21. Floats are numbers that contain a deciml point, such as 10.5 or 2.34. Keep in mind that doing arithmetic with two integers will always return an integer. Substitute a float to get accurate results:

    17 / 5              //returns 3
    17 / 5.0            //returns 3.4

### Converting Number Types
When converting from a float to an integer, Ruby will drop any decimal places. There is no rounding that takes place. Converting an integer to a float:

    13.to_f             //13.0

Converting from a float to an integer:

    13.0.to_i           //13

### Checking Even/Odd
Some useful methods for working with numbers:

    6.even?             //true
    7.even?             //false

    6.odd?              //false
    7.odd?              //true

## Strings
Can be formed with either single (string literals) or double quotes. Note that string interpolation and the escape characters only work within double quotes.

### Concatenation
There are multiple ways to concatenate strings:

    "Welcome " + " "friend."
    "Welcome " << "my " << "friend."
    "Welcome ".concat("my ").concat("friend.")

### Substrings
Accessing strings inside strings can be achieved in several ways:

    "hello"[0]              //"h"
    "hello"[0..1]           //"he"
    "hello"[0, 4]           //"hell"
    "hello"[-1]             //"o"
    
### Escape Characters
Escape characters allow you to add representations into your string without ending it:

    \\              //creates a "\"
    \b              //backspace
    \r              //carriage return
    \n              //new line
    \s              //space
    \t              //tab
    \"              //double quotation mark
    \'              //single quoration mark
    
### Interpolation
Interpolation allows you to evaluate a string that contains placeholder variables. Make sure to use double quotes:

    name = "Markus"
    
    puts "Hello, #{name}"           //"Hello, Markus"
    puts 'Hello, #{name}'           //"Hello, #{name}"





## Review
1. List the basic arithmetic operators and what they do.
2. Describe the difference between an integer and a float and how to convert between the two.
3. Explain string interpolation and concatenation.
4. Describe what escape characters are, and list several examples.
5. Define what a symbol is and how it differs from a string.
6. Explain what the Booleans true, false, and nil represent.
















