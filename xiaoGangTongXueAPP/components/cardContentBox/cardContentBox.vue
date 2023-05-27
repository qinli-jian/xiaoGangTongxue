<template>
	<view>
		<view class="box">
			<view v-for="(goodsObject,index) in goodsObjects" :key="index" class="card" :style="'height:'+ (500-(index==0)*30)+'rpx'">
				<goodsCard v-bind:goodsObject="goodsObject"></goodsCard>
			</view>
		</view>
		<view style="height: 90px;border:0px solid #000"></view>
	</view>
</template>

<script>
	import goodsCard from '@/components/goodsCard/goodsCard.vue'
	export default {
		components:{
			goodsCard
		},
		name: "cardContentBox",
		data() {
			return {
				goodsObjects: [
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods1.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods2.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
					{
						imageUrl:'/static/images/testgoods.png',
						goodsDescription:"重庆观音桥手机置换 手机回收问价不亏。#手机 #Apple/苹果 回收苹果14 苹果13 苹果13pro 14promax苹果12 苹果11（iPhone,iPad）华为，小米，三星，OPPO，vivo，各大品牌手机 手机进水，屏幕更换，电池更换，内存升级（苹果），解锁刷机，信号差，死机重启，触摸失灵，显示异常，后壳(玻璃）更换，听筒无声，不送话，按键失灵， 主板精修（不开机，不照相，无服务，无WiFi，无声音，不充电，无触摸，短路，漏电，触摸不灵） #双11闲置急出 当然我们能做的还有更多～～欢迎咨询",
						goodsPrice:455.8,
						priceUnit:"RMB",
						originalPrice:"900",
						spot:"重庆交通大学",
						user:{
							user_id:2,
							user_name:"咖啡会死的粉红色看到回复跨境电商",
							profilePhoto:"/static/images/testheadphoto.jpg"
						}
					},
				]
			};
		}
	}
</script>

<style>
	.box {
		column-count: 2;
		column-gap: 20rpx;
		width: 100%;
	}

	.card {
		overflow: hidden;
		border-radius: 20rpx;
		margin-bottom: 20rpx;
		width:100%;
		break-inside: avoid;
		/* border: 1px solid #000; */
		box-sizing: border-box;
	}
</style>