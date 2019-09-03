<template>
    <view class="content">
		<view class="search">
			<input type="text" value="" />
			<span class="iconfont icon-zhenhuichongtubiaozhizuo-kuozhan-"></span>
		</view>
		<view class="page-section swiper">
			<myswiper :swiper="swiper" />
		</view>
    </view>
</template>

<script>
	import myswiper from '../../components/swiper.vue'
	import '../../common/css/font/iconfont.css'
	export default {
	    data() {
	        return {
	            swiper:{
					images: [
						'/static/images/index/ad1.jpg', 
						'/static/images/index/ad2.jpg', 
						'/static/images/index/ad3.jpg', 
						'/static/images/index/ad4.jpg'
					],
					indicatorDots: true,
					autoplay: true,
					circular: true,
					interval: 3000,
					duration: 500,
					indicatorColor: '#fff',
					indicatorActiveColor: '#FF5777'
				},
				typeOfGoods: [
					
				],
	            
	        }
	    },
	    methods: {
	        
	    },
		onLoad() {
			console.log(this.swiper.images[1]);
		},
		components: {
			myswiper
		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 0 15rpx;
		.search{
			position: relative;
			height: 50rpx;
			width: 100%;
			padding-top: 20rpx;
			input{
				height: 100%;
				width: 100%;
				border: 1px solid #FF5777;
				border-radius: 30rpx;
			}
			span.iconfont{
				position: absolute;
				left: 24rpx;
				top: 28rpx;
				font-size: 34rpx;
				color: #FF5777;
			}
		}
		.swiper{
			box-sizing: border-box;
			height: 380rpx;
			width: 720rpx;
			padding: 20rpx 0;
			overflow: hidden;
		}
	}
	
</style>
