# Vue 的优化技巧

## Components 全局导入

```javascript
// allImport.js，入口文件中引入此文件
import Vue from 'vue'

function capitalizeFirstLetter(string) {
  // 此函数用途是首字符大写，baseInput->BaseInput 如果是已经首字符大写的文件名，不需要
  return string.charAt(0).toUpperCase() + string.slice(1)
}

function handleFileName(string) {
  // 把形如 ./fileName.vue -> fileName
  return string.replace(/^\.\//, '').replace(/\.\w+&/, '')
}

const requireComponent = require.context('.', false, /\.vue$/)
// 表示找到此文件夹下所有.vue为后缀的文件，详见webpack require.context文档

requireComponent.keys().forEach(fileName => { // fileName可以认为是路径字符串
  const componentConfig = requireComponent(fileName)
  const componentName = capitalizeFirstLetter(handleFileName(fileName))
  Vue.component(componentName, componentConfig.default || componentConfig)
})
```
