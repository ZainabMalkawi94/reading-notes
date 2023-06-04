# reading-notes

# Table of contents
1. [Node Ecosystem](#NodeEcosystem)
2. [Express, NPM, TDD, CI/CD](#Express)



## Class - 1 - Node Ecosystem <a name="NodeEcosystem"></a>
The Node.js ecosystem is a robust and diverse collection of tools, libraries, and frameworks built around Node.js, enabling developers to create scalable and efficient server-side applications using JavaScript.

1. How would you describe Node to a non-technical friend?

Node.js is a runtime environment that allows you to run JavaScript code outside of a web browser. It's like a powerful engine that can execute JavaScript on a computer or server. While JavaScript is commonly used for front-end development, Node.js extends its capabilities to server-side programming. Overall, Node.js opens up new possibilities for JavaScript developers, allowing them to use their skills not only in the browser but also on servers and other platforms. It's a versatile tool that brings JavaScript to new domains and helps create fast, scalable, and real-time applications.




2. What does it mean that Node is a JavaScript runtime?
When we say that Node is a JavaScript runtime, it means that it provides an environment for executing JavaScript code. Typically, JavaScript code is executed within a web browser, where the browser's JavaScript engine interprets and runs the code. Node.js, however, extends the capabilities of JavaScript by providing a separate runtime environment outside of the browser. It includes its own implementation of the JavaScript engine (V8 engine, developed by Google) that allows JavaScript code to be executed directly on a computer or server, without the need for a browser.

3. What is Node used for?
Node.js is used for building scalable, server-side applications and real-time web applications, leveraging JavaScript to handle concurrent connections efficiently and deliver high-performance solutions.

-----------------------------------------------------------------------------------------------------------------------

1. Looking ahead at this module’s course schedule, What do you look forward to learning?
When encountering the title "Node Ecosystem," you can anticipate learning about the vast array of frameworks, libraries, and tools within the Node.js community. 

2. What are your learning goals after reading and reviewing the class README?
After reviewing the Node.js ecosystem, your learning goals may include gaining a comprehensive understanding of its frameworks, libraries, and tools, and applying that knowledge to build scalable applications while staying updated on the latest trends and best practices.

-------------------------------------------------------------------------------------------------------------
## Class - 2 - Express, NPM, TDD, CI/CD <a name="Express"></a>
### An introduction to NodeJS and Express

1. Explain middleware, answer as though I were a non-technical recruiter.
In software development, middleware can be described as a bridge between different components of a software system. It acts as a mediator, helping these components communicate and work together effectively. It's like a helpful assistant that manages and processes data as it moves through the different parts of an application. Middleware allows developers to add extra features, validate data, handle errors, and ensure smooth interactions between different parts of the application without needing to make direct changes to the core components. It's a flexible tool that enhances the functionality and efficiency of software systems.

2. Express the most popular __ __ ____.
Node.js frameworks.

3. Express is “unopinionated.” What does that mean?
Express being "unopinionated" means it does not impose strict conventions or dictate specific architectural choices. It offers flexibility for developers to design and structure their application according to their preferences. This allows for greater customization but requires more decision-making from the developer.

4. What is a module and why is modularity useful to us as developers?
A module is a self-contained and reusable unit of code that encapsulates related functionality. Modularity is useful to developers as it promotes code organization, reusability, and maintainability. It allows us to break down complex systems into smaller, manageable parts, making development and collaboration easier while enhancing code readability and reducing duplication.


### What is NPM?

1. What version of npm are you running on your machine?
npm -v : 9.6.7

2. What command would you type to install a library/package called ‘jshint’ into your node project?
To install the 'jshint' library/package into a Node.js project, you would typically use the following command:
"npm install jshint"
This command will use npm (Node Package Manager) to download and install the 'jshint' package from the npm registry into your project's 'node_modules' directory.


### What is TDD?

1. Explain why tests are important. Please explain as though I were your non technical elder.
Tests are important because they ensure that the software we build works correctly and reliably. They act as a safety net, helping us catch and fix issues before they cause problems. By running tests, we gain confidence that our software will function as intended, providing a better experience for users and avoiding potential complications down the line.

2. What are three expected benefits of testing
Testing provides three expected benefits:

- Bug Detection: Tests help uncover bugs and errors in software. By running various test cases, we can identify issues early on, allowing developers to fix them before they become larger problems.

- Software Reliability: Testing enhances the reliability of software by verifying that it functions correctly in different scenarios. Through comprehensive testing, we can ensure that the software behaves as expected and delivers accurate results.

- Maintainability: Tests make software more maintainable by serving as documentation for the expected behavior of the code. When making changes or adding new features, tests act as a safety net, allowing developers to confidently modify code without introducing unintended side effects.


3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
Individual pitfalls commonly encountered while writing tests:

1. Overlooking edge cases: One pitfall is not considering all possible scenarios and failing to write tests for edge cases. This can lead to insufficient coverage and missed bugs.

2. Writing overly complex tests: Another pitfall is creating tests that are overly complex or tightly coupled with the implementation details. This can make the tests difficult to understand, maintain, and update when the code changes.

Team pitfalls commonly encountered while writing tests:

1. Lack of communication and collaboration: When team members fail to communicate effectively about testing strategies and requirements, it can result in inconsistent test coverage, duplication of effort, or gaps in testing.

2. Neglecting test maintenance: Sometimes, teams focus on writing tests initially but fail to maintain and update them as the codebase evolves. Outdated or broken tests can lead to false positives/negatives and reduce the effectiveness of the test suite. Regular test maintenance is crucial to ensure their ongoing usefulness.


### CI/CD

1. What are three benefits of Continuous Integration?

Continuous Integration (CI) offers the following benefits:

1. Early Bug Detection: By automatically building and testing code changes, CI helps identify and address bugs early in the development process. This prevents issues from affecting the main codebase and allows for faster bug resolution.

2. Faster Feedback Loop: CI provides immediate feedback to developers about the quality and integration of their code changes. This reduces the time spent on manual testing and waiting for results, enabling faster iterations and quicker software delivery.

3. Increased Collaboration: CI fosters collaboration by creating a shared and automated environment for integrating code changes. It improves communication, detects conflicts early on, ensures up-to-date code for all team members, and facilitates the resolution of integration issues that can arise during concurrent development.


2. What is the difference between Continuos Delivery and Continuous Deployment?

Continuous Delivery is the practice of continuously delivering software to a production-like environment for testing and validation, while Continuous Deployment takes it a step further by automatically deploying the software to production after passing all tests and quality checks. While they are different, continuous deployment is an extension of the continuous delivery concept.

3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background
GitHub is a collaborative platform for software development that supports Continuous Integration and Continuous Deployment. It serves as a central repository for code, allowing teams to track changes and collaborate through pull requests and code reviews. Integrated with CI tools, GitHub automates the building and testing of code changes, ensuring continuous validation. It also seamlessly integrates with deployment platforms, enabling automated deployment of validated code to production environments.