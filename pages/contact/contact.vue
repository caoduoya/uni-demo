<template>
	<view class="contact">
		<image class="img" src="http://www.itcast.cn/2018czydz/images/gywmban.jpg" mode=""></image>
		<view @click="phone" class="info">
			<view>联系电话:13870244028(点击拨打)</view>
			<view>联系地址:江西省九江市都昌县阳光府邸</view>
		</view>
		<map :scale="scale" :markers="markers" :latitude="latitude" :longitude="longitude" class="map"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				longitude: 116.198239,
				latitude: 29.277712,
				scale:13,
				markers: [{
					longitude: 116.198239,
					latitude: 29.277712,
					iconPath: '../../static/logo.png',
					height:30,
					width:30
				}]
			}
		},
		methods: {
			phone(){
				uni.makePhoneCall({
					phoneNumber:'13870244028'
				})
			}
		}
	}
</script>

<style lang="scss">
	.contact {
		.img {
			width: 750rpx;
			height: 320rpx;
		}

		.info {
			padding: 10rpx 20rpx;
			font-size: 30rpx;

			view {
				line-height: 80rpx;
				border-bottom: 1px solid #eee;
			}
		}

		.map {
			width: 750rpx;
			height: 750rpx;
		}
	}
</style>
