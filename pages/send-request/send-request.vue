<template>
	<view class="send-request">
		<view class="bg"><view class="bg-img"></view></view>
		好友请求
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
.send-request {
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
			background-color: #ffe431;
			filter: blur(32rpx);
		}
	}
}
</style>
