<template>
	<view class="chat-message-content d-flex">
		<!-- 聊天页面导航栏 -->
		<chat-content-navbar></chat-content-navbar>
		<!-- 内容容器 -->
		<chat-content></chat-content>
		<!-- 聊天输入框容器 -->
		<view class="chat-input-box d-flex align-items-center">
			<image src="../../static/images/语音@2x.png" mode="aspectFill"></image>
			<input class="input-msg" type="text" value="聊点什么呢？" @focus="showOtherSend = false" />
			<image src="../../static/images/表情@2x.png" mode="aspectFill"></image>
			<image @click="handleShowOtherSend" src="../../static/images/add_group@2x.png" mode="aspectFill"></image>
		</view>
		<view class="other-send-box d-flex" v-show="showOtherSend">
			<view class="item">
				<view>
					<view class="img-box">
						<image src="../../static/images/照片@2x.png" mode="widthFix"></image>
					</view>
					<view class="text">
						照片
					</view>
				</view>
			</view>
			<view class="item">
				<view>
					<view class="img-box">
						<image src="../../static/images/相机@2x.png" mode="widthFix"></image>
					</view>
					<view class="text">
						拍摄
					</view>
				</view>
			</view>
			<view class="item">
				<view>
					<view class="img-box">
						<image src="../../static/images/定位@2x.png" mode="widthFix"></image>
					</view>
					<view class="text">
						位置
					</view>
				</view>
			</view>
			<view class="item">
				<view>
					<view class="img-box">
						<image src="../../static/images/文件@2x.png" mode="widthFix"></image>
					</view>
					<view class="text">
						视频
					</view>
				</view>
			</view>
			<view class="item">
				<view>
					<view class="img-box">
						<image src="../../static/images/文件@2x.png" mode="widthFix"></image>
					</view>
					<view class="text">
						文件
					</view>
				</view>
			</view>
		</view>
	</view>
</template>s

<script>
import ChatContentNavbar from './components/ChatContentNavbar.vue';
import ChatContent from './components/ChatContent.vue';
export default {
	components: {
		ChatContent,
		ChatContentNavbar
	},
	data() {
		return {
			showOtherSend:false
		};
	},
	methods:{
		// 其他发送
		handleShowOtherSend(){
			this.showOtherSend = true
			uni.pageScrollTo({
				selector:"#scrollId9"
			})
		}
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
		justify-content: space-between;
		flex-wrap: wrap;
		padding-bottom: 30rpx;
		box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.1);
		.item{
			width: 25%;
			margin: 30rpx 0 0;
			display: flex;
			justify-content: center;
			.img-box{
				text-align: center;
				height: 120rpx;
				width: 120rpx;
				background-color: #FFFFFF;
				border-radius: 24rpx;
				display: flex;
				justify-content: center;
				align-items: center;
				image{
					width: 54rpx;
					height: 46rpx;
				}
			}
			.text{
				text-align: center;
				font-size: 24rpx;
				color: #272832;
				line-height: 34rpx;
				 margin-top: 10rpx;
			}
		}
	}
}
</style>
