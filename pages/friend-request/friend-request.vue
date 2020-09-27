<template>
	<view class="friend-request">
		<view class="request-list">
			<view class="item" v-for="(item, index) in requestDataList" :key="index">
				<view class="user-avatar"><image :src="item.avatarUrl" mode="aspectFill"></image></view>
				<view class="btn-group d-flex justify-content-between align-items-center">
					<view class="btn refuse">拒绝</view>
					<view class="btn agree">同意</view>
				</view>
				<view class="petitioner-name">{{ item.name }}</view>
				<view class="request-time">{{ item.time }}</view>
				<view class="request-message">{{ item.msg }}</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			requestDataList: [
				{
					name: '肥仔松(宝宝)',
					avatarUrl: 'http://ww1.sinaimg.cn/large/73d8d25egy1gj2qc302v3j20u01t0ax7.jpg',
					time: '2020-09-25 11:22',
					msg: '留言：你好，小妹妹，配哥哥玩一玩吧！请求您加我为好友。'
				},
				{
					name: '颓废BB呆哥',
					avatarUrl: 'https://static001.geekbang.org/resource/image/3d/44/3d07bcb16ac1f8725ab27674256bae44.jpg?x-oss-process=image/resize,m_fill,h_168,w_127',
					time: '2020-09-25 11:22',
					msg: '留言：你好，美女，今晚约吗？想请求加为好友！'
				}
			]
		};
	}
};
</script>

<style lang="scss">
.friend-request {
	border-top: 1rpx solid rgba(0, 0, 0, 0.05);
	padding: 20rpx;
	.request-list {
		padding-top: 120rpx;
		.item {
			position: relative;
			background-color: #ffffff;
			border-radius: 20rpx;
			padding: 30rpx;
			margin-bottom: 150rpx;
			box-shadow: 0px 24rpx 64rpx -8rpx rgba(0, 0, 0, 0.1);
			.user-avatar {
				position: absolute;
				left: 50%;
				top: 0;
				transform: translate(-50%, -50%);
				image {
					width: 144rpx;
					height: 144rpx;
					border-radius: 50%;
				}
			}
			.btn-group {
				.btn {
					width: 160rpx;
					line-height: 64rpx;
					text-align: center;
					border-radius: 40rpx;
					font-size: 32rpx;
				}
				.refuse {
					background: rgba(255, 93, 91, 0.1);
					color: #ff5d5b;
				}
				.agree {
					background-color: #ffe431;
					color: #272832;
				}
			}
			.petitioner-name {
				color: #272832;
				font-size: 36rpx;
				font-weight: 500;
				line-height: 50rpx;
				text-align: center;
			}
			.request-time {
				text-align: center;
				font-size: 24rpx;
				font-weight: 400;
				line-height: 34rpx;
				color: rgba(39, 40, 50, 0.4);
			}
			.request-message {
				margin-top: 30rpx;
				padding: 20rpx;
				border-radius: 20rpx;
				background-color: #f3f4f6;
				font-size: 28rpx;
				color: rgba(39, 40, 50, 0.8);
				line-height: 40rpx;
			}
		}
	}
}
</style>
