# cc-serviceDialog 自定义服务说明弹窗 自下而上 底部弹窗

 # 


#### 使用方法

```使用方法

		
<!-- 服务组件弹窗 close:关闭事件 class:定义类(显示或隐藏)  -->
		
<cc-serviceDialog @close="closeService" class="hidden" :class="{show:serviceFlag}"></cc-serviceDialog>
		

```

#### HTML代码实现部分
```html

<template>
	<view class="content">

		<!-- 服务组件弹窗 close:关闭事件 class:定义类(显示或隐藏)  -->
		<cc-serviceDialog @close="closeService" class="hidden" :class="{show:serviceFlag}"></cc-serviceDialog>
		
		
		<button @click="showSerivicClick" style="margin-top: 60px; width: 190px;">显示服务说明弹窗</button>




	</view>
</template>

<script>

	export default {
		
		data() {
			return {

				serviceFlag: false,

			}
		},
		
		methods: {

			closeService() {
				this.serviceFlag = false
			},
			showSerivicClick() {

				this.serviceFlag = true;
			},


		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;

	}

	.hidden {
		display: none;
	}

	.show {
		display: block;
	}
</style>





```
