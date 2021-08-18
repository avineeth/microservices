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
- It is a model where in any tenant can be served by any compute node.
- They enable horizontal auto-scaling, enhanced resilience, and zero-downtime upgrades

##### How can you connect customers to their data in a multi-tenant architecture, if every customer has their own database?
By introuducing a lookup-table that looks up tenant configuration based on a unique id, like hostname

#### Netflix Eureka
