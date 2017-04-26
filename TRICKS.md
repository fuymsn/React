# React 小技巧

## className 拼接
使用数组拼接代替字符串拼接。

**Deprecate**
```jsx
render() {
    return (
        <div className={ style1 + " " + style2 } ></div>
    )
}
```
**Recomend**
```jsx
let classes = [style1];
classes.push(style2);

render() {
    return (
        <div className={ classes.join(" ") } ></div>
    )
}
```
