## Search function

Create an array with users
```
const allUsers = [
  'user1',
  'user2',
  'user3',
  'user4'
];
```

Let's display this list using the map function
```
<ul>
    {users.map((user) => (
        <li key={user}>{user}</li>
    ))}
</ul>
```

Now we need to create the search input. Create the 'Search.js' file in the 'src' folder and include an input. This input listen to the value when it changes and passes te parameter

Search.js
```
function Search({onChange}) {
    return(
        <div>
            <input type="text" onChange={(e) => onChange(e.target.value)}/>
        </div>
    );
}

export default Search;
```

In the 'App.js' file import the 'Search' component and add the onChange attribute to expect a function
```
import Search from './components/Search';

<Search onChange={handleSearch} />
```

The 'handleSearch' function is a filter function
```
  const handleSearch = (text) => {
      const filteredUsers = usersList.filter((user) =>
        user.includes(text),
      );
      setUsers(filteredUsers);
  };
```

We need to set the useState hook
```
import { useState } from 'react';

const [users, setUsers] = useState(usersList);
```

The final 'App.js' should look like this:

App.js
```
import { useState } from 'react';
import Search from './components/Search'

const usersList = [
  'user1',
  'user2',
  'user3',
  'user4'
];

function App() {

  const [users, setUsers] = useState(usersList);

  const handleSearch = (text) => {
      const filteredUsers = usersList.filter((user) =>
        user.includes(text),
      );
      setUsers(filteredUsers);
  };

  return (
    <div className="App">
      <Search onChange={handleSearch} />

      <ul>
        {users.map((user) => (
          <li key={user}>{user}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```