<template>
	<view class="box">
		<image mode="aspectFill" class="goodsImage" :style="'width:'+100+'%;'" :src="goodsObject.imageUrl">
		</image>
		<view class="goods-describe">{{truncateText(20,goodsObject.goodsDescription)}}</view>
		<view class="goods-price">
			<view class="rmb-icon">￥</view>{{goodsObject.goodsPrice}}
		</view>
		<view class="seller-box">
			<image mode="aspectFill" class="head-icon" :src="goodsObject.user.profilePhoto" />
			<view class="seller-name">{{truncateText(6,goodsObject.user.user_name)}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "goodsCard",
		props: {
			goodsObject: Object
		},
		data() {
			return {
				boxwidth: 0
			};
		},
		mounted() {
			let _this = this;
			this.$nextTick(() => {
				var query = uni.createSelectorQuery().in(this);
				query.select('.box').boundingClientRect(data => {
					// console.log(data.width);
					_this.boxwidth = data.width;
					console.log("===", _this.boxwidth)
				}).exec();
			});
		},
		methods: {
			truncateText(maxLength, text) {
				if (text.length > maxLength) {
					return text.substring(0, maxLength) + '...';
				} else {
					return text;
				}
			}
		}
	}
</script>

<style>
	.rmb-icon{
		/* border: 1px solid #000; */
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 15rpx;
	}
	.seller-name {
		/* border: 1px solid #000; */
		height: 100%;
		margin-left: 10rpx;
		width: 60%;
		font-size: 20rpx;
		color: gray;
		display: flex;
		align-items: center;

		white-space: nowrap;
		box-sizing: border-box;
	}

	.head-icon {
		border-radius: 50%;
		height: 50rpx;
		width: 50rpx;
	}

	.seller-box {
		width: 100%;
		height: 10%;
		display: flex;
		flex-direction: row;

	}

	.goods-price {
		margin-bottom: 10rpx;
		/* border: 1px solid #000; */
		display: flex;
		flex-direction: row;
		width: 100%;
		/* height: 50rpx; */
		font-weight: 600;
		color: #EB5428;
	}

	.goods-describe {
		/* border: 1px solid #000; */
		flex: 1;
		box-sizing: border-box;
		padding: 5rpx;
		display: flex;
		justify-content: left;
		width: 100%;
		box-sizing: border-box;
		font-size: 30rpx;
	}

	.box {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

	}

	.goodsImage {
		/* border: 1px solid #000; */
		/* width: 100% !important; */
		max-height: 350rpx;
		/* overflow: hidden; */
		/* border: 2px solid red; */
		border-radius: 20rpx;
		box-sizing: border-box;
	}

	.box {
		width: 100%;
		height: 100%;
		/* border: 2px solid red; */
		box-sizing: border-box;
		display: flex;

	}
</style>