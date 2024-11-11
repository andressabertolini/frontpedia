## UseEffect Hook

A hook is a function that return JS variants and handle state.

UseEffect is a hook that is used to perform side effects in our application.

Side effects - when something happens, something else happens as consequence.

In most aplications, side effects are going to be a result of state changing.

You have some state in your application, it goes from one value to another and that causes a side effect to happen that you can control.

```
import { useEffect } from 'react';

useEffect(() => {}, []);
```

{} is the code to run 
[] dependency array where you tell useEffect what it should react to 
```
useEffect(() => {
    //Code to run

    //optional return function (cleanup)
}, [//dependency array]);
```

useEfect runs at least one time when it mount

Example of use:
```
useEffect(() => {
    console.log('Count:', count);

    return () => {
        console.log('I am being cleaned up');
    }
}, [count]);
```

"This useEffect is hooked to the count"

The cleanup function will run before the function