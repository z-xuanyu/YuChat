<template>
	<view class="user-profile">
		<!-- 模糊背景 -->
		<view class="bg"><image class="bg-img" src="http://ww1.sinaimg.cn/large/73d8d25egy1gj2qc302v3j20u01t0ax7.jpg" mode="aspectFill"></image></view>
		<view class="user-avatar">
			<image src="http://ww1.sinaimg.cn/large/73d8d25egy1gj2qc302v3j20u01t0ax7.jpg" mode="aspectFill"></image>
		</view>
		<view class="user-name">
			肥仔松(宝宝)
		</view>
		<view class="user-nick-name">
			昵称：祖安挂机达人
		</view>
		<view class="user-desc">
			夜，结束了一天的喧嚣后安静下来，伴随着远处路灯那微弱的光。风，毫无预兆地席卷整片旷野，撩动人的思绪万千。
		</view>
		<!-- 按钮 -->
		<view class="btn-add">
			加为好友
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

<style lang="scss">
.user-profile {
	width: 100%;
	height: 100%;
	overflow: hidden;
	.bg {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		.bg-img {
			opacity: 0.4;
			position: absolute;
			left: -10rpx;
			top: -10rpx;
			width: 110%;
			height: 110%;
			filter: blur(32rpx);
		}
	}
	.user-avatar{
		margin-top: 80rpx;
		text-align: center;
		image{
			width: 400rpx;
			height: 400rpx;
			border-radius: 48rpx;
			border: 6rpx solid #FFFFFF;
		}
	}
	.user-name{
		margin-top: 20rpx;
		font-size: 52rpx;
		color: #272832;
		line-height: 64rpx;
		text-align: center;
	}
	.user-nick-name{
		margin-top: 5rpx;
		text-align: center;
		font-size: 28rpx;
		line-height: 40rpx;
		color: #272832;
	}
	.user-desc{
		margin-top: 10rpx;
		padding: 0 100rpx;
		text-align: center;
		font-size: 28rpx;
		color: #272832;
		font-weight: 300;
		line-height: 48rpx;
	}
	.btn-add{
		text-align: center;
		position: fixed;
		box-sizing: border-box;
		padding: 15rpx;
		right: 30rpx;
		left: 30rpx;
		bottom: 50rpx;
		background-color: #FFE431;
		border-radius: 10rpx;
		color: #272832;
		font-size: 32rpx;
	}
}
</style>
