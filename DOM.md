DOM => Document Object Model 

 -HTML => Static 
 
 
 -DOM => api 


*DOM is an api that connects the js with the html of the page. 


*Actually, all tags and html codes are stored as documents in js and js can access it with DOM. 


*In fact, DOM takes files with html and xml extensions and turns them into an object that js can recognize. In fact, tags in html are known as elements in js

 
More:


The Document Object Model (DOM) is a programming interface for web documents. It represents the structure of a document (like an HTML or XML file) as a tree of objects, where each object corresponds to a part of the document. This model allows programs and scripts (like JavaScript) to dynamically access and update the content, structure, and style of documents.
JS use api(DOM) to connect with HTML


Relationship between HTML and DOM:


  -HTML is static and defines the content and structure of a webpage.

  
  -DOM is an API that allows JavaScript to interact with and manipulate HTML.






JavaScript utilizes the DOM API to connect with and manipulate the HTML of a page. Through the DOM, JavaScript can:


Access and modify the structure of the document.
Change the content of the elements.
Add or remove elements dynamically.
Handle events triggered by user actions.
Transforming HTML into a DOM Tree
When a browser loads an HTML document, it parses the HTML file and converts it into a tree of objects, known as the DOM tree. In this tree:



HTML tags become elements.
The attributes of tags become properties of the elements.
The text inside tags becomes text nodes.
This tree structure allows JavaScript to navigate through the document and manipulate it easily.



Example: Accessing and Modifying the DOM
Consider the following HTML snippet:


<!DOCTYPE html>
<html>
<head>
  <title>Document Object Model Example</title>
</head>
<body>
  <h1 id="header">Hello, World!</h1>
  <p>This is an example paragraph.</p>
</body>
</html>


JavaScript can access and modify this document using the DOM API. For example:


javascript:
            // Access the element with the id 'header'
            const header = document.getElementById('header');
            
            // Change the content of the header element
            header.textContent = 'Welcome to the DOM Example';
            In this example, document.getElementById('header') accesses the <h1> element, and header.textContent modifies its content.



-----------------------------------------------------------------------------------------------------------------------------------------------------------------



CRP => Critical Rendering Path

The Critical Rendering Path (CRP) is the sequence of steps the browser takes to convert HTML, CSS, and JavaScript into a webpage that the user can interact with. It determines which parts of the page should be rendered first based on priority. Understanding the CRP can help optimize web performance.


In fact, each browser has a CRP for itself, which determines which part of the page should be rendered first based on its priority.



DOM : Source & Sink



*DOM Source => Where data is received or input into the DOM. Examples include: 
  - document.url
  - location.hash 
  - xhr.responseText



*DOM Sink => Where data is output or rendered in the DOM. Examples include:
  - document.write()
  - innerHTML
  - postMessage


These concepts help identify potential security vulnerabilities, such as Cross-Site Scripting (XSS), where malicious scripts might exploit how data flows from sources to sinks.