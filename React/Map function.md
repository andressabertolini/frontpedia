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
