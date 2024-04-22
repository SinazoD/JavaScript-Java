# JavaScript
JavaScript – Introduction

What is JavaScript?
JavaScript is a versatile programming language commonly used for enhancing web pages and creating interactive web applications. 
JavaScript allows developers to manipulate website content, respond to user actions, and create dynamic functionality such as animations, form validation and interactive maps.

It was originally designed for adding small amounts of interactivity to a page like hovers and animation, but now it is almost used for anything like including mobile applications, games and can be found in server applications. 

Common uses of JavaScript include:
•	Arlet messages
•	Popup windows 
•	Dynamic dropdown menus
•	Form validation. 
•	Displaying Date/time 

Client-side scripting 

•	JavaScript usually runs on the client-side (the browser’s side), as opposed to server-side scripting (on the webserver).
•	One benefit of doing this is performance. 
•	On the client side, JavaScript is loaded into the browser and can run as soon as it is being called or executed. 

An example on how you can write a text to a web page using JavaScript: 

Application Programming Interfaces (APIs)
•	One of the most useful aspects of JavaScript is that it enables us to make use of APIs. • An API is a set of code that allows us to simple commands and code to interact with an external service to complete coding tasks that would be very difficult to complete otherwise. 
•	When using an API, you are using the internet to collect data from your webpage or application, then send the collected data to a server where the data is handled and returned to you in a way that is easily readable or can be interacted with a meaningful way.
•	APIs are most found in one of two categories which are Browser APIs and Third-party APIs.
 
Browser APIs include: 
•	The Document object Model (DOM) allows you to apply new styles to a page by dynamically updating or removing HTML or CSS elements. 
•	The Geolocation API helps position you, enabling you to use something like Google Maps to Figure out where you and where you need to go.

 Third-party APIs are APIs that are not standard with your browser, often created by other companies or for very specific reasons. 
•	The Google Maps API, for example, will help you to embed a custom map into your website. 
•	The New York Times API enables you to take news stories from the New York times and integrate them into your webpages.

Features of JavaScript:

High-level Language: JavaScript abstracts away low-level details, making it easier to write and understand code.
Dynamic Typing: JavaScript employs dynamic typing, allowing variables to hold values of any data type without explicit declaration. For example, if you have stored the number value of a particular variable, you can update the variable’s value with the string.
Cross-platform compatibility: JavaScript is supported by all modern web browsers, making it a truly cross-platform language. Developers can write code once and have it work seamlessly on different devices, including desktops, tablets, and smartphones.
Object-oriented: JavaScript contains the classes, and we can implement all object-oriented programming concepts using its functionality.
It also supports inheritance, abstraction, polymorphism, encapsulation, etc, concepts of Object-oriented programming.
JSON: stands for JavaScript object notation. It is a widely used data format to exchange data between two networks. For example, server and client.
JavaScript also supports the JSON format to store the data.


Adding JavaScript
Much like the relationship between CSS and HTML you can either include JavaScript inline or externally. 
As a default you can use the following method using the defer attribute:
<!DOCTYPE html>
<html>
<head>
<script src =” my-file.js” defer></script>
</head>
<body>
<h1>I will be changed by JavaScript</h1>
</body>
</html>

The async and the defer can be described as the following:

•	async: The browser starts downloading the JavaScript in parallel to HTML (without being render-blocking) and executes the file immediately once it is done downloading.
•	 defer: The browser starts downloading the JavaScript in parallel to HTML (without being render-blocking) and only executes the file once all HTML is done rendering.

In short, we now had the benefit of starting the download of the file immediately, while still rendering the HTML while it is downloading. Due to the common usage of JavaScript today to modify HTML, you will use defer in most cases (while putting the <script> tag in the head of your HTML). This means that if we have an HTML element (for example an <h1> that we want to do something with we would use defer), we will add our JavaScript as follows:
 
<!DOCTYPE html>
<html>
   <head>
     <script src="my-file.js" defer></script>
   </head>
   <body>
     <h1>I will be changed by JavaScript</h1>
   </body>
</html>
 
Whereas, if we want to include a script that is not reliant on the HTML being present then we can use async:
 
<!DOCTYPE html>
<html>
   <head>
     <script src="my-file.js" async></script>
   </head>
   <body>
     <h1>I will **not** be changed by JavaScript</h1>
   </body>
</html>

It is important to note that async and defer are mutually exclusive. If you incorrectly apply both the one that is declared first will be used and the following attribute will be ignored. Additionally, also note that the above means that there is no reason to put JavaScript at the bottom of HTML anymore (although there are older codebases and libraries out there that still haven't caught up and still do this/recommend this).
 
There are still certain cases where you might want to put the script tag in the head of your HTML and forgo either async or defer. This is not recommended and usually indicates poor code architecture and deeper problems within the codebase, therefore should be avoided as far as possible. Yet, due to reasons out of your control, you might require the JavaScript to download and execute in a render-blocking manner. 

JavaScript – Variables

Variables
Variables are containers for storing data. These data values can be of different data types such as numbers, strings, Booleans etc.
JavaScript Variables can be declared in 3 ways:
•	Using var 
•	Using let 
•	Using const

Example 
var age = 25;
 let name = "John";
 const PI = 3.14; 


In the above example:
•	Age is a variable of type number,
•	Name is a variable of type string,
•	PI is a constant variable with a value of 3.14. 


Variables declared with var are function-scoped, while variables declared with let and const are block-scoped.

 
1. Variable Declaration: Here the variable is registered in its corresponding scope, the scope of a variable is simply where the variable can be used. We'll talk more about scope in another lesson.
 
These are examples of variable declarations:
 
var x;
var car;
var cup;
 
2. Variable Initialisation: This usually occurs automatically when a variable is declared. Here the variable is assigned a piece of memory or space by the JavaScript engine. Once a variable is declared, it takes a value of undefined even before assignment.
 
3. Variable Assignment: Variable assignment is usually the most important step when using a variable. Here the variable is assigned a value using the assignment operator "=". Values in JavaScript take one of the standard JavaScript data types which are:
•	String
•	Number
•	Boolean
•	Null
•	Undefined
•	Any of the complex data structures (arrays and objects)
var x         = 22; // Number
var name      = "Nate”; // String
var developer = true | false; // Boolean
var location = null; // Null
var blue; // Undefined
 
The syntax for assigning data types can be seen above with only strings having single or double quotes. A string is simply a series of characters used to represent text as opposed to numbers. Also, Boolean values are either true or false.
 
Naming Variables
 
When naming variables in JavaScript, there are certain rules to be followed, which are:
•	Names should begin with lowercase string.
•	Names cannot contain symbols or begin with symbols.
•	Names cannot begin with a number.
•	Names can contain a mix of uppercase strings, lowercase strings, and numbers.
 
Examples of variable names are:
 
// VALID
var dog;     
var warrior3;  
var blackPanther; // This is a way to name variables with several words (camelCase)

// INVALID
var 1cat;   
var -PewDiePie;  
 
Multiple variables in JavaScript can also be chained, while separated by a comma.
 
var x, y, z; 
 
Assigning values:
 
var x = 5, y = 6, z = 7;

var a = 10,
    b = 30,
    c = 90;
 
Variables in JavaScript can also evaluate simple mathematical expressions and assume the value. Here:
 
var x = 7 + 10 + 2;
console.log(x); // 19
 
After the first declaration of a variable using var, it is possible to declare it again. The variable will take the last assignment:
 
var age = 22;
var age = 38;

console.log(age) // 38
 
 
Now we shall have a look at the other variable types, let and const.
 
Let
 
Introduced in ES6, the variable type let shares a lot of similarities with var, but unlike var, it has scope constraints (scope is explained below). let is constrained to whichever scope in which it is declared. Its declaration and assignment are similar to var. let was introduced to mitigate issues posed by variables' scope which developers face during development.
 
In short, let helps us by making it easier to see where variables live in our code.
 
Declaring variables with let:
 
let x;
let x = 5; //results in an error as x can only be defined once when using let, unlike var
 
Multiple declarations can also be made with let:
 
let x, y, z;
x = 50, y = 20, z = 3; //don't use let again for the same variable name
 
Unlike var, variables cannot be re-declared using let, trying to do that will throw a Syntax error: Identifier has already been declared.
 
//var
var x = 20;
var x = 50;

console.log(x); // 50

//let
let x = 20;
let x = 50;

console.log(x); // SyntaxError: identifier "x" has already been declared.
 
Scope
 
let is only accessible in the block level in which it is defined. In the following example, everything within the curly brackets delimits a single code block. This means variables declared using let are only available within its code block and any descending code blocks. If let is declared within a code block it will not be available outside of that code block. This limitation is known as scope. For example:
 
if (true) {
 let a = 40;
 console.log(a); //40
}
console.log(a); // undefined
 
The scope of let is limited to the function in which it was declared. Let's look at another example:
 
let a = 50;
let b = 100;
if (true) {
 let a = 60;
 var c = 10;
 console.log(a/c); // 6
 console.log(b/c); // 10
}
console.log(c); // 10
console.log(a); // 50
 
As we can see in the example above, the value of let is limited to its scope. This modification to var goes a long way to providing a level of organisation while managing large data structures, as it is safer knowing that your variable cannot be reassigned anywhere in its scope.
 
Const
 
Also introduced in ES6, const is a variable type (although, it does not vary) assigned to data whose value cannot and will not be changed throughout the script. Now, this is stricter. const is also limited to the scope in which it operates. const is declared like var and let.
 
Use const when you are sure a variable will not be redeclared.
 
const x = 20; 
const y = 'dog';
const z = 'developer';
 
Note: A variable declared with const MUST be initialized with a value.
 
const x; // SyntaxError: missing initializer
 
Like var and let, variables declared with const can also be chained with commas separating each variable:
 
const x = 20, y = 50, man = true;
 
For different variable names, these variable types can all be used together depending on the development process.
 
Changing const
 
You are not allowed to change the value of a variable declared with const.
 
const a = 50;
a = 60; // shows error. You cannot change the value of const.

const b = "Constant variable";
b = "Assigning new value"; // shows error.
 
However, if you declare an object as const, you can change the properties. 
 
const person = {};

person.name = 'Nate'; // no error
 
Which to Use
 
When declaring variables, it is good practice to avoid using var. Always lean towards let or const based on the following rules:
•	Use let when we will be changing the value of the variable.
•	Use const when you are sure the variable won't change.
Using both let and const will keep our variables in the right scope and make our code easier to manage.
 
We have understood how variables are declared in JavaScript, and the differences between the variable types var, let and const. These variable types are unique in their own way and serve to make code development efficient. However, it is advised to use let whenever possible and const whenever the value of the variable is to remain constant.

Data Types

JavaScript has several data types that define the nature of values stored in variables. Understanding these data types is important for manipulating and working with data effectively.
Number
The number data type represents numeric values. It can be either an integer or a floating-point number.

let count = 10; // integer 
let price = 2.99; // floating-point number

String
The string data type represents a sequence of characters enclosed in single or double quotes.

let name = "Alice"; // using double quotes 
let message = 'Hello';// using single quotes

Boolean
The Boolean data type represents a logical value, either true or false. It is commonly used in conditional statements and comparisons.

let isTrue = true;
 let isFalse = false;

Undefined

Undefined is a data type that is automatically assigned to variables that have been declared but not initialized with a value.

let value; // undefined

Null

The null data type represents the intentional absence of any object value. It is often used to indicate that a variable has no value or is empty.

let result = null;

Object

The object data type represents a collection of key-value pairs. Objects can contain properties and methods which can be accessed using dot notation (.).

let person = { 
name: "John", 
age: 25, 
gender: "Male" 
};

Array

The array data type represents a collection of elements enclosed in square brackets ([]). Each element in an array is assigned a numeric index starting from zero.

let fruits = ["apple", "banana", "orange"];

Symbol

Symbols are a new primitive data type introduced in ECMAScript 2015. They are unique and immutable values that can be used as property keys in objects.

let id = Symbol("id");


