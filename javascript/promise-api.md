# Promise API 列表，粗略解析

- Promise.all(iterable) - 所有的 promise resolved 或者任何的 promise rejected
- Promise.allSettled(iterable) - 所有的状态 settled「resolved 或 rejected」
- Promise.race(iterable) - 任何一个 resolved 或 rejected
- Promise.reject(reason) - reject
- Promise.resolve(value) - resolve
- Promise.prototype.catch() - handle rejected 的错误
- Promise.prototype.then() - handle fullfilled 的值
- Promise.prototype.finally() - callback 没有参数

> `catch`/`then`/`finally` 都是取上一个 `promise` 的状态，后面可以继续接上 `catch`/`then`/`finally`
