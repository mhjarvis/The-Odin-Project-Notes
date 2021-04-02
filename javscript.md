<h1 align=center>----- Links -----</h1>

1. https://javascript.info/

<h1 align=center>----- Fundamentals -----</h1>

## The "script" Tag

    <script src="/path/to/script.js"></script>                  //absolute path
    <script src="script.jss"></script>                          //relative path

## Interaction: alert, prompt, confirm

    alert("Hello");                             //"Hello"
    result = prompt(title, [default]);          //title is text shown to visitor, default (optional) is the initial value for the input field
    
    let isBoss = confirm("Are you the boss?");
    alert( isBoss );                            //true if OK is pressed
    
## Type Conversions

    let value = true;
    value = String(value);                      //value equals the string "true";
    
    value = "6" / "3";                          //conversion happens automatically and value equals 2 (int)
    let str = "123";
    let num = Number(str);                      //num equals the number 123
    
    alert( Boolean(0) );                        //false
    alert( Boolean("") );                       //false
    alert( Boolean("0") );                      //true
    alert( Boolean(" ") );                      //true

## Basic operators, maths
Operands are what operators are applied to. An operator is unary if it has a single operand (ex: - reverses the sign). A operator is binary if it has two operands (ex: 1 - 2).

    alert( "1" + 2);                            //"12"; only the + operator works like this
    alert( 2 + 2 + "1");                        //"41"
    alert( "1" + 2 + 2);                        //"122"
    alert( 6 - "2");                            //4
    
    alert( +true);                              //1; unary+ converts non-numbers
    alert( +"" );                               //0
    
    let apples = "2";
    let orangs = "3";
    alert( apples + oranges);                   //"23"
    alert( +apples + +oranges);                 //5
    
## Comparisons

    alert( 'Z' > 'A' );                         //true; string comparisons work
    alert( 'a' > 'A' );                         //true
    alert( 0 == false );                        //true; strict equality (==) cannot differentiate between ```0``` from ```false```
    alert( 0 === false );                       //false, strict equality (===) checks equality without type conversion
    alert( null === undefined );                //false
    alert( null == undefined );                 //true
    
## Conditional branching: if, '?'

    if(0) { ... }                               //falsy value; 0, "", null, undefined, and NaN become ```false``` (never execute);
    if(1) { ... };                              //truthy value
    
    let accessAllowed = (age > 18) ? true : false;              //returns true/false depending on condition
    let accessAllowed = age > 18 ? true : false;                //same as above
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
