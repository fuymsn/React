# Collection of Reactjs Uncaught Error

## Uncaught Error
Uncaught Error: Invariant Violation: _registerComponent(...): Target container is not a DOM element.
```js
ReactDOM.render(<abc />, document.getElementById("abc"));  //id绑定错误
```

Uncaught Error: React DOM tree root should always have a node reference.
1. 当组件传值丢失时，报此错误
2. 当jsx dom里的变量没有声明时，报此错
```jsx
render(){
	return (
		<div className={ customerClassName }></div> //customerClassName没有定义
	)
}
```

## Uncaught TypeError
Uncaught TypeError: Cannot read property 'map' of undefined
```js
getInitialState: function(){
	return { //原因是这里没有定义 }
}
```

## style属性在jsx中内嵌写法
#### 1. 以不传参的方式：
```js
<img style={{ backgroundImage:"url(http://p1.1room1.co/public/images/vzhubo.jpg)" }} />
```
#### 2. 以传参的方式（字符串拼接）
```js
var urllink = "http://img.x.com/x.jpg";
<img style={{ backgroundImage:"url("+ urllink +")" }} />
```
