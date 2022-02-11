<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<comA></comA>
		<comB></comB>
		<view>全局过滤器：{{30.21|new_price}}</view>
		<navigator url="/pages/index/B">
			跳转
		</navigator>
		<u-button type="primary">zhou</u-button>
		地址：{{this.$mConfig.hostUrl}}
	</view>
</template>

<script>
	import comA from "@/components/new_file.vue"
	import comB from "./B.vue"
	export default {
		components:{
			comA,comB
		},
		data() {
			return {
				title: 'Hello',
			}
		},
		onLoad() {
			this.title=process.env.NODE_ENV;
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
