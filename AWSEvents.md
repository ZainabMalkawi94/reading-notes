## AWS:Events

### 1.What is the difference betweeen SQS and SNS?
SQS is primarily used for queuing and asynchronous communication, while SNS is used for real-time, push-based messaging to multiple subscribers. Depending on your application's needs, you might choose one or both services to achieve the desired decoupling and scalability.

### 2.What are some use cases for both SNS and SQS?
- Send notifications about events and updates to multiple recipients.
- Deliver push notifications to mobile app users across various platforms.
- Distribute messages to multiple microservices, applications, or instances in a fan-out pattern.
_ _ _
### 1.Describe how to use SQS and SNS in a “fanout” pattern.
In a "fanout" pattern, you can combine SQS and SNS to broadcast a single message to multiple subscribers (consumers) simultaneously. Here's how you can implement this pattern:

* Create an SNS Topic: First, you need to create an SNS topic. This topic acts as the central point for broadcasting messages.

* Create SQS Queues: Create multiple SQS queues, each representing a different subscriber or group of subscribers. These queues will receive copies of the messages published to the SNS topic.

* Subscribe SQS Queues to the SNS Topic: Subscribe each SQS queue to the SNS topic. This step enables the queues to receive messages from the topic when they are published.

* Publish Messages to SNS Topic: Whenever you have a message that needs to be sent to multiple subscribers, publish it to the SNS topic.

* Message Distribution: SNS will automatically fan out the message to all the SQS queues that are subscribed to the topic. Each queue will receive a copy of the message, and their consumers can then process the messages independently.

### 2.Explain how “push notifications” work, using SNS.
* Mobile App Registration: The mobile app that wishes to receive push notifications registers with a push notification service like Apple Push Notification Service (APNS) for iOS devices, Firebase Cloud Messaging (FCM) for Android devices, or other platform-specific services. These services provide the necessary credentials and tokens to identify the app and the device.

* Create an SNS Platform Application: In the AWS Management Console, you create an SNS Platform Application for the target platform (e.g., APNS, FCM, etc.). You configure the application with the necessary credentials provided by the platform-specific service.

* Create an SNS Topic: Create an SNS topic to which you want to send push notifications.

* Subscribe Endpoints: The mobile app's backend server (or any other service) subscribes the SNS Platform Application to the SNS topic. This creates a connection between the SNS topic and the mobile app's push notification service.

* Send Push Notifications: When you have a message or notification to send to the mobile app users, you publish the message to the SNS topic.

* SNS Delivery: SNS will forward the message to the subscribed endpoints (registered mobile devices) via the configured push notification service (APNS, FCM, etc.).

* Device Reception: The push notification service delivers the message to the target devices, and the mobile app displays the notification to the user in real-time.

_ _ _
### 1.How might a large scale, distributed application make use of a Queue system like SQS?
A large-scale, distributed application can make extensive use of a queue system like Amazon SQS to handle various aspects of its architecture and communication between different components. Here are some ways a distributed application might leverage SQS:

* Decoupling Services: In a distributed architecture, services are often decoupled to allow them to operate independently and be more scalable. SQS acts as a buffer between services, enabling asynchronous communication. Services can produce messages (tasks, events, requests) and put them in an SQS queue, while other services consume messages from the queue at their own pace. This decoupling ensures that a slow or temporarily unavailable consumer doesn't affect the producer or vice versa.

* Load Balancing: In a scenario where one service is generating a large number of requests, you can use SQS to distribute those requests among multiple instances or workers. The requests are placed in an SQS queue, and the instances consume messages from the queue, ensuring a balanced load distribution.

* Background Jobs and Task Processing: SQS is well-suited for managing background tasks and long-running processes. Large-scale applications often have numerous tasks that can be processed asynchronously, such as image or video processing, data analysis, and more. The application can enqueue these tasks in an SQS queue, and a pool of workers can pick up tasks from the queue and process them.

-----

return to [Main Reading File](./README.md)