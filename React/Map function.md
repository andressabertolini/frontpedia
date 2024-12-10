```
const usersList = [
  'user1',
  'user2',
  'user3',
  'user4'
];

function App() {
  return (
    <div className="App">
      <ul>
        {usersList.map((user) => (<li key={user}>{user}</li>))}
      </ul>

      <ul>
        {usersList.map((user) => (
          <li key={user}>{user}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

> [!NOTE]
> Basic structure: m.map(item => item)

If the keys are strings or unique values ​​that don't repeat, React works without any issues. But if noy, the key needs to be something else. Example:

```
const usersList = ['user1', 'user1', 'user2'];
```
Here, "user1" is repeated. If you use the same value as the key, React won't be able to differentiate between these elements, which causes a problem in the virtual DOM. The ideal is to use unique identifiers

```
const usersList = [
  { id: 1, name: 'user1' },
  { id: 2, name: 'user2' },
  { id: 3, name: 'user3' },
];

usersList.map((user) => (
  <li key={user.id}>{user.name}</li>
))
```