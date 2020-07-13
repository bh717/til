# 括号生成 JS 版递归实现

```javascript
function generateParentheses(n) {
  let ret = []
  brackets(0, 0, n, '', ret)
  return ret
}

function brackets(left, right, n, s = '', ret = []){
  if(left === n && right === n) {
      ret.push(s)
      return
  }
  if(left < n) {
    brackets(left + 1, right, n, s + '(', ret)
  }
  if(left > right) {
    brackets(left, right + 1, n, s + ')', ret)
  }
}
```
