---
layout: post
comments: true
title: Spring Interview Questions
date: 2017-10-07 13:32:20 +0300
description: So you are about to pass an interview as Full stack developer, Backend spring developer and yo are wondering what are # Add post description (optional)
img: spring.png # Add image post (optional)
tags: [spring, interview]
---


## Introduction
So you are about to pass an interview as Full stack spring developer, Backend spring developer and you are wondering what are
the questions that might be asked about spring during the interview. So, you are in the right place.
Interested. Let's dive in!


## The Spring Ecosystem
As a rule of thumb, Spring is too big to cover, that's why, I believe that you didn't include in your resume that you master Spring EcoSystem without specifying what frameworks and modules you mean. If you do so, you are screwed! and don't blame anyone for not picking up you, though that is another topic. That's why we will try to cover the most used frameworks and modules.

Speaking about a modern java-based enterprise application, you will mostly need:

* Spring Core: Ioc (Inversion of Control) container and Spring AOP (Aspect oriented programming)
* Spring WEB: Spring MVC, RestFul Web Services and Spring WebSocket (it depends)
* Spring Test: with JUnit and Mockito
* Spring Boot: less configuration, more focus on business logic
* Spring Security: Who doesn't need that! a Powerful framework to manage authentication and access-control 
* Spring Data JPA: an easy way to implement JPA based repositories
* Spring Social: Connect your application with known social providers, Google, Facebook and Twitter and Others.

## First things first: Basics

### What's JEE:

JEE or Java Enterprise Edition is a **collection of specifications, APIs and technologies** maintained by JCP(Java Community Process) **designed to support Enterprise Applications which usually are large-scale, distributed, difficult to maintain and mission-critical**.

The so-called application servers, like WildFly (formely known as JBoss), GlassFish, etc. are implementations of these specifications.

### What's Spring?
Spring means different things in different contexts. In the old days, people refer to Spring as a framework to handle Dependency Injection. Over time, Spring has been much more improved to become **an Ecosystem that provides everything you need to embrace the java in an enterprise environment**. Nowadays, Spring refer to the whole family of Spring Projects and modules. 
*You should know that Spring maintain and develop it's framework around what's called Projects. Inside any Project, you will find different sub-projects maintained either by the community or the Spring developers. Every Project depends on different modules. refer to this [article][1] for a more thorough explanation about they relate to each other.*

[1]: http://springtutorials.com/introduction-to-spring-modules/ "introduction to spring modules"

Let's have a look inside [spring social project][2], the project contains different sub-projects:

* Spring Social Facebook
* Spring Social Twitter
* Spring Social Linkden

as well as different community projects, they are by tens:

* Spring Social DropBox
* Spring Social Google

[2]: https://projects.spring.io/spring-social/ "spring social"
### Spring and JEE:
Now you might wonder, how does JEE relate to Spring? in both definitions, I didn't mention one another!

That's quite true! because Spring isn't an application server nor an implementation of JEE.
In fact, JEE and Spring are competing for enterprise java. Spring doesn't necessary require JEE to run.
As an example, Tomcat, which is an implementation of Servlet and JSP and also provide support for different view technologies including and not limited to Thymeleaf, is more than sufficent to run All the whole Spring Ecosystem.

* Dependency Injection: Spring IOC, CDN
* AOP: Spring AOP, interceptor
* Presentation Framework: Spring MVC, JSF
* Security: Spring Security, JAAS/JASPIC
* Testing: Spring Testing, Arquilian
* Spring Beans vs EJB








