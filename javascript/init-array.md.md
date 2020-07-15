# 初始化指定长度的 Array

## 下面四种方法可以解决

```javascript
// 方法一
Array.apply(null, Array(7))

// 方法二
Array(10).fill(0)

// 方法三
Array.from({length: 10}, (v, i) => i)

// 方法四
[...Array(10).map((v, i) => i)]
```
