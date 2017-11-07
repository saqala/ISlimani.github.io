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
So you are about to pass an interview as Full stack spring developer, Backend spring developer and yo are wondering what are
the questions that might be asked about spring during the interview. So, you are in the right place.
Interested. Let's dive in!


## The Spring Eco-system
As a general rule, Spring is too big to cover, that's why, I believe that you didn't include in your resume that you master Spring EcoSystem without specifying what frameworks and modules you mean. If you do so, you are screwed! and don't blame anyone for not picking up you, though that is another topic. That's why we will try to cover the most used frameworks and modules.

Speaking about a modern java-based enterprise application, you will mostly need:

* Spring Core: Ioc (Inversion of Control) container and Spring AOP (Aspect oriented programming)
* Spring WEB: Spring MVC, RestFul Web Services and Spring WebSocket (it depends)
* Spring Test: with JUnit and Mockito
* Spring Boot: less configuration, more focus on business logic
* Spring Security: Who doesn't need that! a Powerful framework to manage authentication and access-control 
* Spring Data JPA: an easy way to implement JPA based repositories
* Spring Social: Connect your application with known social providers, Google, Facebook and Twitter and Others.
 ** Spring MVC (including Restful web services), Spring Security, Spring Core (including Inversion of Control IOC), Spring Data, Spring Boot **
to some extent, ** Spring Social, Spring Test**

Still unclear, think of this example.

**A mp3 player on the cloud, e.g soundcloud (client) wants to access your (the resource owner) mp3 files (protected resources) on Google Drive ( Google is the authorization server – see below)**

You don’t want to give the app access to (client) all your files on Google Drive, but only a limited access to mp3 files to enjoy your library. That’s where OAuth2 comes very handy.

It gives a limited access to an HTTP service on behalf of the resource owner to a third-party application without the need of the client to understand all the hassle of the protocol or the implemented security mechanism.
Have you ever seen  a web page or android app like the one in figure1, then you have used OAuth without even knowing about it!

![Figure 1 A Web App asking for authorization]({{site.baseurl}}/assets/img/oauth2.jpg)

## Components in OAuth 2.0
We have just mentioned all the components of OAuth 2.0 in our example. You see, it’s just that simple.
These are the components that we have so far:

* *The resource owner has access to an API and can delegate access to that API. The resource owner is usually a person and is generally assumed to have access to a web browser.[^2]  (The user with the Google Account in the last example)*

* *The protected resource is the component that the resource owner has access to. This can take many different forms, but for the most part it’s a web API of some kind.[^3]  (mp3 files)*

* *The client is the piece of software that accesses the protected resource on behalf of the resource owner.[^4]  (web app, e.g soundcloud)*

* *The authorization server (AS) is trusted by the protected resource to issue special purpose
security credentials—called OAuth access tokens—to clients.[^5]  (Google).*

[^2]: OAuth2 in Action By RICHER and SANSO Manning Publications p5
[^3]: OAuth2 in Action By RICHER and SANSO Manning Publications p6
[^4]: OAuth2 in Action By RICHER and SANSO Manning Publications p6
[^5]: OAuth2 in Action By RICHER and SANSO Manning Publications p11

## So How does OAuth 2 work?

* Simply put, the client first sends the resource owner to the authorization server in order to authorize the client.

* The resource owner authenticates to the authorization server and is generally presented with a choice of whether to authorize the client making the request (figure1).

* Once the authorization grant has been made, the client can then request an access token from the authorization server.

* This access token can be used at the protected resource to access the API, as granted by the resource owner.

## What now?

In the next part, we will be looking into real examples using Spring Framework.

Stay Tuned!




