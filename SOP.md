SOP => Same Origin Policy


A security policy in web browsers that prevents unrestricted access to resources between websites. This policy ensures that scripts running on a web page can only access data that comes from the same origin.

Same Origin Concept : 
1.Protocol 
2.Port 
3.Host

In order for the addresses to be of the same origin, the above 3 conditions must be met. 

Example:

https://example.com

https://example.com/home/about.php  SOP


http://www.example.com              Not SOP  => protocol


https://example.com:81              Not SOP  => port


https://www.example.com             Not SOP  => host




* Why is SOP important? Prevent XSS and CSRF attacks


* How to bypass SOP:

1-Tags that do not follow SOP:


img
script
iframe
...

Example: 

If a web developer puts a verify-token.js in the root of his web directory for his login panel, the attacker can read it. How? Attacker can read it by using tags like img and script.


<!-- <img src=https://target.tld/home/user1/verify-token.js > -->



2-CORS Misconfiguration: 


3-Use JSONP:

It is a method using the script tag and loading JS data from an external server.


<script src="http://attacker.tld/info.js"></script>


