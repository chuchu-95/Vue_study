## Vue本地应用
用Vue开发网页效果
获取元素，操纵他们
例如使用v-if等Vue指令

### v-text
设置标签的文本值(textContent)
```html
<div id="app">
	<h2 v-text="message">
	</h2>
</div>
```
```javascript
var app = new Vue({
	el: "#app",
	data: {
		message:""
	}
})
```
**v-text默认替换全部的内容，使用插值表达式可以替换指定的部分
若只需替换一部分数据建议用差值表达式（不会覆盖全部）**


### v-html
设置标签的innerHtml
```html
<div id="app">
</div>
```


### v-xx



### Vue学习路线

 - vue基础
 - vue-cli 脚手架，用于工程化开发 
 - vue-router 用于在vue中实现前端路由
 - vuex 应用足够复杂时借助其帮助保管数据
 - element-ui  好看的ui组件库
  
