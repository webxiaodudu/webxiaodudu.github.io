[<<返回react列表页](/react/index)

[<<返回首页](/index)


### 插值表达式
在 JXS 中可以使用 {表达式} 嵌入表达式



* 字符串、数字：原样输出

```jsx
ReactDOM.render(
  <h1>{'这是纯文本'}</h1>,
  document.getElementById('root')
);

```

输出：

```html
这是纯文本
```

* 数组去掉逗号号，直接输出

```jsx
const arr=[<li>React</li>,<li>Vue</li>,<li>Typescript</li>]

ReactDOM.render(
  <ul>{arr}</ul>,
  document.getElementById('root')
);

```

输出：

```html

<ul>
    <li>React</li>
    <li>Vue</li>
    <li>Typescript</li>
</ul>

```


* 不支持对象的直接输出