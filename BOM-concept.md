BOM => Browser Object Model 


 - browser , version , width , height ,... 
 - window is object of BOM and document is object of DOM 
 - DOM is a object of DOM
 - important methods of BOM : 
    alert() , confirm() , prompt() , setInterval() , setTimeout()


In fact, BOM is a higher part of DOM and DOM can be an object of BOM.
(window.document == document) => True


more: 

What is the BOM?


The Browser Object Model (BOM) provides a way to interact with the browser itself, beyond the content of the web page. The BOM includes objects like the window object, which represents the browser window, and other objects that provide information about the browser and allow control over its features.



Key Components of the BOM


Browser Information: The BOM allows access to information about the browser, such as the name, version, screen width, and height.
Window Object: The window object is the global object for JavaScript in the browser. It represents the window in which the browser displays a document.


Important Methods: The BOM includes several methods that provide interactions with the browser:


alert(): Displays an alert box with a message and an OK button.


confirm(): Displays a dialog box with a message, an OK button, and a Cancel button.


prompt(): Displays a dialog box that prompts the user for input.


setInterval(): Calls a function or evaluates an expression at specified intervals (in milliseconds).


setTimeout(): Calls a function or evaluates an expression after a specified number of milliseconds.


Relationship Between BOM and DOM


The window object is a part of the BOM and represents the browser window.

The document object is part of the DOM and represents the web page loaded in the window.

The DOM itself can be considered an object within the BOM, as window.document provides access to the DOM.

javascript
// This expression evaluates to true
console.log(window.document === document); // true


Example: Using BOM Methods


Consider the following examples of BOM methods in action:

javascript


// Display an alert box
alert('Hello, World!');

// Display a confirmation dialog
const userConfirmed = confirm('Do you agree?');
if (userConfirmed) {
  console.log('User agreed.');
} else {
  console.log('User did not agree.');
}

// Prompt the user for input
const userInput = prompt('Please enter your name:');
if (userInput !== null) {
  console.log(`Hello, ${userInput}!`);
}

// Execute a function every 2 seconds
setInterval(() => {
  console.log('This message appears every 2 seconds.');
}, 2000);

// Execute a function after 3 seconds
setTimeout(() => {
  console.log('This message appears after 3 seconds.');
}, 3000);


Summary:


The Browser Object Model (BOM) is a higher-level abstraction that allows interaction with the browser beyond just the document content. Key components of the BOM include the window object and its methods like alert(), confirm(), prompt(), setInterval(), and setTimeout(). The DOM, which represents the document structure of a web page, is an object within the BOM, allowing seamless interaction between JavaScript and the HTML content. Understanding both the BOM and the DOM is crucial for creating dynamic and interactive web applications.






