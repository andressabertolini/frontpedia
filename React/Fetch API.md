```
const api = {
  key: "abcde12345",
  base: "https://apiurl.api/data/1.0/"
}

fetch(`${api.base}?q=${string}&id=12345&appid=${api.key}`)
    .then(res => res.json())
    .then(result => {
        setWeather(result);  
        console.log(result);
    }
)
```

