---
layout: post
comments: true
title: What you should to pass a Spring Interview
date: 2017-10-07 13:32:20 +0300
description: So you are about to pass an interview as a Backend Spring developer and you are wondering what are # Add post description (optional)
img: spring.png # Add image post (optional)
tags: [spring, interview]
---


## Introduction
So you are about to pass an interview as Backend Spring developer and you are wondering what are
the things that I should know about. Then you are in the right place. This will be a good start for you.
This will be a work in-progress, in which I will try to add as many questions and answers as possible.
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
As an example, Tomcat, which is an implementation of Servlet and JSP and also provide support for different view technologies including and not limited to Thymeleaf, is more than sufficent to run All Spring Ecosystem.

* Dependency Injection: Spring IOC vs CDN
* AOP: Spring AOP vs interceptor
* Presentation Framework: Spring MVC vs JSF
* Security: Spring Security vs JAAS/JASPIC
* Testing: Spring Testing vs Arquilian
* Spring Beans vs EJB

### What's Dependency of Injection

So far, the simplest definition that I've found for dependency injection is the following:
*Basically, instead of having your objects creating a dependency or asking a factory object to make one for them, you pass the needed dependencies in to the object externally, and you make it somebody else's problem. This "someone" is either an object further up the dependency graph, or a dependency injector (framework) that builds the dependency graph. A dependency as I'm using it here is any other object the current object needs to hold a reference to.*[^1]

[^1]: https://stackoverflow.com/questions/130794/what-is-dependency-injection/140655#140655

In Spring terms, instead of creating your objects with the *new* operator, let *The IoC Container* handle them for you. All you need to do, is to *@Autowired* your object and define the referenced object with an xml file, with annotations or with java configuration.

### What's the IoC Container

The Spring IoC container is responsible for instantiating, configuring and assembling objects known as *beans*, as well as managing their lifecycle. It is represented by the interface ApplicationContext.

### How to instantiate Spring Ioc Container?

As a general rule of thumb, use *ApplicationContext* unless otherwise you have a good reason not to do so. Why? because ApplicationContext is built on top of BeanFactory and it offers what BeanFactory provides and other more enterprise-specific functionality.

### What's a bean and what are its scopes?

Every Object created and maintained by Spring IoC is called a bean.
They are 6 predefined and supported beans:

* Singleton: (Default) Scopes a single bean definition to a single object instance per Spring IoC container.
* ProtoType: Scopes a single bean definition to any number of object instances.
* Request: Scopes a single bean definition to the lifecycle of a single HTTP request
* Session: Scopes a single bean definition to the lifecycle of an HTTP Session.
* Application: Scopes a single bean definition to the lifecycle of a ServletContext.
* WebSocket: Scopes a single bean definition to the lifecycle of a WebSocket.

### Explain the bean lifecycle:

* Instantiation: The Spring IoC will look for a bean definition inside a configuration xml file or annotation. After it will find it, it will create an instance of the bean.
* Properties injection: After creation of that instance, dependency will be injected.
* `setBeanName()`: This method of `BeanNameAware` interface will be called if a bean has implemented it. It sets the bean name.
* `setBeanClassLoader()`: This method of `BeanClassLoaderAware` interface will be called if a bean has implemented it.
* `setBeanFactory()`: This method of `BeanFactoryAware` interface will be called if a bean has implemented it. It provides the owning factory.
* `postProcessBeforeInitialization()`: This method of `BeanPostProcessor` interface will be called if a bean has implemented it
* `@PostConstruct`: The method annotated with this annotation will be called in this phase. Note that Spring recommends to use this annotation over implementing `InitializingBean` interface.
* `afterPropertiesSet()`: This method of `InitializingBean` interface will be called if a bean has implemented it.
* `init-method`: in case you have used an xml configuration, custom init method defined via this attribute will be called. (no need to define it, if you have used @PostConstruct or java based configuration `@Bean(initMethod = "")` ).
* `postProcessAfterInitialization()`: This method of `BeanPostProcessor` interface will be called if a bean has implemented it.

At this stage, the bean is fully ready to be used.

* `@PreDestroy`: The method annotated with this annotation will be called in this phase. Note that Spring recommends to use this annotation over implementing `DisposableBean` interface.
* `destroy()`: This method of `DisposableBean` interface will be called if a bean has implemented it
* `destroy-method`: in case you have used an xml configuration, custom destroy method defined via this attribute will be called. (no need to define it, if you have used @PreDestroy or java based configuration `@Bean(destroyMethod = "")` ).


