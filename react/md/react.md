[###<<返回react列表页](/react/md/react)

[###<<返回首页](/react/index)

### React 是什么？
一个用于构建用户界面的 JavaScript 库
中文手册：https://react.docschina.org/



- React.js 提供 React.js 核心功能代码，如：虚拟 dom，组件
- React.createElement(type,props,children);
- ReactDOM 提供了与浏览器交互的 DOM 功能，如：dom 渲染
- ReactDOM.render(Vnode, container[, callback])
- element：要渲染的内容
- container：要渲染的内容存放容器
- callback：渲染后的回调函数

```html
    <body>
        <div id="root"></div>
    </body>
```

示例：
```jsx
    import React from "react";
    import ReactDOM from "react-dom";

    const App = <div>app</div>;
    ReactDOM.render(App,document.querySelector("#root"))


```
