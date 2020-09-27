<template>
	<view class="chat-message-list">
		<view class="container">
			<view class="msg-item d-flex" v-for="(item,index) in msgListData" :key="index" @click="goMessageContent">
				<view class="user-avatar">
					<image :src="item.avatarUrl" mode="aspectFill"></image>
					<text>{{item.msgNum}}</text>
				</view>
				<view class="msg-info">
					<view class="msg-title d-flex justify-content-between align-items-center">
						<view class="name">{{item.name}}</view>
						<view class="time">{{item.msgTime}}</view>
					</view>
					<view class="msg-text">{{item.msgText}}</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			msgListData:[
				{
					name:"肥仔松",
					avatarUrl:"https://static001.geekbang.org/resource/image/e6/39/e617d8532447343993eb8ff4f2991139.jpg",
					msgText:"达钦是要腿，还是要狗尾，怎么跟我达钦说话的呢",
					msgTime:'上午7:45',
					msgNum:'9'
				},
				{
					name:"钦管严",
					avatarUrl:"https://static001.geekbang.org/resource/image/50/b6/50cac4f8a8e9b600636c0890967113b6.jpg?x-oss-process=image/resize,m_fill,h_36,w_36",
					msgText:"你在嘲讽何总没妹子？",
					msgTime:'上午10:15',
					msgNum:'3'
				},{
					name:"肥仔松",
					avatarUrl:"https://static001.geekbang.org/resource/image/e6/39/e617d8532447343993eb8ff4f2991139.jpg",
					msgText:"达钦是要腿，还是要狗尾，怎么跟我达钦说话的呢",
					msgTime:'上午7:45',
					msgNum:'9'
				},{
					name:"何总",
					avatarUrl:"https://static001.geekbang.org/resource/image/15/be/1538be68a5f597ab1baf179a4a724ebe.jpg?x-oss-process=image/resize,m_fill,h_36,w_36",
					msgText:"我是怕呆呆一个人在宿舍无聊，所以申请了在宿舍办公",
					msgTime:'10:25',
					msgNum:'13'
				},{
					name:"呆哥",
					avatarUrl:"https://static001.geekbang.org/resource/image/3d/44/3d07bcb16ac1f8725ab27674256bae44.jpg?x-oss-process=image/resize,m_fill,h_168,w_127",
					msgText:"小孩子不要问这些",
					msgTime:'11:45',
					msgNum:'99'
				}
			]
		};
	},
	methods:{
		goMessageContent(){
			console.log("sdsds")
			uni.navigateTo({
				url: '/pages/chat-message-content/chat-message-content'
			});
		}
	}
};
</script>

<style lang="scss" scoped>
.chat-message-list {
	background-color: #ffffff;
	box-sizing: border-box;
	.container {
		margin-top: 20rpx;
		.msg-item {
			padding: 0 20rpx;
			height: 128rpx;
			.user-avatar {
				position: relative;
				image {
					width: 96rpx;
					height: 96rpx;
					border-radius: 24rpx;
				}
				text {
					position: absolute;
					top: -10rpx;
					right: -10rpx;
					width: 30rpx;
					text-align: center;
					height: 30rpx;
					border-radius: 36rpx;
					color: #ffffff;
					font-size: 24rpx;
					padding: 5rpx;

					background-color: $y-color-error;
				}
			}
			.msg-info {
				margin-left: 20rpx;
				overflow: hidden;
				flex: 1;
				.msg-title {
					.name {
						margin-left: 20prx;
						font-size: 36rpx;
						color: #272832;
						line-height: 50rpx;
						font-weight: 400;
						font-family: PingFangSC-Regular, PingFang SC;
					}
					.time {
						color: rgba(39, 40, 50, 0.4);
						font-size: 24rpx;
						line-height: 34rpx;
					}
				}

				.msg-text {
					font-size: 28rpx;
					color: rgba(39, 40, 50, 0.6);
					line-height: 40rpx;
					@include text-ellipsis-1;
				}
			}
		}
	}
}
</style>
