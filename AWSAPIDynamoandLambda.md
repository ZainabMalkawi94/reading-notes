## AWS: API, Dynamo and Lambda

### AWS API Gateway Overview
1. What is Amazon API Gateway?

    Amazon API Gateway is a fully managed service by AWS that allows developers to create, publish, and manage APIs securely at any scale. It acts as a front door for applications to access data, services, or functionalities from backend services like AWS Lambda, EC2, or HTTP endpoints.


2. Why is Amazon API Gateway an important part of the Serverless ecosystem?

    Amazon API Gateway is crucial in the Serverless ecosystem because it enables serverless applications to expose APIs easily, abstracting the complexities of managing infrastructure. It seamlessly integrates with AWS Lambda, facilitating event-driven architectures and enabling cost-effective, auto-scaling, and highly available serverless solutions.


3. How does API Gateway integrate with other AWS services?

    Amazon API Gateway integrates with other AWS services through seamless connections and configuration options. It can directly link with AWS Lambda functions, AWS HTTP endpoints, and AWS service integrations, allowing APIs to access various AWS resources and functionalities. Additionally, API Gateway provides built-in authorization and authentication options, ensuring secure interactions with integrated services.


---
### AWS API Gateway

1. What are the some benefits of using Amazon API Gateway?

    1. Simplifies API management and deployment with a fully managed service.
    2. Provides robust security features like authentication, authorization, and throttling.
    3. Supports caching, allowing improved performance and reduced backend load.

2. What two API types might you choose from?
    1. REST APIs: Suitable for traditional HTTP-based interactions with clear URL structures.
    2. WebSocket APIs: Ideal for real-time, bidirectional communication enabling features like chat applications and live updates.
---

### AWS DynamoDB Guide


1. What is DynamoDB?

    DynamoDB is a fully managed NoSQL database service by AWS, offering seamless scaling, low latency, and high availability for applications with any scale of workload.

2. Under what circumstances would you recommend DynamoDB over MongoDB?

    DynamoDB might be recommended over MongoDB for projects that require automatic scaling and minimal administrative overhead, as DynamoDB handles these aspects for you. Additionally, DynamoDB is well-suited for applications with unpredictable or rapidly changing workloads due to its serverless architecture.

---- 
### AWS DynamoDB

1. Explain to a non-technical friend how DynamoDB works.
    To a non-technical friend, DynamoDB is like a magical notebook where you can store any kind of information easily. It automatically makes more notebooks when needed, so you never run out of space, and you can quickly find your notes whenever you want!

---
### Dynamoose

1. What is Dynamoose?

     Dynamoose is an Object Data Modeling (ODM) library for Node.js, designed to simplify interactions with DynamoDB by providing a more intuitive and familiar programming interface.
2. What are some key features of Dynamoose?

    Key features of Dynamoose include easy schema definition, automatic data validation, middleware support, and integration with AWS DynamoDB without the need for complex AWS SDK interactions.

------------------------------------------
return to [Main Reading File](./README.md)