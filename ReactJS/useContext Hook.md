## useContext Hook

Context: a way to store data and have it be accessible to components no matter where they are without having to pass it through props

```
import { createContext } from 'react';

import { User } from '../useContext';

export const DashboardContext = createContext<User | undefined>(undedfined);
```

Provider
Consumer