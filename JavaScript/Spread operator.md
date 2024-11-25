## Spread operator

It's represented by 3 dots ...

Separate the content from an iterable such as an array or string
(Unpacks the elements)

Doesn't work
```
let numbers = [1, 2, 3, 4, 5];

//Doesn't work
let maximum = Math.max(numbers);

//Works
let maximum = Math.max(...numbers);
```

Spread operator "opens a box and takes out all the content that is inside"
