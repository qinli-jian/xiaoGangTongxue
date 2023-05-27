<template>
	<view class="optionsBarBox">
		<view class="box-row" v-for="(item_list,index1) in list" :key="index1" >
			<view v-for="(item,index2) in item_list" :key="index2" class="row-item" style="width:20%;border: 0px solid #000;">
				<image class="option-icon" :src="item.itemIcon"></image>
				<view class="option-text">{{ item.itemName }}</view>
			</view>
		</view>

		<!-- <view style="width:33%;border: 1px solid #000;">hi</view> -->
	</view>
</template>

<script>
	export default {
		name: "homePageOptionsBar",
		data() {
			return {
				list:[
					[
						{
							itemName:"驾校",
							itemIcon:"../../static/icons/driving-school.png"
						},
						{
							itemName:"二手交易",
							itemIcon:"../../static/icons/second-hand.png"
						},
						{
							itemName:"帖子",
							itemIcon:"../../static/icons/tiezi.png"
						},
						{
							itemName:"就业",
							itemIcon:"../../static/icons/get-a-job.png"
						},
						{
							itemName:"兼职",
							itemIcon:"../../static/icons/part-time-job.png"
						},
					]
				]
			};
		}
	}
</script>

<style>
	.option-text{
		font-size: 20rpx;
	}
	.option-icon{
		width: 60rpx;
		height: 60rpx;
		margin-bottom: 10rpx;
	}
	.row-item{
		padding-top: 10rpx;
		padding-bottom: 10rpx;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.box-row{
		display: flex;
		flex-direction: row;
	}
	.optionsBarBox {
		margin-top: 40rpx;
		width: 100%;
		border: 0px solid #000;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
	}
</style>