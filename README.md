
# fanbot.me Development Process & Technical Design

## Development Process 

This document provides guidance and template material intended to help technical staff team, it is also useful background reading for anyone involved on the development process of our current product, this document will assume you know a thing or two about Lean and/or SCRUM, The less lengthy your sprints are, the faster you can course correct.

*"Sprints are like flights; shorter = better."*

Stay lean, build less, you should keep your development process as lean as possible meaning, The more you and your people know, the more you can do in a smaller number of people for smaller amount of money.

Development Process Principles

1. Agile Development

    1. Features

    2. Stories

    3. Task

2. Code Peer Review

    4. Early debugging

    5. The code stays here

    6. Developers learn from each others

    7. Teamwork

3. Time Tracking

4. Stage Environment

    8. Development 

    9. Staging 

    10. Production

5. Straight-line Communication

6. Weekly Reports

7. Progress Tracking

8. Maintenance & Support

## Development tools and process

### Source Control

Our source control tool for our development process will be [Github](https://github.com/) so we assume you know git, we will use release automation, and we will set up environments so we can regularly release updates, the benefits of a release process is that it forces us to think in terms of "shipping" this will help us to start planning to releasing stables versions of our application every one or two sprints depending on our development process. So the main goal is release the update of our product  with a single command.

Four our branching model will be using GitFlow is suited to collaboration and scaling the development team, for more information visit this link. [Git Flow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)

### Automated Testing

Mostly of our code will be writing in javascript for automation testing in javascript will be using [Phantom.js](http://phantomjs.org/) this framework is mostly used for front-end testing is easy to run  from a command line so it integrates nicely in our CI system, for our server-side code will be using 

[Mocha.js](http://mochajs.org/) 

Bug and issue Tracking

For bug and issue tracking will be using a trello board with the following structure:

1. Reported by team

2. Reported by clients

3. Accepted

4. In Progress

5. To be validated

6. Done

### Continuous Integration

Unit tests only help if you’re running them. we have  a [Drone.io](https://github.com/drone) server to watch and test our code, Drone is a lightweight, powerful continuous delivery system built on container technology, drone uses a simple yaml configuration file, a superset of docker -compose to defines and execute pipelines inside Docker containers.

### Code Reviews and code Quality

We want to make sure that our team members reviews each other’s code this has several significant benefits. First and foremost, it ensures that you’re shipping higher quality code. Second, it serves as an amazing educational opportunity for team members, so for this will be using our source control version Github using the feature of pull request to make code reviews in our development team once every member of the team review the pull request this can be merged on the requested branch

### Release Management and Environments 

Release management include our CI environment and our scripts for releasing new code, so we have multiples environments for that staging and production, a staging environment serves two major purposes. First, it creates a shared environment where our members can test their code against consistent representation of your application; this give us a predictable a reliable version of your application that helps to decrease the "works for me" problem, Second, it creates a production-like environment for testing and features that may work slightly differently in a production or staging setting than they would on local development environment — this helps us detect any issues that might not otherwise be visible until you’ve released your code into production.

Complete Process.

## Our Development Stack

We will separate our development stack in 4 categories.

1. Application and Data

2. Utilities

3. DevOps

4. Business Tools

Application and Data

1. Languages

* Javascript

* Php

* Go

* Python

Frameworks

* React 

* Node.js

* Mocha

* PhantomJS

* Cloud Hosting & Storage 

* AWS

* Digital Ocean

Databases

* MySQL

* PostgreSQL

* Mongodb

* Redis (In-Memory Database)

Utilities

* Paypal

* Stripe

* Messenger Platform

* Api.ai

* Google Analytics

DevOps

* Github & git

* Docker

* Webpack

* Drone.io

* Sentry

Business Tools

* G Suite

* Slack

* Trello

* Zendesk

* Intercom

* InVision

* Zoho CRM

Javascript Style Guide 

* [https://github.com/fanbotme/javascript](https://github.com/fanbotme/javascript)

# ChatBots

Chatbots are on the rise. Startups are building chatbots like us in fanbot we’ve been working on chatbots for a while, and we’ve been looking on what is going on in the industry.

* Tools

1. [flowxo](https://flowxo.com/)

2. [Messenger](https://messenger.fb.com/)

3. [Api.ai](https://api.ai/docs/integrations/facebook)

4. [Init](https://www.init.ai/)

* Books	

1. [Bot Business 101: How to start, run & grow your Bot / AI ](https://www.amazon.com/gp/product/B01NBU30DA/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&tag=botsfloor0d-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=B01NBU30DA&linkId=aa42854489ad31d9a907b97ac4eb77f5)

2. [Designing Bots: Creating Conversational Experiences](https://www.amazon.com/gp/product/1491974826/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&tag=botsfloor0d-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=1491974826&linkId=1d6760d3ae2be41e363ff48a796ebc68)

3. [Conversational Interfaces: Principles of Successful Bots, Chatbots, Messaging Apps, and Voice Experiences ](https://www.amazon.com/gp/product/0998289000/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&tag=botsfloor0d-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=0998289000&linkId=dfb125ac89c4e991d1f8e5e5ff587f7d)

4. [Business of Bots: How To Grow Your Company Through Conversation](https://www.amazon.com/gp/product/0998289019/ref=as_li_qf_sp_asin_il_tl?ie=UTF8&tag=botsfloor0d-20&camp=1789&creative=9325&linkCode=as2&creativeASIN=0998289019&linkId=c932cfee54ea743388ee5ef7992222b7)

*  Blogs:

1. [ChatBot Architecture](https://medium.com/@surmenok/chatbot-architecture-496f5bf820ed)

2. [Natural Language Pipeline for Chatbots](https://medium.com/@surmenok/natural-language-pipeline-for-chatbots-897bda41482)

3. [Character-Level Convolutional Networks](https://medium.com/@surmenok/character-level-convolutional-networks-for-text-classification-d582c0c36ace)

4. [Deep Learning for Chatbots](http://www.wildml.com/2016/04/deep-learning-for-chatbots-part-1-introduction/)

5. [Architecture Of Probot](http://highscalability.com/blog/2017/3/15/architecture-of-probot-my-slack-and-messenger-bot-for-answer.html)

6. [Chatbots work guide architecture](https://www.marutitech.com/chatbots-work-guide-chatbot-architecture/)

7. [Conversational UX Design. All Facebook Messenger Bots Interactions](https://chatbotsmagazine.com/cheat-sheet-all-facebook-chatbot-interactions-4b14e4e00178)

References.

Development Process

* [Development Tools & Process](https://medium.com/starting-sustaining/chapter-10-development-tools-processes-c4bb7706883e)


