<template>
	<view class="content">
		<homepagetoptab @switch="switchPage"></homepagetoptab>
		<swiper class="swiper" :current="currentPage" @change="handleChange">
			<swiper-item style="box-sizing: border-box;">
				<homePageOptionsBar></homePageOptionsBar>
				<scroll-view class="scroll-v" scroll-y="true">
					<cardContentBox></cardContentBox>
				</scroll-view>
			</swiper-item>
			<swiper-item>第二页的内容</swiper-item>
		</swiper>
		<!-- <bottomTabBar :activeTab="activeTab" @switch="switchTab"></bottomTabBar> -->
		<view style="height: 50px;" </view>
</template>

<script>
	// import bottomTabBar from '@/components/bottomTabBar/bottomTabBar.vue'
	import homePageOptionsBar from '@/components/homePageOptionsBar/homePageOptionsBar.vue'
	import homepagetoptab from '@/components/homepagetoptab/homepagetoptab.vue'
	import cardContentBox from '@/components/cardContentBox/cardContentBox.vue'
	export default {
		components: {
			homepagetoptab,
			homePageOptionsBar,
			cardContentBox
		},
		data() {
			return {
				title: 'Hello',
				currentPage: 0,
				tabBarHeight: 0, 
				// activeTab: 0,
			}
		},
		onLoad() {
			const systemInfo = uni.getSystemInfoSync();
			this.tabBarHeight = 50;
			console.log("安全区", this.tabBarHeight)
		},
		methods: {
			switchPage(page) {
				console.log("test", page)
				this.currentPage = page;
				console.log("this.currentPage", this.currentPage)
			},

			handleChange(event) {
				this.currentPage = event.detail.current;
				console.log("this.currentPage", this.currentPage)
			},

			// switchTab(index) {
			// 	this.activeTab = index;
			// 	// 这里你可以根据 tab 的索引来切换页面内容
			// },
		}
	}
</script>

<style>
	/* 下面这样才在浏览器中实现滚动条的隐藏 */
	/deep/.scroll-v ::-webkit-scrollbar {
		display: none;
		width: 0 !important;
		height: 0 !important;
		-webkit-appearance: none;
		background: transparent;
		color: transparent;
	}

	.scroll-v {
		/* overflow-y: scroll; */
		height: 100%;
	}

	.swiper {
		/* border: 1px solid #000; */
		flex: 1;
		/* padding-bottom: 10rpx; */
		/* 或者你需要的高度 */
		box-sizing: border-box;
	}

	.content {
		overflow: hidden;
		margin-bottom: 1px;
		/* border: 1px solid #000; */
		padding-left: 20rpx;
		padding-right: 20rpx;
		padding-top: 20rpx;
		display: flex;
		flex-direction: column;
		justify-content: center;
		/* align-items: center; */
		width: 100%;
		/* 
		height: 100%; */
		/* vh 是 viewport height 的简写，代表视口高度。1vh 等于视口高度的1% */
		position: absolute;
		/* 使用绝对定位可以使元素脱离文档流，占满整个父元素 */
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		box-sizing: border-box;
		/* 记笔记，要加入无限笔记*/
		/* overflow: hidden; */
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>