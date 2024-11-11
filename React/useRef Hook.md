## useRef Hook

Similar to state but doesn't trigger a re-render of a component

The value will always be inside the .current 

```
import { useRef } from 'react';

const countRef = useRef(0);

console.log(countRef.current);
```

Example of use (focus on html element when the app loads):
```
const inputRef = useRef<HTMLInputElement | null>(null);

useEffect(() => {
    inputRef.current?.focus();
}, []);

return (
    <div className="tutorial">
        <input ref={inputRef} type="text" placeholder="Type something..." />
    </div>
);
```