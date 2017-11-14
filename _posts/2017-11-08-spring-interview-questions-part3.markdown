---
layout: post
comments: true
title: Spring Security
date: 2017-10-07 13:32:20 +0300
words: 0
description: In the last post, we talked about Spring WEB MVC. # Add post description (optional)
img: security.png # Add image post (optional)
tags: [spring, interview, security]
---


## Introduction
In the last post, we talked about Spring Web MVC.
This time, we are gonna talk about Spring Security. I'll divide this article into three parts: Generalities, Practical and Architectural. Let's dive in!

## Generalities

### What's Spring Security?

**Spring Security** is a powerful and highly customizable *authentication* and *authorization* framework. It is the de-facto standard for securing Spring-based applications.[^1]

* **Authentication** is the process of establishing a principal is who they claim to be (a "principal" generally means a user, device or some other system which can perform an action in your application)
* **Authorization** refers to the process of deciding whether a principal is allowed to perform an action within your application

### What's CSRF?

**Cross-site request forgery** is an attack that forces an end user to execute unwanted actions on a web application in which they're currently authenticated wihtout knowing about it!

To illustrate this even more, let's follow this scenario where Ilias is transferring 5$ to Youcef using a Banking application. The attacker in this case will be Jamal. We will imagine that we are using a form that has two fields, *amount*, *receiver* and a submit button.
The `POST` request will look like this:
```
POST http://bank.com/transfer

receiver=Youcef&amount=5
```

What Jamal could do in this case is to create a form with hidden fields:

```html
<form action="http://bank.com/transfer" method="POST">
<input type="hidden" name="receiver" value="Jamal"/>
<input type="hidden" name="amount" value="500"/>
<input type="submit" value="View sexy pictures"/>
</form>
```

Jamal has high skills in Social Enginnering. He will simply use that at his own advantage to send to Ilias an email with embedded html code that contains this form to trick him to click on the submit button when he's logged into the application.

Alternatively, he could use JavaScript:

```javascript
<body onload="document.forms[0].submit()">
```

and Voilà! Jamal receives 500$ from Ilias!

[^1]: https://projects.spring.io/spring-security/

