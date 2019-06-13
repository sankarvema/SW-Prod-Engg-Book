[![MicroServices Implementation](./ServiceCalls.png)]

## Phase Approach

## Maturity Model

## Design Principles
- Design for Failure
- Design for Security

## Advantages of Microservices
- Loosely Coupled
- Boundary context to encapsulate a business function
- Highly scalable
- Embrace polyglot

## Challenges

### Designing Challenges
1. Breaking Microservices: adopt domain driven design guidelines
  - Monolithic Application
  - Green Field Development

- Composability - building a composition of MicroServices to realize end to end business functionality or workflow is a big challenges
  - Deep of the composition, too deep can lead to
    - latency issues as the last MicroServices latency to be considered in the overall latency
    - dependency and virtual coupling
    - traceability to include add features
  - Feature Enhancement - dependency graph of MicroServices composition leads to virtual coupling among the services which leads to barriers in bringing new features or feature enhancement as adding a new function, contract or scheme enhanement can break the functional chain.
    - Ofcourse, this can be managed through versioning. But after a certain time the version strategy may get complex and fail
    - However, this is not isolated to microservice. Even library designing faces the same issue. However with MicroServices this can get tricky as microservice boundaries can lead to functional, department or team boundaries.


- Flow Design & analysis - Application functionality is Implemented by orchestrating a services of Microservices which may make it difficult to have functional traceability and chain of communication. This can lead to domino effect when on microservice fails.

3. Micro Database (polyglot) - Modularizing a huge relational database into micro database is a challenge. Go in phases
  - Implement service layer over Monolithic db. Build database which can build additional layer of abstraction.
  - Extract data entities - lift and shift
  - Complete microservice database model

4. Micro UI (polyglot)

5. Service Discovery




### Implementation Challenges

### Operation Challenges

1. Monitoring -  Need a better monitoring infrastructure and quick means of building potential breakdowns of a chain.

2. Fault Tolerance
  - Failure mode analysis - Risk analysis on potential failure points and having a proper plan of action. Have failure drills
  - Predictive analysis
  - Chaos Management (Chaos Monkey)

References:

- https://www.kennybastani.com/2015/07/spring-cloud-docker-microservices.html?m=1 Simple MicroServices implementation with Spring Cloud
