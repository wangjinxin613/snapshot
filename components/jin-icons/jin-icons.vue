<template>
	<view v-html="type" :class="['jin-icon', className]" @click="toclick"></view>
</template>

<script>
	export default {
		props: {
			type: {
				type: String,
				default: '&#xe644;'
			},
			className: {
				type: String
			}
		},
		methods: {
			toclick() {
				this.$emit('click');
			}
		}
	}
</script>

<style scoped>
	@font-face {
		font-family: 'jin';
		/** 阿里巴巴矢量图标库的字体库地址，可以替换自己的字体库地址 **/
		src: url('https://at.alicdn.com/t/font_2724148_qjf2vq30w3q.ttf?t=1628326967030') format('truetype');
	}

	.jin-icon {
		font-family: jin !important;
		font-size: 34rpx;
	}

</style>
