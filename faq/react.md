### ✍️ Tangxt ⏳ 2020-10-27 🏷️ faq

# React-Question

## ★必须要记住的

- 关于`class`组件，不能在 `render()` 中修改组件状态，总之，`render`方法必须是纯的而且没有副作用 -> `render`其实也是一个生命周期方法！

## ★ 1~10

### <mark>1）关于 React 和 ReactDOM？</mark>

必须同时使用这两个库才能在浏览器上开发 React 应用

总之，只使用其中任何一个都不能在浏览器上开发 React 应用

### <mark>2）如何理解 `const x = React.createElement('div', null, 'hi') `？</mark>

`x` 是一个 React 元素，它代表一个 `div`，它是一个虚拟 DOM 对象

注意，`x`可不是一个 DOM 对象哈！

### <mark>3）有如下三个代码片段，请问，能够在 `n` 为偶数时显示「n 是偶数」，`n` 为奇数是显示「n 是奇数」的是 A、B、C 中的哪一个？</mark>

``` jsx
// 片段 A
let n = 0
const Component = () => {
  return 
    <div>
      { n%2===0 ? <div>n 是偶数</div> : <span>n 是奇数</span> }
    </div>
}
```

注意片段 A 的 `return` 后面没有括号

``` jsx
// 片段 B
let n = 0
const Component = () => {
  return (
    <div>
      n%2===0 ? <div>n 是偶数</div> : <span>n 是奇数</span>
    </div>
  )
}
```

注意片段 B 的 `n%2` 前面没有 `{`

``` jsx
// 片段 C
let n = 0
const Component = () => {
  return (
    <div>
      { n%2===0 ? <div>n 是偶数</div> : <span>n 是奇数</span> }
    </div>
  )
}
```

片段 C 是正确的！

### <mark>4）点加 1 后，数字会加 1？</mark>

代码：[Demo](https://codesandbox.io/s/twilight-sun-iogjz)

### <mark>5）如何使用 parcel 搭建 React 应用？</mark>

![react 应用](assets/img/2020-12-26-14-38-03.png)

代码：[Demo](https://github.com/ppambler/react-demo/commit/76817a1d2bb5be4244015353e56de0b6f1ffdde1)

➹：[How To Set Up a React Project With Parcel - DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-react-project-with-parcel)

### <mark>6）Bulma ？</mark>

一个 CSS 框架，做一些代码测试时，可以用它提供的样式去搞！

使用：

``` html
<link href="https://cdn.bootcdn.net/ajax/libs/bulma/0.9.1/css/bulma.min.css" rel="stylesheet">
```

➹：[Documentation - Bulma: Free, open source, and modern CSS framework based on Flexbox](https://bulma.io/documentation/)

➹：[CSS 框架 Bulma 教程 - 阮一峰的网络日志](http://www.ruanyifeng.com/blog/2017/10/bulma.html)

### <mark>7）React vs Vue？</mark>

- Vue：自动挡，坏了很难修，构造复杂但使用简单
- React：手动挡（半自动挡），坏了很容易修，使用较 Vue 复杂但构造简单

总之，使用 Vue，就是在让开发者放弃 JS 的编程序和灵活性，而且面试官考察 Vue 大部分都认为问不出你到底是个什么样的水平，而问 React，则可以考察出你对 JS 底层的掌握能力！

> 电锯 vs 类似斧头一样的电锯

### <mark>8）感觉 React 上手比 Vue 要简单？</mark>

任何库都要在「概念简洁」（自由度高）和「使用便利」（提供现成的范式）上做选择。React 选择了前者，Vue 选择了后者。

不可能有一个库能同时做到两者。即使做到了两者，你也会发现使用的人分成两拨，两拨人互相看不惯。

如果你一定要问他俩孰优孰劣，可能没有答案。

> Webpack vs Parcel

➹：[Vue真的比React上手简单吗? - 方应杭的回答 - 知乎](https://www.zhihu.com/question/271908748/answer/364203091)

### <mark>9）JSX 里边不能用`Object`类型的值（`{}`）？</mark>

![不能用普通对象](assets/img/2021-01-13-17-42-54.png)

10）React 组件的状态？

➹：[深入理解React的组件状态](https://juejin.cn/post/6844903624603090952)

## ★11~20

11）在 VS Code 里边写 JSX 代码，如何生成提示？

![jsx 提示](assets/img/2021-02-10-21-10-25.png)

配置了这个，就能愉快地写 JSX 代码了！

12）如何透过`ref`属性获取一个元素？

![ref](assets/img/2021-03-13-02-01-55.png)

