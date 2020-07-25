# 关于 JS 的类型转换

## `hint` 类型及触发条件

- `string` - `alert` 以及其他需要 `string` 的操作
- `number` - `math` 相关操作
- `default` - 其他少数的操作，如`==`

## 转换算法

- 优先执行 `obj[Symbol.toPrimitive](hint)`
- `Symbol.toPrimitive` 不存在
	- `hint` 为 `string` 执行顺序：`toString` `valueOf`
	- `hint` 为 `number` or `default` 执行顺序：`valueOf` `toString`
