+++
authors = ["PedroMataRodrigues"]
date = 2021-02-15T00:00:00Z
excerpt = "I decided to embrace in a new side project, something that could be large enough to cover all the areas needed in software development.  A short - and lonely - brainstorm led to an idea that can be expanded almost infinitely. I decided to build a Financial Portfolio Manager."
hero = "/images/airfinance_blog_1.png"
timeToRead = 3
title = "Building a Financial Portfolio Tracker - Introduction and Architecture"

+++
_Hello There!_

The number of frameworks and programming languages is increasing and, as I needed to solidify and diversify my knowledge in order to understand what would catch my attention,

I decided to embrace in a new side project, something that could be large enough to cover all the areas needed in software development.A short - and lonely - brainstorm led to an idea that can be expanded almost infinitely. I decided to build a Financial Portfolio Tracker.

A platform like this could scale to a high number of requirements if I wanted to continue with it, but at the same time it was perfect for a small and steady start.

> This post is written in the present, as I'm writing as things are advancing, and every new post will be related to each achieved checkpoint.

***

## Project Architecture

Starting this project with the mindset of creating something that could be used to improve my knowledge means that every step should be taken having in mind a correct software development process. So... No skipping steps.

With this in mind, I'm starting with a basic diagram of the technological stack I'm using. This can be changed in the future if I realize that some things can be improved. This is a learning process after all.

![](/images/architecture.png "architecture")

## Database Architecture

![](/images/db_diagram.png)

I sketched an initial and pretty basic database diagram to serve as base for this project, it's main components being User (user data and login information), Account (bank, exchange account, under the mattress or some place where the user keeps its money), Holding (what that account holds. for example EUR, USD, Stocks, Crypto, etc..) and Checkpoints. This last table will be mainly used to build evolution diagrams with the main goal of learning about Big Data in the future.

***

## Frontend

For frontend, [React](https://reactjs.org/) with [Typescript](https://www.typescriptlang.org/) were the chosen ones. Because I have some experience in developing React projects and wanted all the benefits that Typescript provides, mainly related to static typing (in contrary to Javascript that uses dynamic typing), which leads to faster detection of bugs before runtime and better readability.

Frontend code was generated using [Create React App](https://reactjs.org/docs/create-a-new-react-app.html), which is stated as a "_comfortable environment for learning React_**",** this means that it's not the best for large scale usage but it's enough for the type of project that I'm trying to build. Create React App is powered by babel and webpack, so choosing this tool actually removes some of their complexity but also means that I skipped some useful learning. (I'll probably do it in the next couple of projects ^^)

CSS is left to [TailwindCSS](https://tailwindcss.com/). I absolutely fell in love with it the first time I used it. The time it saves and the simplicity necessary for building some component are some major advantages in comparison to regular css and even scss. The only downside I found is the amount of code that stays on the html side, which is one thing I'm currently studying in order to better understand how it can be overcome.

This is the first look of how it looks. I'm still trying to play a bit with positioning and colours but it's not bad for a first sketch. (Do not make fun of my income, I'm slowly working it out `:sweat_smile:` )

![](/images/first_screenshot-1.png)

## Next Step

This first step was mainly focused on exposing the project and introducing what my main goals are and what will be necessary for this to be built. In the next post, I'll write about the backend part and how the connection between the two will be made.

Find out on the next ~~episode~~ **_Building a Financial Portfolio Tracker_** part ^^

Thank you for reading.

#### Continuing...

***

If you have any questions regarding this post (or just want to follow me), I'm on [Twitter](https://twitter.com/pmatarodrigues), [Github](https://github.com/pmatarodrigues) and [Linkedin](https://linkedin.com/in/pmatarodrigues).