# What is ReactJS?
ReactJS is an open-source front-end JavaScript library for building user interfaces. ReactJS is maintained by Facebook and a community of individual developers and companies. It is widely used as a base in building single-page websites and mobile applications. It is very easy to use, and it allows users to create reusable UI components.

# Getting Started with Create React App
Install Node and npm
(https://nodejs.org/en/download/)

    npx create-react-app my-app
    cd my-app
    npm start

## Features
JSX : JSX is an extension to javascript. Though it is not mandatory to use JSX in react, it is one of the good features and easy to use.

Components: Components are like pure javascript functions that help make the code easy by splitting the logic into reusable independent code. We can use components as functions and components as classes. Components also have a state, props which makes life easy. Inside a class, the state of each of the props is maintained.

Virtual DOM: React creates a virtual dom, i.e., in-memory data -structure cache. Only the final changes of DOM has later updated in the browsers DOM.

Javascript Expressions: JS expressions can be used in the jsx files using curly brackets, for example {}.


# What are Components in ReactJS?
Components are like pure javascript functions that help make the code easy by splitting the logic into reusable independent code.

A piece of code that we can reuse by importing it

## Statefull / Stateless Components
Simply In Statefull we use state and in Stateless we don't.


## Components as functions:
    
    import React from 'react';
    import ReactDOM from 'react-dom';
    function Hello() {
        return <h1>Hello</h1>;
    }
    const Hello_comp = <Hello />;
    export default Hello_comp;
We have created a function called Hello that returned h1 tag as shown above. The name of the function acts as an element, as shown below:
    
    const Hello_comp = <Hello />;
    export default Hello_comp;
The Component Hello is used as an Html tag, i.e., <Hello /> and assigned to Hello_comp variable and the same is exported using export.

Let us now use this component in index.js file as shown below:
    
    import React from 'react';
    import ReactDOM from 'react-dom';
    import Hello_comp from './test.jsx';
    
    ReactDOM.render(
        Hello_comp,
        document.getElementById('root')
    );

## Class as Component:
Here is a ReactJS example that uses a class as a component.

test.js

    import React from 'react';
    import ReactDOM from 'react-dom';
    
    class Hello extends React. Component {
    render() {
        return <h1>Hello</h1>;
    }
    }
    export default Hello;
We can use Hello component in index.js file as follows:

index.js
    
    import React from 'react';
    import ReactDOM from 'react-dom';
    import Hello from './test.js';
    
    ReactDOM.render(
        <Hello />,
        document.getElementById('root')
    ); 

# What is a State in ReactJS?
A state is a javascript object similar to props that have data to be used with the reactjs render. The state data is a private object and is used within components inside a class.


Example of State
Here is a working example on how to use state inside a class.

test.js

    import React from 'react';
    import ReactDOM from 'react-dom';
    
    class Hello extends React.Component {
        constructor(props) {
            super(props);
            this.state = {
                 msg: "Hello!"
            }
        }
        render() {
             return <h1>{this.state.msg}</h1>;
        }
    }
    export default Hello;
index.js

    import React from 'react';
    import ReactDOM from 'react-dom';
    import Hello from './test.js';
    
    ReactDOM.render(
        <Hello />,
        document.getElementById('root')
    );  


# What are Props in ReactJS?
Props are properties to be used inside a component. They act as global object or variables which can be used inside the Component.

## Props to Function Component
Here is an example of passing props to a function component.

    import React from 'react';
    import ReactDOM from 'react-dom';
    function Hello(props) {
        return <h1>{props.msg}</h1>;
    }  
    const Hello_comp = <Hello msg="Hello!" />;
    export default Hello_comp;
As shown above, we have added msg attribute to <Hello /> Component. The same can be accessed as props inside Hello function, which is an object that will have the msg attribute details, and the same is used as an expression.

The component is used in index.js as follows:

index.js

    import React from 'react';
    import ReactDOM from 'react-dom';
    import Hello_comp from './test.jsx';
    
    ReactDOM.render(
        Hello_comp,
        document.getElementById('root')
    ); 

## Props to Class Component
To access the props in a class we can do it as follows:

test.jsx

    import React from 'react';
    import ReactDOM from 'react-dom';
    
    class Hello extends React.Component {
        render() {
        return <h1>{this.props.msg}</h1>;
        }
    }
    export default Hello;
The msg attribute is passed to the component in index.js as follows:

    import React from 'react';
    import ReactDOM from 'react-dom';
    import Hello from './test.jsx';
    
    ReactDOM.render(
    <Hello msg="Hello, from Guru99 Tutorials!" />,
    document.getElementById('root')
    ); 

# Life Cycle of a Component
A component life cycle is divided into Initialization, Mounting, Update, and UnMounting stages.

Here is a detail explanation about each Component.

A component in reactjs has the following stages :

\
**Initialization**: This is the first stage of the component life cycle.
Here it will have the default props and the state at the initial level.


\
**Mounting**: In this phase, the Component is rendered inside the dom. We having exposure to following methods in the mounting state.

*componentDidMount()*: This is also called when the Component is just added to the dom.

*render()*: You have this method for all the components created. It returns the Html node.


\
**Update**: In this state, the dom is interacted by a user and updated. For example, you enter something in the textbox, so the state properties are updated.

Following are the methods available in update state:

*shouldComponentUpdate()* : called when the component is updated.

*componentDidUpdate()* : after the component is updated.

\
**UnMounting**: this state comes into the picture when the Component is not required or removed.

# JSX
Jsx is shorthand for Js Xml its allows html code inside javascript code directly



# Real Dom vs Virtual Dom
- Updates Slow / Update Faster
- Directly Update Html / Can't Update Directly
- Create A New DOM on Element Update / Update JSX If Element Update(reconstruct)
- Too Much Memory Wastage / No Memory Wastage




# IMP Links
React Official Docs

(https://reactjs.org/)

(https://react-bootstrap.github.io/)

Tutorials

(https://www.guru99.com/reactjs-tutorial.html)


YouTube
    
(https://www.youtube.com/playlist?list=PL8p2I9GklV44oDSE3j-E-OkvxFkz5a1d8)

(https://youtu.be/4UZrsTqkcW4)
