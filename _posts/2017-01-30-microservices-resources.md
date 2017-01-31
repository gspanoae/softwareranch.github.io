---
layout: post
title: Microservices resources
date: '2017-01-30 22:00:00 +0000'
categories: resources Microservices
author: gabi
published: true
---

**work-in-progress**

# What is Microservices architecture?

> In short, the microservice architectural style is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API. These services are built around business capabilities and independently deployable by fully automated deployment machinery. There is a bare minimum of centralized management of these services, which may be written in different programming languages and use different data storage technologies.
**[From James Lewis and Martin Fowler](https://martinfowler.com/articles/microservices.html){:target="_blank"}**

#### **Articles**
* [Open Group White Paper](https://www2.opengroup.org/ogsys/catalog/W169){:target="_blank"}
* [Microservices by Martin Fowler](https://martinfowler.com/articles/microservices.html){:target="_blank"}
* [Microservice Architecture Pattern by Chris Richardson](http://microservices.io/patterns/microservices.html){:target="_blank"}

#### **Videos**
* [YOW! Nights March 2016 with Martin Fowler](https://www.youtube.com/watch?v=Irlw-LGIJO4){:target="_blank"}

# Which are the design principles?
Each architectural style is nothing else than a set key principles which will shape the landscape of your technical solution, and Microservices architecture is no exceltion:
-**Cohesion and Autonomy**
-**Business domain centric**
-**Resilience**
-**Centralized logging and monitoring**
-**Automation tools**

The next sections will provide more details and resources around these key aspects. 

## Cohesion and Autonomy(loosely coupled, ownership and versioning)
In other words each Micro-Service will need to do a well define job, support a core purpose in an autonomous way, basically will validate the Single Responsibility Principle: 
> A class should have only one reason to change
Robert C. Martin

#### **Articles**
* [](https://en.wikipedia.org/wiki/Single_responsibility_principle){:target="_blank"}

## Business domain centric
Design your microservice in line with relevant business use cases and keep clear boundaries in your solution. Take action and fix any overlaps, split further or join two if that is necessary. 

#### **Articles**
* [Domain Driven Design for Services Architecture](https://www.thoughtworks.com/insights/blog/domain-driven-design-services-architecture){:target="_blank"}

## Resilience

## Centralized logging and monitoring

## Automation tools

# Which are the different deployment options?

## Synchronous or asynchronous communications

## API Gateway, scaling and caching

## Centralized Logging and Monitoring

## Virtualization, Containers and Self Hosting

## Automation CI and CD Tools

# What technologies can help achieving?

# Microservice Governance

# Greenfield and Transition strategies
