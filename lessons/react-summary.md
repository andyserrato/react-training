---
layout: lesson
title: "Conclusion"
permalink: /react-summary/
---

- Use NPM or Yarn for package management
- Use `create-react-app` to set up a new project
  - `npm install --global create-react-app`
- Use NPM commands to build and run the application
  - `npm start` for development
  - `npm build` to build for deployment
- React components are functions that generate page elements on the client
- Use JSX to embed HTML in JavaScript (in HTML in JavaScript in...)
  - Requires transpilation with Babel to convert to pure JavaScript
- Properties of HTML pseudo-element passed to React function in `props`
  - Write `<Greet company="Rangle.io"/>`
  - Calls `Greet(props={company: "Rangle.io"})`
  - Must return a single top-level HTML element
    - But that can contain many other elements generated by other components
- Use `prop-types` to specify what `props` must contain
- Use `className` instead of `class` to specify `class` property of HTML
- Two types of components:
  - Stateless (pure functional) components for display only
  - Stateful components (often classes) to contain state and handle events
- Stateful components maintain state in a member variable called `state`
  - Initialize with a single object in constructor
  - Always update with `this.setState({key: value, ...})`
    - Only need to pass in elements that are changing
  - `setState` triggers re-rendering of nested elements
  - React does work behind the scenes to minimize actual redrawing
- Lifecycle methods of class components are called at specific moments
  - `constructor` when component created (as usual)
  - `componentDidMount` when component added to DOM
  - `componentWillMount` called during server rendering
  - `componentWillUnmount` when component being removed
  - `shouldComponentUpdate` called after a component's props or state has changed.
  - `componentWillUpdate` and `componentDidUpdate` called before and after a component re-renders
  - `componentWillReceiveProps` called before a component has received props whose values have changed