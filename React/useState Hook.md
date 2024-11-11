## UseState Hook

State - data that changes

useState is the react hook that you use to manipulate state

```
import { useState } from 'react';

const [variable, setVariable] = useState(0);

{ variable }

setVariable(variable + 1);
```

If you don't provide a value, it is gonna be undefined