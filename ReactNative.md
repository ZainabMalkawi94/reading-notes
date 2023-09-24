## React Native

### Getting started with react native
1. Name three Core Components of React Native and describe what they do.

    1. Three core components of React Native are:
    - **View**: The View component serves as a fundamental building block for creating the user interface. It acts as a container for other components and can style and arrange them within the layout.
    - **Text**: Text is used to display text content on the screen. It supports styling and formatting of text, making it suitable for displaying labels, headings, and paragraphs.
    - **Image**: The Image component allows you to display images in your app. It can load local or remote images and provides options for resizing and controlling aspect ratios.


2. What problem does React Native solve (why call it native)?


     React Native solves the problem of cross-platform mobile app development by allowing developers to write code in JavaScript and React and then compile it to native code for both iOS and Android platforms. It's called "native" because the resulting apps are not web-based; they run on the device's native code, providing a native look and feel.




3. What are the building blocks of a React Native app? How does that compare to a React app?

    The building blocks of a React Native app include:
    - **Components**: Components are the UI elements of the app, similar to how React web apps are built.
    - **JavaScript**: React Native uses JavaScript for defining components, logic, and behavior.
    - **Native Modules**: Developers can access native device features and APIs using native modules written in Java (for Android) and Objective-C or Swift (for iOS).
    - **Bridge**: React Native uses a bridge to communicate between JavaScript code and native code, enabling seamless interaction with device features.
    Compared to a React web app, React Native apps have the same component-based structure and JavaScript as the building blocks, but they also include native modules and a bridge for communication with the device's native capabilities.
---
### expo
1. What solution does expo provide?

    Expo provides a simplified development platform for building React Native apps, offering a range of tools and libraries to streamline app development.



2. Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow.

    Expo is known for its "developer-friendly" workflow, as it aims to manage a significant portion of the complexity involved in building mobile apps.




3. What is the difference between React Native and Expo?

    The main difference between React Native and Expo is that React Native is a framework that provides more flexibility and allows direct access to native modules and code, while Expo is a higher-level set of tools and services built on top of React Native, offering a more opinionated and streamlined development experience but with some limitations on native module usage and configurability.
---
### expo snack
1. Checkout this tool. What does snack allow you to do?

    Expo Snack is an online platform that allows developers to quickly prototype and experiment with React Native code in a web-based code editor. It offers the following capabilities:

    1. **Code and Preview**: Developers can write React Native code directly in the web-based editor and immediately see the live preview of their app on the right side of the screen. This allows for rapid development and testing.

    2. **Sharing**: Snack enables users to easily share their code and project with others. You can generate a shareable link to your Snack project, making it simple to collaborate or seek help from the community.

    3. **Library Integration**: Snack comes with built-in support for many popular JavaScript libraries and npm packages. You can add and use these libraries in your project to extend its functionality.

    4. **Cross-Platform**: Developers can use Snack to build and preview apps for both iOS and Android platforms within the same environment.

    5. **No Setup**: Snack eliminates the need for setting up a development environment on your local machine, making it accessible for beginners and experienced developers alike.

    In essence, Expo Snack provides a convenient and accessible way to experiment with React Native code, share projects, and quickly see the results in a live preview. It's a valuable tool for learning, prototyping, and collaboration in the React Native development ecosystem.
---
### ejecting

1. What does “eject” mean within the context of Expo?

    In the context of Expo, "eject" refers to the process of transitioning from the managed workflow to the bare workflow. The managed workflow in Expo abstracts many of the native development complexities and provides a high-level development environment, while the bare workflow allows for more direct control over native code and dependencies.


2. When should you not eject?

    You should not eject from Expo when you want to maintain the simplicity and ease of development offered by the managed workflow, especially if your project doesn't require extensive customization of native code or specific native modules. Ejecting introduces more complexity and requires additional knowledge of native development.


3. Why might you choose to eject?

    You might choose to eject from Expo when you need more control over your project's native code, want to add custom native modules, or have specific requirements that are not supported by Expo's managed workflow. Ejecting allows you to access and modify native code directly, giving you the flexibility to integrate third-party libraries and make low-level customizations to your app. However, it comes with the trade-off of increased complexity and maintenance responsibilities.
-----------
return to [Main Reading File](./README.md)