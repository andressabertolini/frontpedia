```
import React, { Component } from 'react';

class MyComponent extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  }

  render() {
    return (
      <div>
        <p>Contador: {this.state.count}</p>
        <button onClick={this.increment}>Incrementar</button>
      </div>
    );
  }
}

export default MyComponent;
```

Lifecycle
- Mounting
componentWillMount()
render() - first time
componentDidMount()

- Updating
getDerivedStateFromProps()
getSnapshotBeforeUpdate()
componentDidUpdate() - side effects
render() - updates the component

- Unmounting
componentWillUnmount() - cleanup