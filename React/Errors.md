**ERR_OSSL_EVP_UNSUPPORTED** 
```
export NODE_OPTIONS=--openssl-legacy-provider
npm start
```

**ERR_PACKAGE_PATH_NOT_EXPORTED**
Install sass
```
npm install sass
```

Remove the node-sass line from package.json
Example:
```
"node-sass": "^4.0.0"

"node-sass": {
  "optional": true
},
```

Delete the node_modules folter

Reinstall
```
npm install
```

**Blank page when deploying**
In package.json, delete what's in homepage and replace with a dot
```
  "homepage": "."
```