+++
title = "How should I set the initial state of a class component?"
extra.tags =[ "react",]
created = "Jan 11, 2021 5:44 PM"
+++
# How should I set the initial state of a class component?


Before the ES2019 version of JavaScript you *had* to write your React classes like this if you wanted to set an initial state:

```jsx
class App extends Component {
  constructor() {
    super();
    this.state = {
      counter: 0,
    }
    this.setCounter = this.setCounter.bind(this);
  }

  setCounter() {
    this.setState((prevState) => ({
      counter: prevState.counter + 1,
    }));
  }

  render() {
    return (
      <div className='App'>
        <p>{title} {this.state.counter}</p>
        <button onClick={this.setCounter}>Add</button>
      </div>
    )
  }
}
```

With ES2019 we got [class fields](https://javascript.info/class#class-fields). This means we no longer *need* to set the state in the constructor:

```jsx
class App extends Component {
  state = {
    counter: 0,
  }

  setCounter = () => {
    this.setState((prevState) => ({
      counter: prevState.counter + 1,
    }));
  }

  render() {
    return (
      <div className='App'>
        <p>{title} {this.state.counter}</p>
        <button onClick={this.setCounter}>Add</button>
      </div>
    )
  }
}
```

But: if you already have a need for the constructor method for some reason it may be more readable to use the first version. But: this is more of a preference than a technical thing.