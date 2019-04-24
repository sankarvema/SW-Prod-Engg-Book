# REST - REpresentative State Transfer

Representational state transfer (REST) is a style of software architecture. As described in a dissertation by Roy Fielding, REST is an "architectural style" that basically exploits the existing technology and protocols of the Web.

## Principles



## Considerations

There are 6 key constraints to think about when considering whether a RESTful API is the right type of API for your needs:

1. Client-Server: This constraint operates on the concept that the client and the server should be separate from each other and allowed to evolve individually.
2. Stateless: REST APIs are stateless, meaning that calls can be made independently of one another, and each call contains all of the data necessary to complete itself successfully.
3. Cache: Because a stateless API can increase request overhead by handling large loads of incoming and outbound calls, a REST API should be designed to encourage the storage of cacheable data.
4. Uniform Interface: The key to the decoupling client from server is having a uniform interface that allows independent evolution of the application without having the application’s services, or models and actions, tightly coupled to the API layer itself.
5. Layered System: REST APIs have different layers of their architecture working together to build a hierarchy that helps create a more scalable and modular application.
6. Code on Demand: Code on Demand allows for code or applets to be transmitted via the API for use within the application.

## REST vs. RESTful vs. RESTless

1. REST is an architecture style while RESTful or REST API is the implementation of webservices following REST architecture style
2. 'RESTless' as any system that is not RESTful. For that it is enough to not have one characteristic that is required for a RESTful system

## REST APIs

Unlike SOAP, REST is not constrained to XML, but instead can return XML, JSON, YAML or any other format depending on what the client requests. And unlike RPC, users aren’t required to know procedure names or specific parameters in a specific order.

### HETEOS - Hypermedia As The Engine Of Application State

With HATEOAS, a client interacts with a network application whose application servers provide information dynamically through hypermedia. A REST client needs little to no prior knowledge about how to interact with an application or server beyond a generic understanding of hypermedia


### References
- REST API maturity model by Richardson https://martinfowler.com/articles/richardsonMaturityModel.html
