<template>
	<view class="navbar">
		<view class="box">
			<view @click="switchPage(0)" :class="{select : currentPage==0,noselect:currentPage!=0}">推荐</view>
			<view @click="switchPage(1)" :class="{select : currentPage==1,noselect:currentPage!=1}">附近</view>
		</view>
		<view class="search-bar">
			<view class="search-box">
				<view class="uni-form-item uni-column search-input">
					<input class="uni-input" confirm-type="search" placeholder="搜索" />
				</view>
				<!-- <image class="icon" src="../../static/logo.png"></image> -->
				<view @click="search" class="search-text">搜索</view>
			</view>
			<image @click="classification" class="icon" src="../../static/icons/classify.png"></image>
		</view>
	</view>
</template>

<script>
	export default {
		name: "homepagetoptab",
		data() {
			return {
				currentPage: 0
			};
		},
		methods: {
			switchPage(page) {
				console.log("test", page)
				this.currentPage = page
				this.$emit('switch', page);
			},
			search() {
				console.log("搜索")
			},
			classification(){
				console.log("进入分类界面")
			}
		}
	}
</script>

<style>
	.search-bar{
		width: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		/* border: 1px solid #000; */
	}
	.search-text {
		background-color: #fae64f;
		width: 120rpx;
		font-size: 30rpx;
		font-weight: 700;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100%;
		padding: 15rpx;
	}

	.icon {
		width: 50rpx;
		height: 50rpx;
		margin: 10rpx;
	}

	.search-input {
		width: 100%;
		padding: 10rpx;
	}

	.search-box {
		/* padding: 6rpx; */
		width: 100%;
		border: 2px solid #fae64f;
		border-radius: 10px;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		overflow: hidden;
	}

	.noselect {
		font-size: 32rpx;
		color: gray;
	}

	.select {
		font-size: 40rpx;
		font-weight: bold;
	}

	.box {
		width: 40%;
		height: 100rpx;
		background-color: #fefefe;
		display: flex;
		align-items: center;
		justify-content: space-evenly;
	}

	.navbar {
		/* padding-left: 5px;
		padding-right: 5px; */
		width: 100%;
		/* height: 230rpx; */
		background-color: #fefefe;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		/* border: 1px solid #000; */
	}

	.title {
		/* border: 1px solid #000; */
		font-size: 20px;
		color: #000;
	}
</style>