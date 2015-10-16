#Collection of Reactjs Uncaught Error

##Uncaught Error
Uncaught Error: Invariant Violation: _registerComponent(...): Target container is not a DOM element.
```js
ReactDOM.render(<abc />, document.getElementById("abc"));  //id绑定错误
```

##Uncaught TypeError
Uncaught TypeError: Cannot read property 'map' of undefined
```js
getInitialState: function(){
	return { //原因是这里没有定义 }
}
```
