<h1 align=center>----- Links -----</h1>

1. JavaScript.info: https://javascript.info/devtools
2. MDN JavaScript Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
3. Compatability Tables: https://caniuse.com/

<h1 align=center>----- Fundamentals -----</h1>

## Hello World!
#### The 'script' Tag
The ```<script>``` tag can be used to add JavaScript directly to the html document.

    <script src="/path/to/script1.js"></script>                 //using an absolute path
    <script src="https://something.script.js"></script>         //using url
    <script src="/path/to/script2.js"></script>                 //linking to multiple files

## Code Structure
#### Semicolons
Usually, but not always, a page break will indicate a semicolon (automatic semicolon insertion). However, the following would not produce a semicolon:

    alert(3 +                       //no semicolon is inserted due to ()
    1
    - 23);

Semicolons are also not assumed before square ```[]``` brackets. 

## The Modern Mode, 'use strict'
Inserted at the beginning of a document (or function/object/class) to make the script work the 'modern' way. The devloper console does not use ```use strict``` mode by default. 

## Variables
#### A Variable
Can begin with letters, '$', and '_ '. Cannot contain hyphens. Case matters. Variables are declared with the ```let``` keyword. Multiple variables can be declared on one line:

    let user = "Markus", age = 22, message = "Hi";          //same line declaration
    let user = "Markus"                                     //multiline declaration
        , age = 22,
        , message = "Hi";

#### var vs let
The ```var``` keyword has no block scope. For example, a variable declared in a if-then statement can be called outside that statement if declared with 'var' instead of 'let'.

#### Constants
To declare use ```const``` instead of ```let```. Constants that are known prior to execution should be named in all uppercase, while other constants can be named in camelCase.

## Data Types
#### Numbers
Consists of integers and floats. ```NaN``` represents a computational error caused by a incorrect or an undefined mathematical operation. ```NaN``` is sticky meaning that any further attempts on ```NaN``` will return ```NaN```. ```Infinity``` (or the - version) represent the mathematical Infinity. It is greater than any number.

    alert(1 / 0);                       //Infinity (division by zero)
    alert("not a number" / 2);          //NaN

#### BigInt
The 'number' type cannot represent values greater than 2^(53) - 1 or 9007199254740991. A ```BigInt``` is created by appending a ```n``` to the end of an integer:

    const bigOne = 238477474777474747457577575784n;

#### Strings
Strings can use '', "", ``. Backticks have 'extended functionality'. They allow for embeding variables and expressions into a string by wrapping them in ${...}. The expression inside ${...} is evaluated and the result becomes part of the string. In JavaScript there is no char type.

    let name = "John";
    alert( `Hello, ${name}!` );         //Hello, John
    alert( `the result is ${1 + 2}` );  //the result is 3

#### Boolean (logical type)
Boolean type has only two values: true, false.

#### The ```null``` Value
Null is a type of its own and only contains the null value. There is no reference, it is just null.

#### The 'undefined' Value
The meaning of undefined is 'value not assigned', as in ```let num;```. Use ```null``` instead of ```undefined``` if you want to set a value to empty.

#### Objects and symbols
Used to store collections of data. They are not primitive because they can store more than one thing. ```symbol``` is used to create unique identifiers for objects.

#### The ```typeof``` Operator
Returns the type of the argumentf. Can be used with or without parentheses.

## Interaction: alert, prompt, confirm
    alert("Hello");
    result = prompt(title, [default]);                  //title is the text shown to the visitor
                                                        //default is optional, it is the initial value for the input field



## Type Conversions (incomplete)
## Basic Operators, maths (incomplete)
## Comparisons (incomplete)
## Conditional Branching: if, '?' (incomplete)
## Logical Operators (incomplete)
## Nullish Coalescing Operator '??' (incomplete)
## Loops: while and for (incomplete)
## The 'switch' Statement (incomplete)
## Functions (incomplete)
One goal of functions is to avoid code duplication. If changes need to be made, you know where to modify it (at one location).

    function name(parameters) {
      ...body...
    }
    name("Mark");                                   //call function

#### Local Variables
Variables declared inside of a function are only visible inside that function.

    function printName(name) {
      let x = name;
      console.log(x);
    }
    printName("Mark");                             //'Mark'
    console.log(x);                                //error
    
#### Other Variables and Parameters
A Function, however, can access outside variables. It can also modify the outside variable. The outer variable is only used if there is no local one (inside the function). Functions also use parameters, in which case they are sent a copy of the passed parameter. 
    
    let name = "Mark";                              //global variable
    function printName() {                          //"Mark"
      console.log(name);                            //name is a function parameter
      name = "Mike";
      conosle.log(name);                            //"Mike"
    }
    
#### Default Values
If no parameter is provided, then its value becomes ```undefined```. If there is a parameter an no value is given for it, then it will get the value "no text given" (a string).
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    


## Function Expressions (incomplete)
Function expressions allow for use of the function before declaration.
## Arrow Functions, the Basics (incomplete)

Syntax for creating functions that can be better than full expressions.

    let sum = (a, b) => a + b;

    //this is the same as:

    let sum = function(a, b) {
        return a + b;
    };

If there is only one argument, the parentheses can be ommitted around parameters:

    let double = n => n * 2;

If there are no arguments, keep the parentheses. Arrow functions can also be used as Function Expressions. To dynamically create a function:

    let age = prompt("Your age: ", 18);
    let welcome = (age < 18) ?
        () => alert('Hello') :
        () => alert('Greetings!');
    welcome();

#### Multiline Arrow Functions (incomplete)
When using arrow functions for more complex situations, enclose in curly braces and use a normal return statement.

    let sum = (a, b) => {
        let result = a + b;
        return result;
    }












## JavaScript Specials(incomplete)



<h1 align=center>----- Code Quality -----</h1> (incomplete)
<h1 align=center>----- Objects: The Basics -----</h1> (incomplete)
<h1 align=center>----- Data Types -----</h1> (incomplete)
<h1 align=center>----- Advanced Working with Functions -----</h1> (incomplete)
<h1 align=center>----- Object Properties Configuration -----</h1> (incomplete)
<h1 align=center>----- Prototypes, Inheritance -----</h1> (incomplete)




<h1 align=center>----- Classes -----</h1>

(incomplete)

## Class Basic Syntax(incomplete)
#### The "class" Syntax
The basic ```class``` syntax is:

    class MyClass {
        //methods
        constructor() {...}
        method1() {...}
        method2() {...}
        method3() {...}
        ...
    };
    
To create a new object of the class with all the listed methods:

    new MyClass();
or

    let myObj = new MyClass();
The ```constructor()``` method is automatically called by ```new```.

    class User {                                        //code can be shortened as the following:
      constructor(name) {                                 
        this.name = name;                                 class User {  
      };                                                    constructor(name) {this.name = name;}
                                                            sayHi() {alert(this.name);}
      sayHello() {                                        }
        alert(this.name);
      };
    };
Note that within classes, there are no requirements for commas, as they will return an error.

#### What is a Class?
A class, in JavaScript, is a type of function. Above, ```class User{...}``` does the following:

1. It creates a function named ```User```. This becomes the result of the class declaration. Function code is taken from the constructor (which is assumed as empty if there is no constructor.
2. It stores class methods, such as ```sayHello()``` in ```User.prototype```. After creation, when methods are called, they are called from the ```prototype```.

Referencing the class object above:

    alert(typeof User);                                     //'function'
    alert(User === User.prototype.constructor);             //'true'
    alert(User.prototype.sayHello);                         //'alert(this.name);'
    alert(Object.getOwnPropertyNames(User.prototype));      //'constructor, sayHello'

#### Not just a Syntactic Sugar
There are reasons for declaring a class (instead of a function).
1. A function created by ```class``` is labeled as ```[[FunctionKind]]:"classConstructor"```. 
2. A class must be called with ```new```.
3. Class methods are non-enumerable (a class sets the enumerable flag to false for all methods in 'prototype').
4. Classes always ```use strict```.

#### Class Expression
Classes can be defined inside other expressions, passed around, returned, assigned, etc. A class expression:
    
    let User = class {
      sayHi().{
        alert("Hello");
      }
    };
Class expressions can have a name, but that name is visible only inside the class:

    let User = class MyClass {
      sayHi() {
        alert(MyClass);
      }
    };
    
    new User().sayHi();                     //works
    alert(MyClass);                         //error
Classes can be made dynamically 'on-demand', like this:

    function makeClass(phrase) {
      //declare a class and return it
      return class {
        sayHi() {
          alert(phrase);
        }
      };
    }
    
    let User = makeClass("Hello");
    new User().sayHi();                     //'hello'
    
#### Getters/Setters
Classes can include getters/setters, computed properties, etc.

    get name() {
      return this._name;
    }
    set name(value) {
      if(value.length < 4) {
        alert("Name is too short.");
        return;
      }
      this._name = value;
    }
    ...
    let user = new User("John");
    alert(user.name);                       //'John'
    user = new User("");

#### Computed Names[...]
A computed method name using brackets [...]:

    class User {
    
      ['say' + 'Hi']() {
        alert("Hello");
      }
    }
    
    new User().sayHi();                     //'Hello'
    
#### Class Fields
Class fields is syntax that allows users to add properties. Adding the ```name``` property:

    class User {
      name = "John";
      
      sayHi() {
        alert('Hello, ${this.name}!');
      }
    }
    
    new User().sayHi();                     //'Hello, John!'
Class fields are set on individual objects, not ```User.prototype```. We can also assign values using more complex expressions ans function calls:

    name = prompt("Name, please?", "John");
###### Making bound methods with class fields
If an object method is passed around and called in another context, ```this``` won't be a refrnce to its object any more. For example, this will show ```undefined```:

    class Button {
      constructor(value) {
        this.value = value;
      }
      click() {
        alert(this.value);
      }
    }
    
    let button = new Button("hello");
    setTimeout(button.click, 1000);         //undefined
    
It is called "loosing ```this```". I can be fixed by either:
1. Pass a wrapper-function, such as ```setTimeout(() => button.click(), 1000).
2. Bind the method to object (the constructor).

Class fields also has special syntax. The class field ```click = () => {...}``` is created on a per-object basis. There will be a seperate function for each ```Button``` object, with ```this``` referencing that object. We can pass ```button.click``` around anywhere, and the value of ```this``` will always be correct. *This is especially useful for in browser environments, for event listeners.* Example:

    class Button {
      constructor(value) {
        this.value = value;
      }
      click = () => {
        alert(this.value);
      }
    }
    
    let button = new Button("hello");
    setTimeout(button.click, 1000);             //'hello'


## Class Inheritance (incomplete)
#### 
text...


##  Static Properties and Methods (incomplete)
#### 
text...


## Private and Protected Properties and Metthods (incomplete)
#### 
text...


## Extending Build-in Classes (incomplete)
#### 
text...


## Class Checking: "instanceof" (incomplete)
#### 
text...


## Mixins (incomplete)
#### 
text..



<h1 align=center>----- ES6 Modules -----</h1> (incomplete)
## The Node Package Manager (npm)
The npm is a command line tool giving access to a software repository that includes plugins, libraries, and tools. It consists of three components:
1. The website - used to discover packages, set up profiles, etc.
2. The Command Line Interface - main way to interact with the npm.
3. The registry - a large public database of JavaScript software and the meta-information surrounding it.











<h1 align=center>----- Error Handling -----</h1> (incomplete)
<h1 align=center>----- Promises, async/await -----</h1> (incomplete)
<h1 align=center>----- Generators, Advanced Iteration -----</h1> (incomplete)
<h1 align=center>----- Modules -----</h1> (incomplete)
<h1 align=center>----- Miscellaneous -----</h1> (incomplete)








JavaScript uses two kinds of types: primitive and reference. 
1. Primitive types are stored as simple data types (there are 5): Boolean, Number, String, Null, Undefined. Variables that hold a primitive directly contain the primitive value.
2. Reference types are stored as objects, which are really just references to locations in memory. Variables that hold references hold a pointer to the location in memory where the value is stored.
To identify primitive data types we can use the ```typeof``` operator (exception is ```null```).

    console.log(typeof "Markus");       //'string'
    console.log(typeof 23);             //'number'
    console.log(typeof true);           //'boolean'
    console.log(typeof undefind);       //'undefined'
    console.log(typeof null);           //'object'

    console.log(value === null);        //true or false (best way to determine is a value is null)



### Comparisons
Note the difference between using ```==``` and ```===```. The tripple equals does the comparison of two items without coercing the item to another type, as in:

    console.log("5" == 5);                  //true
    console.log("5" === 5);                 //false
    console.log(undefined == null);         //true
    console.log(undefined === null);        //false


# Functions

///
///

### Arrow Functions








# Constructors
Constructors should be named with a capital first letter and executed only with the 'new' operator. Any function can be used as a constructor (used with new). 
    
    function User(name) {
      this.name = name;
      this.isAdmin = false;
    
    let user = new User("Fred");
When a function is executed with ```new``` it does the following:

1. A new empty object is created and assigned to this.
2. The function body executes. Usually it modifies ```this```, adds new properties to it.
3. The value of ```this``` is returned.

### Return Statement in Constructors
If there is a ```return``` statement and:
1. It is called with an object, then the object is returned instead of this.
2. It is called with a primitive, it is ignored (```this``` is returned).

##### Dereferencing Objects
JavaScript is a garbage-collected language, but it is still good idea to dereference objects with null.

    let object1 = new Object();
    object1 = null;                     //dereference

##### Adding/Removing Properties
    let object1 = new Object();
    let object2 = object1;

    object1.myProp = "Hello";           //property also applies to object2 since both have pointers
                                        //to the same object

### Instantiating Built-in Types
    let items = new Array();
    let now = new Date();
    let error = new Error("Something happened here!");
    let func = new Function("console.log('Hi');");
    let object = new Object();
    let re = new RegExp("\\d+");

### Objects and Literals
A literal is syntax that allows you to define a reference value without explicityly creating an objet, using the ```new``` operator and the object's constructor. Object literals are made up of an identifier string, a colon, and a value, with multiple properties seperated by commas:

    var book = {
        name: "Markus",             //using identifiers
        "year": 1984,               //using strings literals (use if there are to be spaces)
    }

### Function Literals
Creating function using literal form is both easier and less error prone:

    function sq(val) {                                          //literal
        return val * val;
    }

    let sq = new Function("val", "return val * val;");          

# Property Access
Can access using dot notation or bracket notation:

    let array = [];                         //dot notation
    array.push(1);

    let array = [];                         //bracket notation
    array["push"](123);                     //allows for special characters in property names

    let array = [];                         //using variable instead of string literal
    let method = "push";
    array[method](123);

# Identifying Reference Types

    function reflect(value) {
        return value;
    }

    console.log(typeof reflect);            //'function'
    d
