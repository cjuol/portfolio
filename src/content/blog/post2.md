---
title: "Hexagonal Architecture"
description: "Hexagonal architecture, also known as ports and adapters, was created by Alistair Cockburn."
pubDate: "FEB 05 2024"
heroImage: "/post_img.webp"
---

Hexagonal architecture, also known as ports and adapters, was created by Alistair Cockburn. This architecture aims to create a system decoupled from the framework, database, web server, etc. The idea is that changes in peripheral technologies should not affect the business logic.

## Basic Concepts

Hexagonal architecture is based on two main concepts:

1. **Ports:** These are the interfaces through which our application interacts with the outside world. There are two types of ports:

   - Driving ports (or primary): They represent the inputs to our application. For example, a REST API, a command-line interface, etc.

   - Driven ports (or secondary): They represent the outputs of our application. For example, a database, a web service, etc.

2. **Adapters:** These are the concrete implementations of our ports. There are two types of adapters:

   - Driving adapters: They use the driving ports. They implement the necessary logic to translate user input into something our application can understand.

   - Driven adapters: They use the driven ports. They implement the necessary logic to translate the outputs of our application into something the outside world can understand.

## Benefits of Hexagonal Architecture

- **Decoupling of infrastructure:** Business logic does not depend on infrastructure. This means that infrastructure can be changed without needing to modify the business logic.

- **Testability:** Since the infrastructure is decoupled, it is possible to test the business logic without needing a database, a web server, etc. You can use "mocks" for these components.

- **Multiple interfaces:** By decoupling business logic from the user interface, you can have multiple interfaces for the same application. For example, a REST API and a command-line interface.

## Example of Application with Hexagonal Architecture

Let's imagine a to-do list application. We would have something like this:

1. **Driving ports:** A REST API that allows users to create, read, update, and delete tasks.

2. **Driving adapters:** The logic that takes user input from the REST API and translates it into something the business logic can understand.

3. **Business logic:** The code that handles the logic of tasks. This logic knows nothing about REST APIs, databases, etc.

4. **Driven ports:** Interfaces representing the operations our business logic needs to interact with the outside world. In this case, we could have a port representing the ability to persist tasks.

5. **Driven adapters:** The implementation of the driven ports. In this case, we could have an adapter implementing the persistence port using MongoDB.

I hope this explanation helps you understand Hexagonal Architecture. Remember, the goal of this architecture is to create an application that is decoupled from infrastructure and can easily adapt to changes. In Hexagonal Architecture, business logic is the core of the application, and everything else is details.

## Additional Considerations

It is important to note that while Hexagonal Architecture brings considerable benefits, it can also add a layer of complexity to your code. Introducing ports and adapters can generate more code and abstractions to manage. Therefore, it is crucial to consider whether the benefits of this architecture outweigh the additional cost of complexity before adopting it.

Additionally, Hexagonal Architecture is just one of several architectures you can use to design your application. Other popular options include Layered Architecture, Onion Architecture, and Clean Architecture. Each of these architectures has its own benefits and drawbacks, and the choice between them will depend on the specific needs of your project.

## Conclusion

In summary, Hexagonal Architecture is a software design strategy that puts business logic at the center of the application and allows infrastructure details to be easily interchangeable. It is especially useful in projects where changes in infrastructure are anticipated, or where a high degree of testability is needed. However, it can also add a layer of complexity to your code, so it should be adopted with consideration.
