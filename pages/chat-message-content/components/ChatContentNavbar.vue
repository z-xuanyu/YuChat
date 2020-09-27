<template>
	<view class="chat-content-navbar d-flex justify-content-between align-items-center">
		<view class="left">
			<image src="../../../static/images/left.png" mode="widthFix"></image>
		</view>
		<view class="middle">
			榆木脑袋
		</view>
		<view class="right">
			<image src="../../../static/images/xuanyu.jpg" mode="widthFix"></image>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				
			}
		}
	}
</script>

<style lang="scss" scoped>
	.chat-content-navbar{
		padding:10rpx 20rpx;
		.left{
			image{
				width: 50rpx;
				height: 50rpx;
			}
		}
		.right{
			image{
				width: 68rpx;
				height: 68rpx;
				border-radius: 16rpx;
			}
		}
	}
</style>
