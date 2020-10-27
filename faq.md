### ✍️ Tangxt ⏳ 2020-10-27 🏷️ faq

# FAQ

## ★ 1~10

1）关于 React 和 ReactDOM？

必须同时使用这两个库才能在浏览器上开发 React 应用

总之，只使用其中任何一个都不能在浏览器上开发 React 应用

2）如何理解 `const x = React.createElement('div', null, 'hi') `？

`x` 是一个 React 元素，它代表一个 `div`，它是一个虚拟 DOM 对象

注意，`x`可不是一个 DOM 对象哈！

3）有如下三个代码片段，请问，能够在 `n` 为偶数时显示「n 是偶数」，`n` 为奇数是显示「n 是奇数」的是 A、B、C 中的哪一个？

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

4）点加1后，数字会加1？

代码：[Demo](https://codesandbox.io/s/twilight-sun-iogjz)

