<template>
	<view class="chat-message-content d-flex">
		<!-- 聊天页面导航栏 -->
		<chat-content-navbar></chat-content-navbar>
		<!-- 内容容器 -->
		<chat-content></chat-content>
		<!-- 聊天输入框容器 -->
		<view class="chat-input-box d-flex align-items-center">
			<image src="../../static/images/语音@2x.png" mode="aspectFill"></image>
			<input class="input-msg" type="text" value="聊点什么呢？" />
			<image src="../../static/images/表情@2x.png" mode="aspectFill"></image>
			<image src="../../static/images/add_group@2x.png" mode="aspectFill"></image>
		</view>
<!-- 		<view class="other-send-box d-flex">
			<view class="item">
				<view class="img-box">
					<image src="../../static/images/照片@2x.png" mode=""></image>
				</view>
				<view class="text">
					照片
				</view>
			</view>
		</view> -->
	</view>
</template>

<script>
import ChatContentNavbar from './components/ChatContentNavbar.vue';
import ChatContent from './components/ChatContent.vue';
export default {
	components: {
		ChatContent,
		ChatContentNavbar
	},
	data() {
		return {};
	}
};
</script>

<style lang="scss">
.chat-message-content {
	height: 100vh;
	background: #f4f4f4;
	flex-direction: column;
	justify-content: space-between;
	.chat-input-box {
		padding: 30rpx 20rpx 10rpx;
		border-top: 1rpx solid rgba(0, 0, 0, 0.05);
		image {
			width: 56rpx;
			height: 56rpx;
			&:nth-last-child(1) {
				margin-left: 10rpx;
			}
		}
		.input-msg {
			margin: 0 20rpx;
			padding-left: 10rpx;
			flex: 1;
			background-color: #ffffff;
			border-radius: 10rpx;
			height: 72rpx;
		}
	}
	.other-send-box {
		width: 100%;
		background: #ecedee;
		justify-content: space-around;
		box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.1);
		.item{
			width: 25%;
			.img-box{
				width: 120rpx;
				line-height: 120rpx;
				background-color: #FFFFFF;
				border-radius: 24rpx;
				image{
					width: 54rpx;
					height: 46rpx;
				}
			}
			.text{
				font-size: 24rpx;
				color: #272832;
			}
		}
	}
}
</style>
