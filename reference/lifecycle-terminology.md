Software Lifecycle Terminology
==============================

We work on software that's anywhere in its lifecycle - from something that we've created just to see if it's possible, through to widely-used and well-maintained software that's used in production. 

In order to be clear about what people should expect from a piece of software, we use specific terminology. This page documents our interpretation of these terms, and is intended to be referred to by developers at ODSC, developers that we're collaborating with, and clients. 

Any particular piece of software might have elements that are at different stages of development. For example, a new feature in a mature software product might be a prototype, while the main software product is production-ready. 

As a rule of thumb, it's approximately an order of magnitude of extra work, complexity or cost to move up each level; that is to say that a production implementation of a feature is 100x more complex than its prototype. 

## Prototype

A prototype has been created to see if something is technically feasible, or to demonstrate what something could look like. 

It will:
* Be quick to make
* Serve a single purpose - for example to try out an interface idea, or to test an algorithm
* Provide some learning for a future implementation of a feature. 


It won't:
* Deal with any cases that it wasn't explicitly designed for
* Provide any help when a user tries to do something that it wasn't designed for
* Have any documentation to help a user without supervision


A prototype is appropriate when we're not sure if something's possible, or we want to show what something could look like. 

Example: A prototype of a web preview for some data will only work if the data is correctly formatted, and the field contents are broadly as expected. A user shown this preview with some data that's as expected can tell us whether they find the presentation helpful. A user who provides data with (for example) an excessively long Title field, or a poorly-formatted Address field, may see a broken webpage. 

## MVP

A Minimum Viable Product is a complete, working application that implements the minimum set of features that provide some value to users. 

It will:
* Do what it's designed to, for the most common cases, well enough to be useful
* Be tested
* Have a clear purpose that it has been designed to achieve; usually this is to help a user with a specific task
* Provide clear feedback if a user tries to do something it wasn't designed for
* Provide learning, and potentially code, for a future production implementation 
* Have sufficient documentation to help a user who has a good level of relevant skills to carry out their task

It won't:
* Have been designed to scale, be easily altered, or be optimized for performance outside of limited criteria

An MVP is appropriate when we want to provide limited value quickly; such as in order to demonstrate the potential for future investment or to make a specific task easier. 

Example: An MVP of a data preview tool will check that the data is of a size range that it can handle, and will check that the data is correctly formatted before trying to display it. Any unusual entries in the data will be rendered; they might make the webpage look a little odd, but not broken. 

## Production

Production software is ready to use for a wide range of workloads; it can be used for real-life applications and (supported by appropriate maintenance) can be used indefinitely. 

It will:
* Do what it's designed to do, well enough to handle almost any case that can be conceived of
* Detect conditions that it can't handle, and provide helpful feedback
* Be extensively tested
* (if appropriate) Combine multiple functions to help a user achieve an outcome that may span multiple tasks with minimal friction
* Be documented for a range of users

