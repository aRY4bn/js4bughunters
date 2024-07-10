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
