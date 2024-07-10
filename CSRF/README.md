CSRF => Cross Site Request Forgery 


This vulnerability occurs when an attacker forces an end user to perform an unwanted action on a portal that has already performed authentication and has a valid session. 
In fact, the purpose of CSRF is to change an action in a request that goes to the server.


CSRF Example:
   - reset password 
   - email changes 
   - upload profile pictures
   - change mobile number

go to submit.html : 


There is a page with a submit button where the normal user has to enter something:

In fact, the attacker can copy the entire page of the source code and enter the URL address that he wants the client to send to the request in the action part of the form tag, so that the CSRF attack takes place.


form method="post" action="https://target.tld/update" id="csrf">


But this attack has a problem, and that is that when the client clicks on the button, he will enter the target page and will notice this attack. 

Now, the attacker must use the iframe tag so that the VICTIM does not notice this attack. Thus:

iframe style="display:none;" name="csrf-form"></iframe> 


form method="post" action="https://target.tld/update" id="csrf" target="csrf-form">


Now, when the VICTIM clicks on the button, the target page will no longer be displayed for him and he will not notice this CSRF attack.

*CSRF Preventation: 

   - set nonce( CSRF-Token in body)   // wordpress
   - check referrer
   - set custom header like JWT , CSRF-Token
   - SameSite Cookie



*Bypass CSRF Prevenation:

    - remove  token value => "token :f136803ab9c241079ba0cc1b5d02ee77"
    - set valid token value (not expired!)
    - change method (GET => POST , POST => OPTION) and change simple request to preflight request
    - algorithm
    - remove field : &_request_token=sadsadsa& 
    - Bypass with another attacks : CORS Misconfiguration , XSS
