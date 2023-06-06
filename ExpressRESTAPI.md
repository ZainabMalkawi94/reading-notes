## Class - 02 - Express REST API
### Review: ES6 Classes

1. Classes are a template for creating ____.

    Classes are a template for creating objects.

2. Can a class declaration be hoisted?

    Yes, in JavaScript, class declarations are hoisted.

3. How would you describe a constructor and contextual “this” to a non-technical friend?

    A constructor acts as a blueprint that defines how objects should be created, setting up their initial properties and behaviors. The contextual "this" keyword refers to the current object being used or accessed, enabling access to its specific properties and methods. Using a constructor and "this" allows us to create and manipulate multiple objects based on the same template, each with its own distinct set of properties and behaviors. Well done!

-------------
### Using Express Routing

1. Within Express, what does routing refer to?

    In Express, routing refers to the process of defining how the server handles client requests based on specific URLs and HTTP methods.
    It involves mapping routes to corresponding functions or actions that determine the server's response to each request.
    By configuring routes in Express, you can create a structured API and define the behavior for different URL endpoints.

2. What is the difference between a route path and a route method?

    The route path in Express specifies the URL pattern to match for a request, such as "/users" or "/products/:id".

    The route method, on the other hand, indicates the HTTP method (GET, POST, PUT, DELETE, etc.) used to access that route.

    Together, the route path and method determine how Express matches incoming requests and triggers the corresponding callback function to handle the request.

3. When is it appropriate to add "next" as a parameter to a route handler and what must you do if "next" has been passed to your middleware as a parameter?

    "next" should be added as a parameter to a route handler in Express when you want to pass control to the next middleware or route handler after executing the current handler.

    If "next" has been passed to your middleware, you should call it within the middleware to pass control to the next middleware in the chain or to the next matching route handler. Failing to call "next" can result in request hanging or not being properly handled.

---

### Express Routing

1. What is an Express Router?

    An Express Router is a feature in the Express.js framework that allows you to create modular and organized route handlers. It provides a way to group related routes together and define middleware functions specific to those routes. Express Router helps in structuring and managing the routes in your application, promoting code organization, reusability, and separation of concerns.

2. By what mean do we initialize "express.Router()" in an express server?

    In an Express server, you initialize an Express Router by requiring the express module and invoking the Router() method from the express object. This creates a new instance of the router that you can use to define routes and middleware.

    Here's an example of how you would initialize an Express Router in an Express server:

            const express = require('express');
            const app = express();
            const router = express.Router();
    In the code snippet above, express.Router() is called to create a new router instance, and it is assigned to the router variable. This router can then be used to define routes and middleware specific to that router instance.
3. What do we use route middleware for?
    Route middleware in Express is used for performing additional processing or handling specific tasks before or after a route handler is executed.

    It allows you to add custom logic, perform authentication, validation, error handling, or any other operations specific to a particular route or group of routes.

    Route middleware enhances code reusability, modularity, and helps in implementing cross-cutting concerns efficiently within an Express application.


---
## Reflection 
1. What are your learning goals after reading and reviewing the [class README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-03/)

    In this class, the main learning goals are focused on building a web server that follows the principles of REST API using a framework called Express. Express servers can become complex, so one of the key concepts taught is how to break down the server code into smaller and more manageable modules using external (modular) routing. This approach helps keep the code organized and maintainable.

    Students will learn how to define routes for different actions such as creating, reading, updating, and deleting data (CRUD operations) in their API using Express. They will understand the different HTTP methods (POST, GET, PUT, DELETE) and how to map these methods to specific routes in their server.

    To work with a database, the class introduces Sequelize, a library that allows communication with SQL databases. Students will learn how to define models and schemas using Sequelize, which represent the structure of the data they want to store. They will then use these models to perform CRUD operations, such as creating new records, retrieving existing records, updating records, and deleting records in the database.

    Another important aspect covered in the class is handling request queries and parameters in routes. This allows the API to receive additional information from the client, such as filters or sorting instructions, and use that information to modify the response returned by the server.

    Lastly, the class teaches students how to test their code that relies on a Postgres Database server. Testing is an essential part of software development to ensure that the code works as intended and to catch any potential issues or bugs.

    Overall, the class aims to provide students with the knowledge and skills to build RESTful APIs using Express, work with databases using Sequelize, handle different types of requests, and effectively test their code.

2. Summarize the [class README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-03/)
### Express Router:

- Express Router allows you to modularize route handling logic by creating separate router instances using express.Router().
- You can define routes and middleware specific to each router instance and export the route definitions.
- In the main server file, you can require the route modules and use them with app.use() to integrate them into your application.

### CRUD Operations with REST and Express:

- Express provides the HTTP methods (app.post, app.get, app.put, app.delete) to perform CRUD operations in a REST API.
- These methods can be used to handle create, read, update, and delete operations for a specific resource.
- The route paths can include parameters (/resource/:id) to identify and perform operations on a specific resource.


### Route Prefixes:

- By using the app.use() method with a router instance, you can prefix all the routes defined in that router with a specific path.
- This allows you to group related routes under a common prefix, making the URLs more organized and manageable.


### Sequelize:

- Sequelize is a library used to communicate with SQL databases in Node.js applications.
- It provides an Object-Relational Mapping (ORM) for managing models and performing CRUD operations.
- You can configure Sequelize with your database environment details in a configuration file and use the provided methods to initialize, sync, and drop tables.


### Hosted Postgres Database:

- When deploying your application, you may need to connect to a cloud-hosted Postgres database.
- You can obtain the connection string for the database and store it in an environment variable like DATABASE_URL.
- Use the environment variable to establish the connection to the hosted Postgres database in your deployed application.

------------------------------------------------
return to [Main Reading File](./README.md)