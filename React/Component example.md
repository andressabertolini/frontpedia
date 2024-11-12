## Component Example

A component is a piece of the UI (user interface) that has its own logic and appearance

React components are JavaScript functions that return markup

Example 1
```
const Hello = () => {
    return(
        <div>Hello!</div>
    );
}

export default Home;
```

Example 2
```
function Hello() {
  return (
    <div>Hello</div>
  );
}
```

> [!NOTE]
> React component names must always start with a capital letter, while HTML tags must be lowercase