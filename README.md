# React Crash Course Cheat Sheet
This React cheat sheet is for my students who attend the three days React crash course. The React cheat sheet may be used and or copied by anyone.

## Hello World
```javascript
// Import React and ReactDOM
import React from 'react'
import ReactDOM from 'react-dom'

// Render component into the DOM
ReactDOM.render(
  <h1>Hello, World!</h1>,
  document.getElementById('main')
)
```

## Stateless Components
```javascript
// Stateless component
const title = () => {
  return <h1>React Crash Course Cheat Sheet</h1>
}

// Stateless component that receives properties
const description = (props) => {
  return <p>Today you will learn react, {props.name}</p>
}
```
