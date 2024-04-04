
# React

React is an open-source JavaScript library developed by Facebook for building user interfaces, particularly for single-page applications and complex user interfaces. It's often used in conjunction with other libraries or frameworks, such as Redux for state management and React Router for routing.

Here are some key features and concepts of React:

### Component-Based: 
React is based on a component-based architecture, where UIs are built using reusable components. Components encapsulate both the UI and the logic associated with it, making it easier to manage and maintain large-scale applications.

### Virtual DOM: 
React uses a virtual DOM to efficiently update the UI. Instead of directly manipulating the browser's DOM, React creates a lightweight virtual representation of the DOM in memory. When the state of a component changes, React compares the virtual DOM with the previous version and only updates the parts of the actual DOM that have changed, minimizing DOM manipulation and improving performance.

### Declarative Syntax: 
React uses a declarative syntax, allowing developers to describe how the UI should look based on the current state, rather than imperatively specifying how to update the DOM. This makes the code more predictable, easier to understand, and less error-prone.

### JSX: 
JSX is a syntax extension for JavaScript that allows developers to write HTML-like code directly within their JavaScript files. JSX makes it easier to define UI components and their structure, and it's transpiled to regular JavaScript by tools like Babel before being executed by the browser.

### Unidirectional Data Flow: 
React follows a unidirectional data flow, where data flows in a single direction from parent components to child components. This makes it easier to understand how data changes propagate through the application and helps prevent unexpected side effects.

### Lifecycle Methods: 
React components have a set of lifecycle methods that allow developers to hook into various stages of a component's life, such as when it's first mounted to the DOM, when it's updated, and when it's about to be unmounted. These lifecycle methods can be used to perform tasks like fetching data, updating the UI, and cleaning up resources.

### Conclusion:
Overall, React provides developers with a powerful and efficient way to build interactive and dynamic user interfaces for web applications.


### Why virtual DOM:
Writing to the DOM is a pretty expensive operation in a browser. Hence changing 2-3 things line by line is going to be detremental to performance (because javascript is single threaded and interpreted line by line). React solves this problem by reconciing and grouping the changes, then writing those changes at once to the DOM, which in turn is less expensive.

### What is happening on render:
When rendering a react element, react converts the element to a type of (not really) JSON structure that would look something like this: https://youtu.be/i793Qm6kv3U?feature=shared&t=347

This is ultimately what you would call the virtual DOM.

### Reason for $$typeOf and Symbol in react
This exists to handle an edge case where the server you are making a request to is compormised and the server sends a request to render something. The Symbol here would generate a unique hash that would be used to validate the component, hence stopping the rogue component from rendering. 

```
Side notes: 

- The Symbol data type can not be rendered in a JSON format since 
JSON is a string and Symbol is a javascript object having a unique hash 
(which it does not expose outside of itself). The more you know.

- Also you could render your react component just returning the structure 
we previously described, but this would be inefficient and hard to maintain.

- Shadow DOM is different from the virtual DOM where in it is a web standard 
that enables encapsulation and isolation of DOM and CSS within web components. 
It allows developers to create reusable components with encapsulated structure 
and style, preventing conflicts with the rest of the page's styles or structure. 
It's used for composition, custom elements, and browser UI components,
providing a clean and isolated way to define the internals of components.
```

### Props in react
The props property is what is going to be rendered. You will find the ```children``` property being used here. This is what will be rendered inside of the react element, ultimately forming a tree like structure where the parent or main component will be the parent node and the children will be nested below it. This is why, in older react versions, you could render components dynamically when the components would get passed as props using the children property. Now you would use something like ```<Outlet/>```.



