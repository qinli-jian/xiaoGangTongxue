<template>
	<view class="custom-tab-bar">
		<view class="tab" v-for="(item, index) in tabs" :key="index" :class="{ active: index === activeTab }"
			@tap="switchTab(index)">
			<view class="box">
				<image :src="index==activeTab? item.selectIcon:item.icon" class="icon"></image>
				<view class="tabtext">
					{{ item.text }}
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "bottomTabBar",
		data() {
			return {

			};
		},

		props: {
			tabs: {
				type: Array,
				default: () => [{
						text: '首页',
						pagePath: '/pages/index/index.vue',
						icon: '/static/tabbar/homepage.png',
						selectIcon: '/static/tabbar/homepageHL.png'
					},
					{
						text: '消息',
						pagePath: '/pages/userMessage/userMessage.vue',
						icon: '/static/tabbar/message.png',
						selectIcon: '/static/tabbar/messageHL.png'
					},
					{
						text: '我的',
						pagePath: '/pages/index/index.vue',
						icon: '/static/tabbar/profile.png',
						selectIcon: '/static/tabbar/messageHL.png'
					},
				],
			},
			activeTab: {
				type: Number,
				default: 0,
			},
		},
		onShow() {
			uni.switchTab({
				url:this.tabs[this.activeTab].pagePath
			})
		},
		methods: {
			switchTab(index) {
				this.$emit('switch', index);
				console.log(index,this.tabs[index].pagePath);
				uni.switchTab({
					url:this.tabs[index].pagePath
				})
			},
		},
	}
</script>

<style>
	.tabtext {
	    font-size: 20rpx;  /* 可以改变这个值来达到你想要的字体大小 */
	}
	.custom-tab-bar {
		display: flex;
		justify-content: space-evenly;
		align-items: center;
		height: 50px;
		/* 修改为你需要的高度 */
		background-color: rgba(240, 239, 239, 1.0); /* 添加半透明背景 */
		/* 更多样式根据需要添加 */
		backdrop-filter: blur(100px);
	}
	.box{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.icon {
		width: 24px;
		height: 24px;
	}

	.tab {
		padding: 10px;
		/* border: 1px solid #000; */
	}

	.tab.active {
		/* color: blue; */
	}
</style>