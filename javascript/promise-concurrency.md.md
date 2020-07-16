# Promise 并发执行任务限制

## 代码如下

```javascript
class PromiseSchedule {
  taskQueue = []
  count = 0
  constructor(maxNum) {
    this.maxNum = maxNum
  }
  start() {
    for (let i = 0; i < this.maxNum; i++) {
      this.doNext()
    }
  }
  addTask(task) {
    this.taskQueue.push(task)
  }
  doNext() {
    if (this.taskQueue.length && this.count < this.maxNum) {
      this.count++
      this.taskQueue.shift()().then(() => {
        this.count--
        this.doNext()
      })
    }
  }
}

// test
const sleep = ms => new Promise(res => setTimeout(res, ms))
const schedule = new PromiseSchedule(2)
const addTask = (ms, order) => {
  schedule.addTask(() => sleep(ms).then(() => {console.log(order)}))
}

addTask(1000, 1)
addTask(600, 2)
addTask(500, 3)
addTask(400, 4)

schedule.start()
```
