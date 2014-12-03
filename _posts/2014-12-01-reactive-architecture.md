---
layout: post
comments: true
title: Reactive Microservice Architecture in Node
tags: javascript nodejs reactive architecture
---

![](/public/react.jpg)

This is the start of what I expect to be several posts on the subject of applying Node in a reactive microservice architecture. I have found that by building single purpose node modules as microservices that live on a scalable message queue, I am able to piece together interesting applications simply as a result of how I deploy and configure these services. In this series of articles I will provide code and deployment examples that show this architecture in action.

<!--more-->

## Inspiration

For years I have been working at SAAS companies as a software architect building applications that integrate many other SAAS services and internal platforms. Over this time, my team and I have run into many challenges knitting these things together in a way that makes a system:

* Reliable - In the face of outages / slow responses from external services
* Responsive - Provide a user experience that minimizes wait time
* Scalable - Available to thousands of customers on a common infrastructure

I have recently been inspired by a combination of articles that have led to my initial thoughts on this architecture. Some of these articles include:

* [The reactive manifesto](http://www.reactivemanifesto.org/)
* [Messaging as a programming model](http://eventuallyconsistent.net/2013/08/12/messaging-as-a-programming-model-part-1/)
* [Microservices](http://martinfowler.com/articles/microservices.html)

I have also been a long time Java and Javascript developer and over the last couple of years I have fallen in love with the power and simplicity of building modules in Javascript on Node. As I have worked with Node, I have realized that the small footprint of Node is a fantastic use for an architecture that consists of tens of hundreds of microservices deployed as an application.

## Microservices

Microservices are very small services running in their own process built around business capabilities and independently deployable by fully automated deployment systems. There are a few significant properties of Microservices that apply to this architecture:

* Componentized - Microservices should be very small with a single responsibility and be out of process. This is very different from a typical library where components are assembled in process.

* Message Driven - Microservices should be driven by asynchronous messaging where the intelligence is left up to the microservice implementation and not provided by the messaging fabric

* Decentralized Data - Each service should manage its own database, either different instances of the same database technology, or entirely different database systems. You can think of this model as the OO concept of data encapsulation. No service can access the database of another service.

## Message Queue

When combining a fast and reliable message queue with the microservices architecture, the individual components of the entire solution can be decoupled. The Reactive Microservices architecture relies on asynchronous message-passing to establish a boundary between services that ensures loose coupling, isolation, and location transparency.

The message queue should provide messaging over a lightweight message bus. The infrastructure chosen is typically dumb (i.e., it acts as a message router only) - simple implementations such as RabbitMQ or ZeroMQ don't do much more than provide a reliable asynchronous fabric - the smarts still live in the end points that are producing and consuming messages; in the services.

## Conclusion

By building these single purpose microservices that simply respond to messages on a message queue, the application can be extremely decoupled and the individual modules can be built without any concern for the expected architecture. This allows application architects to work with DevOps engineers to provide a new solution by simply deploying and configuring a set of services. It provides a LEGO-style application assembly similar to the way that UI engineering often uses components to construct a user interface.

This will change the role DevOps plays in the application architecture. Historically DevOps have been focused on how to deploy load balancers, web servers, application containers and databases in a way that allows the application to scale reliably. Now DevOps can take these pre-constructed microservices and deploy them in many different ways to provide many different application solutions. This allows the actual solution engineering to occur at deployment time instead of at development time.

## Next Steps

Now that we have a foundation established, in my next article I will provide some microservice code examples followed by some deployment examples that will bring this all together in some basic applications.
