# MicroService using NodeJS

### MicroService
* **What is MicroService**
[Microservice](https://www.google.com/search?rlz=1C1GCEA_enNG816NG816&sxsrf=ALeKk03Dy5BwuoKLQbR-DqtHxfwBo9d2XA:1606820376732&q=What+is+Microservices+in+node+JS%3F&sa=X&ved=2ahUKEwiMjZeu0KztAhWTilwKHbHnCkcQzmd6BAgKEAk)One of the many variants of distributed systems is the microservices architecture, which structures an application as a collection of loosely coupled services. ... Services are fine-grained and the communication protocols are lightweight *like the HTTP protocol*

### Node JS
* **What is NodeJS**
[Node Js](https://www.toptal.com/nodejs/why-the-hell-would-i-use-node-js)Node. js is primarily used for non-blocking, event-driven servers, due to its single-threaded nature. It's used for traditional web sites and back-end API services, but was designed with real-time, push-based architectures in mind.

### Routes


**Posts. POST:4000**

URI | Description | Method 
------------ | ------------- | -------------
/posts | Returns all posts | GET
/post | Creates post | POST
/events | Sends event to the event-bus | POST

**Comments. PORT:4001**

URI | Description | Method 
------------ | ------------- | -------------
/posts/:id/comments | Returns all comment for a specific post | GET
/posts/:id/comments | Creates comment | POST

**Query. PORT:4002**

URI | Description | Method 
------------ | ------------- | -------------
/posts | Returns all posts with comments | GET
/events | Sends event to the event-bus | POST

**Moderation. POST:4003**

URI | Description | Method 
------------ | ------------- | -------------
/events | Handles CommentCreated event | POST

**Event Bus. PORT:4005**

URI | Description | Method 
------------ | ------------- | -------------
/events | Returns events | GET
/events | Handles all events | POST