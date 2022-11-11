# Vue 基础
### Vue 简介
1. Javascript 框架
	必须遵守使用规则
2. 简化Dom操作
	Vue会自动用语法获取Dom元素
3. 响应式数据驱动

### 第一个Vue程序
**3 steps**
官方文档: [https://v2.cn.vuejs.org/v2/guide](https://v2.cn.vuejs.org/v2/guide)
1. 创建文件，引入Vue
	**a.开发环境版本**
	完整版本的jquery 		适合学习，有提示

	**b.生产环境版本**
	min版本的jquery 		速度较快，经过压缩的代码

2. 声明式渲染
```javascript
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

```html
<div id="app">
  {{ message }}
</div>
```

```javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

将message中的值渲染到html中去
data是数据
{{ }}插值表达式，模板的语法
"#"是id选择器，el：“#app” 代表去找id=app的元素

**步骤**

 - 导入开发版本的Vue.js
 - 创建Vue实例对象，设置el属性和data属性
 - s使用简洁的模板语法把数据渲染到页面上
 
### el: 挂载点
1. Vue实例的作用范围
	**在el命中的元素内部都可以渲染**
2. 是否可以选择其他的选择器
	id选择器，类选择器，标签选择器均可
	一般用id选择器因为唯一，其他选择器会造成语义不清晰
```html
class="app" 
el:".app"
```

3. 是否可以设置出了div以外的其他选择器
	**只能支持双标签（建议div），单标签不支持**
	*注意双标签不能挂载到body或html上*

### data: 数据对象
```html
<div id="app">
	{{ message }}
	<h2> {{ school.name }} </h2>
	<ul>
		<li> {{ campus[0] }} </li>
	</ul>
</div>
```

```javascript
data:{
	message:"",
	school:{
		name:"chuchu",
		mobile:""
	},
	campus:["", ""]
}
```
在vue中创建一个school对象，通过调用对象中的属性渲染前端；
获取数组中数据用[]；


