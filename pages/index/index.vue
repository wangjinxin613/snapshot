<template>
	<view class="content">
		<view class="search">
			<icon type="search" size="14" />
			<input type="text" placeholder="搜索" />
		</view>
		<view class="swiper">
			<swiper class="swiper" :indicator-dots="true" indicator-active-color="#ADD8E6" :autoplay="true"
				:interval="5000">
				<swiper-item v-for="(item, index) in banner" :key="index">
					<view class="swiper-item">
						<image :src="item" mode="widthFix" />
					</view>
				</swiper-item>
			</swiper>
		</view>
		<view class="nav-list">
			<view class="single" v-for="(item,index) in dataList" :key="index">{{ item.nav }}</view>
		</view>
		<view class="index-view">
			<swiper class="index-view-swiper">
				<swiper-item v-for="(item, index) in dataList" :key="index">
					<view class="content-view">
						<view class="single" v-for="item in 10">
							<view class="user-info">
								<view class="logo">
									<image src="../../static/logo.png" alt="logo"/>
								</view>
								<view class="nick-view">
									<view class="nick-name">小王是最帅的</view>
									<view class="age">1小时前</view>
								</view>
								<button class="focus-btn">关 注</button>
							</view>
							<view class="content-text">
								这是一段九宫格文字描述
							</view>
							<view class="imgs one">
								<image src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fcdn.duitang.com%2Fuploads%2Fblog%2F201404%2F25%2F20140425123452_HZLNs.thumb.600_0.jpeg&refer=http%3A%2F%2Fcdn.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1630739718&t=589b1afb8fb400ef18e7429b2d3397c8" mode="heightFix"/>
							</view>
							<view class="tool-view">
								<view class="symbol active" >
									<jinIcon type="&#xe673;" class="icon"></jinIcon>
									<text>99</text>
								</view>
								<view class="symbol" >
									<jinIcon type="&#xe668;" class="icon"></jinIcon>
									<text>踩</text>
								</view>
								<view class="symbol" >
									<jinIcon type="&#xe66b;" class="icon"></jinIcon>
									<text>评论</text>
								</view>
								<view class="symbol" >
									<jinIcon type="&#xe66f;" class="icon"></jinIcon>
									<text>收藏</text>
								</view>
							</view>
						</view>
					</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
import jinIcon from '@/components/jin-icons/jin-icons.vue';
	
	export default {
		components: {
			jinIcon
		},
		data() {
			return {
				title: 'Hello',
				banner: [
					'https://pic1.zhimg.com/v2-7686f94d95e25bee9114cf6731a334b8_r.jpg?source=172ae18b',
					'https://img.zcool.cn/community/01b70e5b42d5c3a80121b9946f3e04.jpg@1280w_1l_2o_100sh.jpg'
				],
				// 推荐, 最新, 关注的数据
				dataList: [
					{
						nav: '推荐',
					},
					{
						nav: '最新',
					},
					{
						nav: '关注',
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="less" scoped>
@import './index.less';
</style>
