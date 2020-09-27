<template>
	<view class="header d-flex justify-content-between align-items-center">
		<view class="left"><image src="../../../static/images/xuanyu.jpg" mode="widthFix"></image></view>
		<view class="middle"><image src="../../../static/images/火@2x.png" mode=""></image></view>
		<view class="right">
			<image src="../../../static/images/search@2x.png" mode=""></image>
			<image src="../../../static/images/add_group@2x.png" mode=""></image>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	}
};
</script>

<style lang="scss" scoped>
	.header{
		padding: 0 20rpx;
		box-shadow: 0rpx 2rpx 0rpx 0rpx rgba(0,0,0,0.1);
		.left{
			image{
				width: 68rpx;
				height: 68rpx;
				border-radius: 16rpx;
			}
		}
		.middle{
			image{
				width: 88rpx;
				height: 42rpx;
			}
		}
		.right{
			image{
				width: 52rpx;
				height: 52rpx;
				&:nth-child(2){
					width: 48rpx;
					height: 48rpx;
					margin-left: 20rpx;
				}
			}
			
		}
	}
</style>
