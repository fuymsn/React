# Collection of Webpack Error

### Show detail error
if you want to show the detail error, pls run webpack with --display-error-details
```
$ webpack --display-error-details
```

### ERROR in Entry module not found: Error: Cannot resolve 'file' or 'directory'
here are the following cases:
* the incorrect path within Entry

### Module not found: Error: Cannot resolve module 'react/lib/ReactDOM' in sth path
* forget to add "." in this resolve block
```js
resolve:{
	extensions: ["", ".js", ".jsx"]
}
```
* error path in entry block

### Uncaught TypeError: Cannot read property 'call' of undefined
如果错误出现在如下代码中：
```js
modules[moduleId].call(module.exports, module, module.exports, __webpack_require__); 
```
有可能是如下原因引起：
*  commonsPlugin中的common.js写成了common
*  It can be caused by having a commons chunk (which will include the runtime) and an entry point that the commons chunk didn't reference, and thus includes the runtime itself.

> [参考] https://github.com/webpack/webpack/issues/1081
