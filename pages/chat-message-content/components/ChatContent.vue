<template>
	<view class="chat-content-wrapper">
		<scroll-view scroll-y="true" style="height: 100%;" scroll-into-view="scrollId9">
			<block v-for="(item,index) in 10" :key="index">
				<view class="chat-left d-flex" :id="'scrollId'+ item">
					<view class="user-avatar"><image src="../../../static/images/xuanyu.jpg" mode="aspectFill"></image></view>
					<view class="chat-message-text">离别后梦里依稀来到谢家，徘徊在小回廊阑干畔底下。</view>
				</view>
				<view class="chat-right d-flex" :id="'scrollId'+ item">
					<view class="user-avatar"><image src="../../../static/images/xuanyu.jpg" mode="aspectFill"></image></view>
					<view class="chat-message-text">醒来只见庭前多情的明月，它还在临照离人临照落花。</view>
				</view>
			</block>
		</scroll-view>
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
.chat-content-wrapper {
	padding: 20rpx;
	flex: 1;
	border-top: 1rpx solid rgba(0, 0, 0, 0.05);
	overflow: hidden;
	.chat-left {
		margin-top: 40rpx;
		.user-avatar {
			image {
				width: 80rpx;
				height: 80rpx;
				border-radius: 20rpx;
			}
		}
		.chat-message-text {
			width: 450rpx;
			background-color: #ffffff;
			border-radius: 0rpx 20rpx 20rpx 20rpx;
			padding: 20rpx;
			margin-left: 20rpx;
			font-size: 30rpx;
			line-height: 44rpx;
		}
	}
	.chat-right {
		flex-direction: row-reverse;
		margin-top: 40rpx;
		.user-avatar {
			image {
				width: 80rpx;
				height: 80rpx;
				border-radius: 20rpx;
			}
		}
		.chat-message-text {
			width: 450rpx;
			background-color: #ffe431;
			border-radius: 20rpx 0rpx 20rpx 20rpx;
			padding: 20rpx;
			margin-right: 20rpx;
			font-size: 30rpx;
			line-height: 44rpx;
		}
	}
}
</style>
