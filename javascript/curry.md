# Curry 工具函数实现

```javascript
function curry(fn) {
  let length = fn.length
  return function curriedFn(...args) {
    length -= args.length
    if (length <= 0) {
      return fn.apply(this, args)
    } else {
      return function(...argsE) {
        return curriedFn.apply(this, [...args, ...argsE])
      }
    }
  }
}
const add = (a, b, c, d) => a + b + c + d

const curriedAdd = curry(add)

curriedAdd(1)(2, 3)(4) // 10
```

![curry](https://cdn.jsdelivr.net/gh/mopig/oss@master/uPic/202103/curry.js.png)
