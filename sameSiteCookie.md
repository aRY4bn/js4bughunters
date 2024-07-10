*SameSite Cookie: 

This feature helps browsers determine whether a cookie should be sent with a cross-site request or not.

values of SameSite cookie: 
1- lax(default) 
2- strict
3- none 


1-strict:


In strict, the cookie is sent if the request is from the same origin, which is the safest possible state. 

In fact, the cookie is only sent in same origin requests.



2-lax:



In lax, the cookie is sent via same origin and cross origin, provided that the HTTP METHOD is GET request. 

The lax value is set by default in browsers.


3-none:

At none, a cookie is sent on all requests.
