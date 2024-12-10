```
<button onClick={handleClick}>
<button onClick={() => {
    console.log('test');
    handleClick('arg');
}}>
<button onClick={() => handleClick('arg')}>
```

Don't do this:
```
<button onClick={handleClick()}>
```