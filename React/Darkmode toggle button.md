Create a folder in src and name it 'context'. In this folder, create the fila 'GlobalContext.js'

GlobalContext.js
```
import { createContext } from 'react';

export const GlobalContext = createContext(null);

export default GlobalContext;
```

Create the variables for the modes
```
export const themes = {
    light: {
        background: "white",
        text: "black"
    },
    dark: {
        background: "black",
        text: "white"
    }
}
```