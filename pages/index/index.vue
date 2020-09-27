<template>
	<view class="index">
		<!-- 主页头部 -->
		<index-header></index-header>
		<!-- 聊天信息列表 -->
		<chat-message-list></chat-message-list>
	</view>
</template>

<script>
	import IndexHeader from './components/IndexHeader.vue'
	import ChatMessageList from './components/ChatMessageList.vue'
	export default {
		components:{
			IndexHeader,
			ChatMessageList
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>

</style>
