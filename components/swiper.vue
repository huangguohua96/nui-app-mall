<template>
	<view>
		<swiper class="swiper" :indicator-dots="swiper.indicatorDots"
		:autoplay="swiper.autoplay" :interval="swiper.interval" :duration="swiper.duration" 
		:circular="swiper.circular" :indicator-color="swiper.indicatorColor" :indicator-active-color="swiper.indicatorActiveColor">
			<swiper-item v-for="(image, index) in swiper.images" :key="index">
				<image :src="image"/>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		props: {
			swiper: Object
		},
		onLoad() {
			console.log(this.swiper.images[1]);
		}
	}
</script>

<style lang="scss">
	.swiper{
		width: 720rpx; 
		height: 360rpx;
		border-radius: 10rpx;
		overflow: hidden;
		image{
			width: 100%;
			height: 360rpx;
		}
	}
</style>
