
# REST

A Representational State Transfer (REST) API works by allowing clients to interact with a server using standard HTTP methods (GET, POST, PUT, DELETE) to perform CRUD (Create, Read, Update, Delete) operations on resources. Here's a basic overview of how it works:

### Client-Server Architecture: 
REST APIs follow a client-server architecture where the client sends requests to the server, and the server processes those requests and sends back responses.

### Resources: 
Resources are the key abstraction in a REST API. They represent entities or objects that the client wants to interact with. Each resource is identified by a unique URI (Uniform Resource Identifier).

### HTTP Methods: 
RESTful APIs use HTTP methods to perform actions on resources:

* GET: Retrieve a representation of a resource.
* POST: Create a new resource.
* PUT or PATCH: Update an existing resource.
* DELETE: Delete a resource.

### Uniform Interface: 
REST APIs provide a uniform interface between clients and servers, allowing different clients to interact with the same server using standardized methods and data formats.

### Stateless Communication: 
RESTful APIs are stateless, meaning each request from a client to the server must contain all the information necessary for the server to understand and fulfill the request. The server does not store any client state between requests.

### Representation: 
Resources are represented in a format such as JSON or XML, which is transferred between the client and server. Clients and servers negotiate the format using content negotiation (e.g., Accept and Content-Type headers).

### Hypermedia as the Engine of Application State (HATEOAS): 
This principle suggests that the API should provide links or hypermedia controls in the response, allowing clients to navigate the available actions dynamically without prior knowledge of all the endpoints.

### Security: 
REST APIs can implement various security measures such as authentication (e.g., OAuth, JWT) and authorization to control access to resources.

### Conclusion: 
Overall, a REST API provides a flexible and scalable way for clients to interact with server resources over the web.
