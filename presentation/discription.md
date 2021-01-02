## JS libraries
A library is a reusable piece of code that offers specific functionality. It is a collection of functions, objects and classes that you can use in your application. Popular JavaScript libraries include: React, jQuery, D3. And today I will tell you some basic information about one of them – React. 

## Slide 1. React
React is a JavaScript library that specializes in helping developers build user interfaces, or UIs. In terms of websites and web applications, UIs are the collection of on-screen menus, search bars, buttons, and anything else someone interacts with to USE a website or app.
Before React JS, developers were stuck building UIs by hand with “vanilla JavaScript” (developer speak for the raw JavaScript language on its own) or with less UI-focused React predecessors like jQuery. That meant longer development times and plenty of opportunities for errors and bugs. So, in 2011, Facebook engineer Jordan Walke created React JS specifically to improve UI development. 

## Slide 2. React libraries
React is developed and maintained by Facebook, Instagram and the community of individual developers and corporations. React can be used to develop single page and mobile apps. Its goal is to provide high speed, simplicity and scalability. As a library for developing user interfaces, React is often used with other libraries such as MobX, Redux, and GraphQL.

## Slide 3 Websites which used React
There are many sites, that use Reactjs in Production. For example, Netflix, Khan Academy, Asana, Facebook, Airbnb, Reddit, BBC, UberEats.

## Slide 4. JSX, Virtual DOM
In addition to providing reusable React library code (saving development time and cutting down on the chance for coding errors), React comes with two key features that add to its appeal for JavaScript developers: JSX, Virtual DOM. To get an even better understanding of React JS and why you should use it, let’s take a look at both.

## Slide 5. JSX
JSX (short for JavaScript eXtension) is a React extension that makes it easy for web developers to modify their DOM by using simple, HTML-style code. And—since React JS browser support extends to all modern web browsers—JSX is compatible with any browser platform you working with.
Normally in frontend-related projects, we keep HTML, CSS, and JavaScript code in separate files. However, in React, this works a bit differently.

## Slide 5.1.
In React projects, we don't create separate HTML files, because JSX allows us to write HTML and JavaScript combined together in the same file, like in the example above. You can, however, separate your CSS in another file.
JSX is very practical, because we can also execute any JavaScript code (logic, functions, variables, and so on) inside the HTML directly by using curly braces { }.

## Slide 6. DOM
Using JSX to update a DOM leads to significant site performance improvements and development efficiency. It’s all about the React feature, the Virtual DOM.
At the heart of any basic website are HTML documents. Web browsers read these documents and display them on your computer, tablet, or phone as web pages. During this process, browsers create something called a Document Object Model (DOM), a representational tree of how the web page is arranged. Developers can then add dynamic content to their projects by modifying the DOM with languages like JavaScript.

## Slide 6.1. Virtual DOM
If a developer uses JSX to manipulate and update its DOM, React JS creates something called a Virtual DOM. The Virtual DOM (like the name implies) is a copy of the site’s DOM, and React JS uses this copy to see what parts of the actual DOM need to change when an event happens (like a user clicking a button). 

## Slide 6.2. 
Let’s say a user enters a comment in a blog post form and pushes the “Comment” button. Without using React JS, the entire DOM would have to update to reflect this change (using the time and processing power it takes to make this update). React, on the other hand, scans the Virtual DOM to see what changed after a user action (in this case, a comment being added) and selectively updates that section of the DOM only. This selective rendering provides a major performance boost. It saves the effort of recalculating the CSS style, layout for the page and rendering for the entire page.

## Slide 7. Components
React makes it much easier to create interfaces by breaking each page into small chunks. These fragments are called components. Each selection of the page shown in the figure is considered a component. Here is an example of pagination into components.

## Slide 7.1.
A component is a small reusable chunk of code. Components are the core building block of React apps. A React app can be seen as a component tree — having one root component (“App”) and then many nested child components.

## Slide 7.2.
These are like javascript functions. They accept arbitrary inputs (called “props”) and need to return/ render some JSX code (React elements) which describes what should appear on the screen. We can also use multiple JSX in a component. 
The two primary ways of declaring components in React is via functional components and class-based components. The above two components are equivalent from React’s point of view.

## Slide 8. Function Components
The simplest way to define a component is to write a JavaScript function: (рис. 2) This function is a valid React component because it returns a React element. We call such components “function components” because they are literally JavaScript functions. 
Now let’s see how we can create this functional component with 2 other different ways.

## Slide 8.1.
The second way is to use ES6 (ECMAScript 6) syntax for creating a functional component. For this we have to use the arrow function as below:

## Slide 8.2.
The third way of creating a functional component. Here also we will use ES6 but we will modify our arrow function. 

## Slide 8.3.
So a Functional Component in React:
•	is a JavaScript/ES6 function
•	must return a React element (JSX)
•	always starts with a capital letter (naming convention)
•	takes props as a parameter if necessary

## Slide 9. Class Components
You can also use an ES6 class to define a component. Different from functional components, class components must have an additional render( ) method for returning JSX. 

## Slide 9.1.
A Class Component:
•	is an ES6 class, will be a component once it ‘extends’ a React component.
•	takes Props (in the constructor) if needed
•	must have a render( ) method for returning JSX

## Slide 10. Rendering a Component
Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.
One of important concept of components is how they communicate. React has a special object called a prop (stands for property) which we use to transport data from one component to another. 
But props only transport data in a one-way flow (only from parent to child components). It is not possible with props to pass data from child to parent, or to components at the same level. 

## Slide 10.1.
Props are custom values and they also make components more dynamic. Since the React component is the child here, we need to define props on its parent (App), so we can pass the values and get the result simply by accessing the prop "name".

## Slide 11. Lifecycle Methods
You can think of React lifecycle methods as the series of events that happen from the birth of a React component to its death. Mounting – Birth of your component. Update – Growth of your component. Unmount – Death of your component.
•	render()
•	componentDidMount()
•	componentDidUpdate()
•	componentWillUnmount()
•	shouldComponentUpdate()
•	static getDerivedStateFromProps()
•	getSnapshotBeforeUpdate()


## Slide 11.1
The render () is the most used lifecycle method. It is a pure function. You cannot set state in render (). As the name suggests it handles the rendering of your component to the UI. It happens during the mounting and updating of your component.
The componentDidMount() happens as soon as your component is mounted. You can set state here but with caution. Method  is called as soon as the component is mounted and ready. This is a good place to initiate API calls, if you need to load data from a remote endpoint. Unlike the render() method, componentDidMount() allows the use of setState(). Calling the setState() here will update state and cause another rendering but it will happen before the browser updates the UI.

## Slide 11.2
The componentDidUpdate() happens as soon as the updating happens. You can set state here but with caution.
The componentWillUnmount() happens just before the component unmounts and is destroyed. This is a good place to cleanup all the data. You cannot set state here This component will never be re-rendered and because of that we cannot call setState() during this lifecycle method. 
The shouldComponentUpdate() can be used rarely. It can be called if you need to tell React not to re-render for a certain state or prop change. This needs to be used with caution only for certain performance optimizations. 

## Slide 11.3
The two new lifecycle methods are getDerivedStateFromProps() - Called just before calling the render() method. This is a static function that does not have access to “this“.  getDerivedStateFromProps() returns an object to update state in response to prop changes. It can return a null if there is no change to state.
and  getSnapshotBeforeUpdate() – It is called right before the DOM is updated. The value that is returned from getSnapshotBeforeUpdate() is passed on to componentDidUpdate().
They need to be used only occasionally. Not many examples are out there for these two methods and they are still being discussed and will have more references in the future.

## Slide 12.
More information about React you can find on the official site:
https://reactjs.org/
