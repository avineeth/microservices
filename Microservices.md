#### What is Microservice?
Is an architectural style, where application is build as small independent services instead of a large monolithic  service.
- Loosely Coupled
- Independently deployable and testable

#### Spring cloud vs Spring boot
Spring cloud is collection of libraries or solutions which allow you to implement the microservices patterns
Like service discovery, configuration, loadbalancing
Spring boot is a java based framework which helps in building Microservices.
- Embedded server to avoid complexity in application deployment
- Metrics, Health check, and externalized configuration

#### Challenges with Microservices
- Co-ordirnating changes with other microservices teams.
- Operational Overheads with an increase in no. of processes.

#### Multi-tenant architecture, why would you use one?
- It is a model where any tenant can be served by any compute node and they share the computing resources.
- They enable horizontal auto-scaling, enhanced resilience, and zero-downtime upgrades

##### How can you connect customers to their data in a multi-tenant architecture, if every customer has their own database?
By introuducing a lookup-table that looks up tenant configuration based on a unique id, like hostname

#### Service Discovery in Microservice Netflix Eureka

- Let’s imagine that you are writing some code that invokes a service that has a REST API or Thrift API. In order to make a request, your code needs to know the network location (IP address and port) of a service instance. In a traditional application running on physical hardware, the network locations of service instances are relatively static. For example, your code can read the network locations from a configuration file that is occasionally updated.

- Service instances have dynamically assigned network locations. Moreover, the set of service instances changes dynamically because of autoscaling, failures, and upgrades. Consequently, your client code needs to use a more elaborate service discovery mechanism.

- There are two main service discovery patterns: client‑side discovery and server‑side discovery. 

###### Client‑side discovery.

- When using client‑side discovery, the client is responsible for determining the network locations of available service instances and load balancing requests across them. The client queries a service registry, which is a database of available service instances. The client then uses a load‑balancing algorithm to select one of the available service instances and makes a request.

- Netflix Eureka is good example of a service registry. It provides a REST API for registering and querying service instances. A service instance registers its network location using a POST request. Every 30 seconds it must refresh its registration using a PUT request. A registration is removed by either using an HTTP DELETE request or by the instance registration timing out. As you might expect, a client can retrieve the registered service instances by using an HTTP GET request.
