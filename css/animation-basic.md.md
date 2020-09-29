# animation 基本使用

## 基本属性

```css
@keyframes fade-in { /* 关键帧名字 */
	from { /* 等效于 0% */
		background-color: red;
	}
	50% {
		background-color: orange;
	}
	to { /* 等效于 */
		background-color: yellow;
	}
}

.animation-class {
	/*<single-animation> = <time>  ||  <timing-function>  ||  <time>  ||  <single-animation-iteration-count>  ||  <single-animation-direction>  ||  <single-animation-fill-mode>  ||  <single-animation-play-state>  ||  [ none |  <keyframes-name>  ]*/
	animation: 3s ease-out 500ms infinite alternate both running fade-in;
}
/* 和上边等效 */
.animation-class-2 {
	animation-name: fade-in; /* 关键帧名字 */
	animation-duration:  3s; /* 动画时长 */
	animation-timing-function: ease-out; /* 动画的时间函数 */
	animation-delay:  500ms; /* 动画延迟执行时间 */
	animation-direction: alternate; /* 动画方向 normal: 0% => 100% */
	animation-iteration-count: infinite; /* 动画执行次数 */
	animation-fill-mode: both; /* 执行前后的样式 */
	animation-play-state: running; /* 控制运行和暂停 */
}
``` 
