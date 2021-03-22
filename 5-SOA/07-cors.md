* CORS
    * Stands for cross origin resource sharing 
    * is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources.
* Single Origin Policy
    * Browser security prevents a web page from making requests to a different domain than the one that served the web page. 
    * Default Policy
    *  CORS is actually relaxing this security feature by allowing other domains to make requests to your server
* CSRF
    * Cross-site request forgery (also known as CSRF) is a web security vulnerability that allows an attacker to induce users to perform actions that they do not intend to perform. It allows an attacker to partly circumvent the same origin policy, which is designed to prevent different websites from interfering with each other. 
    * Common vulnerability in cookie based systems (yet another good reason to use tokens!)
* Adding Cors 
    * For Windows hosting accounts, create or modify the web.config file in the directory where you want to permit CORS requests. Add the following lines to the web.config file: in the custom header