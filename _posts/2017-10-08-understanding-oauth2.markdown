---
layout: post
comments: true
title: Understanding OAuth2 
date: 2017-10-07 13:32:20 +0300
description: OAuth2 is an open standard for token-based authentication and authorization on the Internet # Add post description (optional)
img: Google-OAuth.png # Add image post (optional)
tags: [OAuth, OAuth2, Security]
---


## Introduction
If you’re a software developer on the web today, chances are you’ve heard of OAuth.
But what is it, how does it work, and why do we need it?


## What is OAuth 2.0?
*OAuth 2.0 is a delegation protocol, a means of letting someone who controls a resource allow a software application to access that resource on their behalf without impersonating them. It is used to protect a large (and growing) number of web APIs all over the world, from large-scale providers such as Facebook and Google to small startups.*[^1]

[^1]: OAuth2 in Action By RICHER and SANSO Manning Publications p3

Still unclear, think of this example.

**A mp3 player on the cloud, e.g soundcloud (client) wants to access your (the resource owner) mp3 files (protected resources) on Google Drive ( Google is the authorization server – see below)**

You don’t want to give the app access to (client) all your files on Google Drive, but only a limited access to mp3 files to enjoy your library. That’s where OAuth2 comes very handy.

It gives a limited access to an HTTP service on behalf of the resource owner to a third-party application without the need of the client to understand all the hassle of the protocol or the implemented security mechanism.
Have you ever seen  a web page or android app like the one in figure1, then you have used OAuth without even knowing about it!

![Alt](oauth2.PNG "Title")

