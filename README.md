# React Crash Course Cheat Sheet
This React cheat sheet is for my students who attend the three days React crash course. The React cheat sheet may be used and or copied by anyone.

## Hello World
```javascript
// Import React and ReactDOM.
import React from 'react'
import ReactDOM from 'react-dom'

// Render component into the DOM.
ReactDOM.render(
  <h1>Hello, World!</h1>,
  document.getElementById('root')
)
```

## Stateless Components
```javascript
// Stateless component.
const Title = () => {
  return <h1>React Crash Course Cheat Sheet</h1>
}
```

```javascript
// Stateless component that receives properties.
const Description = (props) => {
  return <p>In the upcoming three days you will learn the basics of react, {props.name}.</p>
}
```

```javascript
// Component can only return one element.
const Introduction = () => {
  return (
    <section>
      <Title />
      <Description name="Peter"/>
    </section>
  )
}
```
Find more information about [components and props](https://facebook.github.io/react/docs/components-and-props.html) on the React documentation page.

## Class
```javascript
// use classes to create a component with state.
import { Component } from 'react'

class App extends Component {
  constructor(props) {
    super(props)
    this.state = {date: new Date()}
  }
  
  render() {
    return (
      <p>
        Today it is {this.state.date.toLocaleTimeString()}.
      </p>
    )
  }
}
```

## Component Lifecycle
Each component has several "lifecycle methods" that you can override to run code at particular times in the process. Methods prefixed with **will** are called right before something happens, and methods prefixed with **did** are called right after something happens.

```javascript
componentWillMount() {
  // function is called immediately before the initial render
}

componentDidMount() {
  // function is called immediately after the initial render
}

componentWillReceiveProps() {
  // function is called when component is receiving new props
}

shouldComponentUpdate() {
  // function is called before rendering with new props or state
}
 
componentWillUpdate() {
  // function is called immediately before rendering
}

componentDidUpdate() {
  // function is called immediately after rendering
}

componentWillUnmount() {
  // function is called immediately before component is unmounted from DOM
}
```

Find more information about [component lifcycle](https://facebook.github.io/react/docs/react-component.html#the-component-lifecycle) on the React documentation page.

## Conditional Rendering
In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.
```javascript
render() {
  const {isLoggedIn, username} = this.state
  return (
    <div className={`${isLoggedIn ? 'login' : 'logout'}`}>
      {isLoggedIn ? <p>Logged in as {username}.</p> : <p>Logged out.</p>}
    </div>
  )
}
```

## More Information
* [Documentation](https://facebook.github.io/react/docs)
* [Github](https://github.com/facebook/react)
* [Create React apps with no build configuration](https://github.com/facebookincubator/create-react-app)
* [React developer tools for chrome](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
