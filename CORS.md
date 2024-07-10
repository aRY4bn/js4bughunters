CORS => Cross Origin Resource Sharing 


CORS is a solution for sharing and access from different origins. In CORS, it is determined which origins can make requests to the server.


Types of requests in CORS: 


There are two types of requests in CORS: 

Simple Request and Preflight Request. 

These two request types are used to manage the security of cross-domain requests.


Simple Request:

    methods:
    
    - GET
    - POST
    - HEAD 

header:

   - Accept: 
   - Accept-language: 
   - Content-Type:


Simple Request is a type of request that does not require a preflight stage. Because Random Custom Header has not been used. 

Random-Custom-Header: CSRF-Token, JWT ...



Preflight Request:


It is a kind of CORS request that is sent before the main request to specify a random custom header!

 methods: 
 
       - OPTION
       - PUT


A: Attacker.tld
B: target.tld


For example, in the CORS server B, it is determined that the origins of A can send requests to it.


Request Header : 

      - origin : 

Response Header: 

    - Access-Control-Allow-Origin:
    - Access-Control-Allow-Credential: //Permission to send cookies and... on request
    - Access-Control-Allow-Methods:
    - Access-Control-Allow-Header:


Example: 


If we type origin: test.com on the target.tld site in our browser and in our request, and these headers are set in the response like this:


response headers: 

    -Access-Control-Allow-Origin: test.com 
    -Access-Control-Allow-Credential: True


In this case, this site is vulnerable and CORS is not set well. Of course, the CORS vulnerability is worth it when we can extract critical information. 

Of course, also consider this, when these response headers are set, it should be noted that no other random custom has been set:


Random Custom header => JWT , CSRF-Token


origin: test.com => {

             -Access-Control-Allow-Origin: test.com
             -Access-Control-Allow-Credential: True 
            // no custom header like JWT , CSRF Token
}



*Browser Solution for CORS Misconfiguration :


If the attacker puts origin: test.com in his request header and the response headers he receives from the server are as follows:


origin: test.com => { 

          - Access-Control-Allow-Origin: * 
          - Access-Control-Allow-Credential: True
} 


The browser itself stops sending the cookie with the request header! 
If Access-Control-Allow-Credentials is true, the value of Access-Control-Allow-Origin cannot be *. 
This is because it is not security-friendly to allow all (*) origins with credentials.



*CORS Misconfiguration Vulnerability:


It is considered a very dangerous vulnerability because the attacker can obtain sensitive information such as Seesion and apikey, etc.


How to diagnose: By checking the important headers, namely Access-Control-Allow-Origin and Access-Control-Allow-Credential! 


By changing the Access-Control-Allow-Origin header to the attacker's origin and testing again



