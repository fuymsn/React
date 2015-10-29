#Collection of Webpack Error

##Show detail error
if you want to show the detail error, pls run webpack with --display-error-details
```
$ webpack --display-error-details
```

##ERROR in Entry module not found: Error: Cannot resolve 'file' or 'directory'
here are the following cases:
* the incorrect path within Entry

##Module not found: Error: Cannot resolve module 'react/lib/ReactDOM' in sth path
forget to add "." in this resolve block
```js
resolve:{
	extensions: ["", ".js", ".jsx"]
}
```
