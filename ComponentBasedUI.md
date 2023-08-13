## Component Based UI


### React Quick Start
1. What are the building blocks of a React app?

    Components, Props, State.

2. What is the difference between an HTML element and a React component?

    HTML elements and React components are both building blocks used in web development, but they serve different purposes and have some key differences:

    1. **Nature**:
        - **HTML Elements**: HTML (Hypertext Markup Language) elements are the basic building blocks of web pages. They define the structure and content of a webpage. HTML elements are predefined by the HTML specification and represent different types of content like headings, paragraphs, lists, links, forms, etc.
        - **React Components**: React components are building blocks used in building user interfaces with React, a JavaScript library for creating interactive and reusable UI components. React components encapsulate logic, state, and UI elements into reusable and modular pieces.

    2. **Definition**:
        - **HTML Elements**: HTML elements are defined using HTML tags (e.g., `<div>`, `<p>`, `<a>`, `<input>`). They have predefined attributes that control their behavior and appearance.
        - **React Components**: React components are defined using JavaScript classes or functions. They can be custom-defined by developers to encapsulate specific behavior, state, and rendering logic.

    3. **Usage**:
        - **HTML Elements**: HTML elements are part of the HTML markup and are used to structure the content of a webpage. They can be combined to create the desired layout and visual presentation.
        - **React Components**: React components are used to build dynamic and interactive user interfaces. They can include rendering logic, manage state, handle user interactions, and encapsulate complex UI behaviors.

    4. **Reusability**:
        - **HTML Elements**: HTML elements can be reused across different web pages, but the logic associated with them is typically limited to basic behaviors like links or forms.
        - **React Components**: React components promote reusability and modularity. They can be reused across different parts of a single application or even across multiple applications.

    5. **Interactivity**:
        - **HTML Elements**: HTML elements can have static behavior and require external scripts or styles to add interactivity.
        - **React Components**: React components can manage their own state, respond to user interactions, and update the UI in a dynamic way. They make it easier to build interactive and real-time applications.

    6. **Data Flow**:
        - **HTML Elements**: HTML elements are mostly static and rely on attributes and external scripts to update their content.
        - **React Components**: React components can manage their own internal state and also receive data (props) from their parent components, making it easy to manage and pass data throughout the application.


3. What is JSX and why do we use it?

    JSX (JavaScript XML) is a syntax extension for JavaScript used in React. It allows developers to write HTML-like code within their JavaScript, making it easier to create and visualize complex UI structures. JSX is compiled to regular JavaScript and enables seamless integration of logic and UI, enhancing the readability and maintainability of React components.
4. Describe the process of embedding JavaScript expressions in JSX.

    In JSX, you can embed JavaScript expressions using curly braces `{}`. Simply place the expression within the curly braces within your JSX code, and it will be evaluated and rendered as part of the component's output. This enables dynamic content, variable values, and calculations to be seamlessly integrated into the rendered UI.

5. Does React or JSX have any special features for iteration or conditional logic?

    Yes, React supports iteration and conditional logic through JavaScript constructs. For iteration, you can use the `.map()` method to render arrays of components dynamically. For conditional rendering, you can use conditional statements like `if` or the ternary operator within JSX curly braces to control whether components are rendered based on certain conditions.

6. How does React know to respond to a user’s inputs?

    React responds to user inputs through event handling. Event listeners, such as `onClick`, `onChange`, etc., are attached to JSX elements. When users interact with these elements, events are triggered, invoking corresponding event handler functions. React then updates the component's state or triggers re-rendering, reflecting changes in the UI based on user actions.
7. What word indicates that a React component manages data with a Hook?

    The term is "useState." In React, the `useState` hook allows a component to manage and update its state, enabling dynamic data handling and reactivity without using class components or external state management libraries.

8. How can two react components share data?

    Two React components can share data by using "props." One component can pass data down to another component through props, which are essentially parameters passed during component rendering. The receiving component can then access and utilize the passed data for rendering or internal logic, creating a data flow between the parent and child components.
---
### Render and Commit
1. What are the three steps of refreshing a React UI?
The three steps to refresh a React UI are:

    1. **State Update**: Modify the component's state using `setState` or a state management hook like `useState`.
    2. **Reconciliation**: React compares the previous and updated states, identifies the changes, and calculates the minimal set of updates needed to reflect those changes in the virtual DOM.
    3. **Render**: React re-renders the component and its affected child components, updating only the necessary parts of the actual DOM to reflect the changes made in the state.

    This process ensures efficient updates and a responsive user interface.
2. How do you trigger updates to a component after the initial render?
    In React, you can trigger updates to a component after the initial render using two main approaches:

    1. **State Updates**: Call the `setState` method (in class components) or use a state management hook like `useState` (in functional components) to modify the component's state. When the state changes, React automatically triggers a re-render of the component and updates the UI.

    2. **Props Changes**: If a parent component passes new props to a child component, the child component will re-render to reflect the updated props. This is a fundamental way to trigger updates in child components based on changes in parent components.

3. Does React recreate DOM nodes on every rerender?

    No, React uses a process called reconciliation to update only the parts of the DOM that have changed between renders. It calculates the minimal changes needed to bring the virtual DOM in sync with the actual DOM, resulting in efficient and optimized updates. This approach avoids unnecessary recreation of DOM nodes on every re-render.
4. After React has updated the DOM, what still needs to happen before the user sees the change?

    After React updates the DOM, the browser needs to perform "layout" and "paint" operations. Layout calculates the final position and size of elements, while paint involves filling in pixels with colors and images. Once these processes are complete, the updated UI becomes visible to the user, ensuring a smooth and accurate rendering of the changes.
----------------------
return to [Main Reading File](./README.md)