Vertical scaling, or increasing the amount of CPUs or capacity in a single machine !!! GO is here 
Horizontal scaling, or increasing the number of machines to expand capacity

Is webservice a web application?

Web application is a computer program that responds to an HTTP request by a client and sends back HTML back to client in an HTTP response

In other words, a program needs to fulfill only two criteria to be considered a web app:

1.  program must return HTML to a calling client that renders HTML and displays to a user.
2.  data must be transported to the client through HTTP.

if a program doesn’t render HTML to a user but instead returns data in any other format to another program, it is a web service


HTTP is a stateless, text-based, request-response protocol that uses the client-server computing model.

Request-response is a basic way two computers talk to each other. The first computer sends a request to the second computer and the second computer responds to that request. A client-server computing model is one where the requester (the client) always initiates the conversation with the responder (the server). As the name suggests, the server provides a service to the client. In HTTP, the client is also known as the user-agent and is often a web browser. The server is often called the web server.

Having said that, HTTP 1.1 does persist connections to improve performance.

CGI (Common Gate Interface)
SSI (Server side includes)


A method is considered safe if it doesn’t change the state of the server
A method is considered idempotent if the state of the server doesn’t change the second time the method is called with the same data

