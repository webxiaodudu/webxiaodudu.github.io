[<<返回react列表页](/react/index)

[<<返回首页](/index)


### 插值表达式
在 JXS 中可以使用 {表达式} 嵌入表达式



1. 字符串、数字：原样输出

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

2. 数组去掉逗号号，直接输出

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


3. 不支持对象的直接输出


4. jsx中属性class和style, jsx中的属性class要用className,style接收一个样式对象

className:

```jsx

    ReactDOM.render(
        <div className="red">{'className不是class'}</div>,
        document.getElementById('root')
    );

```
输出：

```html
<div class="red">className不是class</div>

```

style对象:

```jsx
    const style = {
  width:'100px',
  height:'100px',
  background:'blue'
}

ReactDOM.render(
  <div style={style}></div>,
  document.getElementById('root')
);

```
输出:

```html
    <div style="width: 100px; height: 100px; background: blue;"></div>
```

5. 条件渲染

```jsx
import { Component } from "react";

class App extends Component {
  state = {
    flag:false
  }
  render(){
    const { flag } = this.state
     
    return <div>
        { flag ? <h1>aaa</h1> : <h1>bbb</h1> }
      </div>
    
  }
} 

export default App;

```

输出：

```html

<div id="root"><div><h1>bbb</h1></div></div>

```


6. Fragment组件

Fragment 文档碎片，作为包含容器存在，并不会渲染到真实DOM中

```jsx

import { Fragment } from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(
  <Fragment>
    <div>1</div>
    <div>2</div>
  </Fragment>,
  document.getElementById('root')
);


```

输出:

```html

<div id="root">
    <div>1</div>
    <div>2</div>
</div>

```