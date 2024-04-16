# JavaScript-Java
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
