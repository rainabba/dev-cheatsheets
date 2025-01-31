# State

## Props vs state

- `props` get passed **to** the component - similar to function parameters.
- `state `is managed **within** the component - similar to variables declared within a function.


## Library for state management

- [When should I use Redux?](https://redux.js.org/faq/general#when-should-i-use-redux) in Redux docs FAQ.

> You'll know when you need Flux. If you aren't sure if you need it, you don't need it.

> don't use Redux until you have problems with vanilla React.


## Basic state examples

See [State hook][] cheatsheet for more info.

[State hook]: {% link cheatsheets/javascript/packages/react/hooks/state.md %}

Here is how you use create an incrementing value based on a timer.

```jsx
class Timer extends React.Component {
  constructor(props) {
    super(props);
    this.state = { seconds: 0 };
  }

  tick() {
    this.setState(state => ({
      seconds: state.seconds + 1
    }));
  }

  componentDidMount() {
    this.interval = setInterval(() => this.tick(), 1000);
  }
```
