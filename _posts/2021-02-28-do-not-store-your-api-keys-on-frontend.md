---
layout: post
title: Do NOT Store your API Keys on Frontend
description: Multiple times I'm asked what is the best way to store and access Secret Keys - such as API keys - on a React application.  There's a couple of things you can do to \"hide\" your keys and actually make them harder to access
summary: Multiple times I'm asked what is the best way to store and access Secret Keys - such as API keys - on a React application.  There's a couple of things you can do to \"hide\" your keys and actually make them harder to access
tags: security
minute: 2
---

Multiple times I'm asked what is the **best way to store and access** **Secret Keys** - such as API keys - on frontend (React, Vue, etc...)

There's a couple of things you can do to "hide" your keys and actually make them harder to access. What most people will say when asked this question is to use **Environment Variables**. They are not wrong but, in my opinion, also not entirely right.

Create a `.env` file, put sensitive information there and access those variables from your code. That file should always be kept away from source control, like Github, so that's already one advantage against using variables directly on the code. But there's a **couple of problems** related to this method.

> You should never store your API Keys on Frontend.
>
>
> ![Never](https://media.giphy.com/media/Y4Jb8jkcqRtnznTnpC/giphy.gif)

First, when you build the project in order to use it in production, those variables will stay somewhere on the bundled code, which means that anyone with access to that code will be able to dig through it and possibly find what your secret key is.

Secondly, if these are API keys, those keys will always be visible on any request, either GET or POST, because request data is visible directly through the browser. Every time a request is made on the frontend, someone could just open browser's network tab and easily visualize the API key.

## The solution

The truth is that none of these previously described methods will completely hide your secrets from unwanted eyes. What I usually do is send a request to my own Backend API, which will then request the third-party API, process the received data and send it back to the client.

![](/assets/images/store-secret-api-keys.png)

This way we can keep our secret variables actually secret. Using this method, it is still recommended the use of Environment Variables, in order to keep keys away from source control.

If you have any questions and suggestions regarding this post, or just want to follow me for more of these, I'm on [Twitter](https://twitter.com/pmatarodrigues), [Github](https://github.com/pmatarodrigues) and [Linkedin](https://linkedin.com/in/pmatarodrigues).
