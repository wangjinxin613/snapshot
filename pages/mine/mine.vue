<template>
	<view>
		<view class="head-img">
			<image mode="aspectFill"
				src="https://bjetxgzv.cdn.bspapp.com/VKCEYUGU-uni-app-doc/6acec660-4f31-11eb-a16f-5b3e54966275.jpg">
			</image>
		</view>
		<view class="user-info-view">
			<view class="nick-view">
				<view class="username">小王</view>
				<jinIcon type="&#xe632;" class="icon"></jinIcon>
			</view>
			<view class="introduction">这里是个性签名</view>
		</view>
		<view class="under-info-view">
			<view class="under-view"> 
				<view class="undername">我的喜欢</view>
				<jin-icon type="&#xe66f;" class="icon"></jin-icon>
			</view>
			<view class="under-view">
				<view class="undername">设置</view>
				<jin-icon type="&#xe67f;" class="icon"></jin-icon>
			</view>
			<view class="under-view">
				<view class="undername">联系我们</view>
				<jin-icon type="&#xe681;" class="icon"></jin-icon>
			</view>
		</view>
	</view>
</template>

<script>
	import jinIcon from '@/components/jin-icons/jin-icons.vue';
	export default {
		components:{
			jinIcon: jinIcon
		},
		data() {
			return {}
		},
		methods: {

		}
	}
</script>

<style lang="less" scoped>
	@import url("./mine.less");
</style>
