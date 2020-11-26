<template>
	<view style="display: block;">
		<view class="new-header">
			<view class="header-item" @click="openCarList('大众')">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;">
						<image style="width: 5vw;height: 5vw;" src="/static/car/大众.png">
					</view>

					<view style="margin:auto;">大众</view>
				</view>
			</view>
			<view class="header-item" @click="openCarList('奔驰')">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;">
						<image style="width: 5vw;height: 5vw;" src="/static/car/奔驰.png">
					</view>

					<view style="margin:auto;">奔驰</view>
				</view>
			</view>
			<view class="header-item" @click="openCarList('宝马')">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;">
						<image style="width: 5vw;height: 5vw;" src="/static/car/宝马.png">
					</view>

					<view style="margin:auto;">宝马</view>
				</view>
			</view>
			<view class="header-item" @click="openCarList('马自达')">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;">
						<image style="width: 5vw;height: 5vw;" src="/static/car/马自达.png">
					</view>

					<view style="margin:auto;">马自达</view>
				</view>
			</view>
			<view class="header-item" @click="openCarList('奥迪')">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;">
						<image style="width: 5vw;height: 5vw;" src="/static/car/奥迪.png">
					</view>

					<view style="margin:auto;">奥迪</view>
				</view>
			</view>
		</view>

		<view class="news-title">
			<view class="title-item" @click="changType('1')">
				<view style="margin:auto;" :class="{ active: isActive === '1' }">默认排序</view>

			</view>
			<view class="title-item" @click="changType('2')">
				<view style="margin:auto;" :class="{ active: isActive === '2' }">订单最多</view>
			</view>

			<view class="title-item" @click="changType('3')">
				<view style="margin:auto;" :class="{ active: isActive === '3' }">离我最近</view>
			</view>
		</view>

		<view class="news-box">
			<view class="news-box-item">
				<view class="box-item-left">
					<image style="width: 80rpx;height: 80rpx;margin:auto" :src="carImg">
				</view>
				<view class="box-item-right">
					<view class="item-right-1"><text style="background-color: rgb(138,190,247,0.5);color:#007AFF;font-size: 24rpx;line-height: 48rpx;">4S店</text>
						<text style="margin-left: 20rpx;font-size: 30rpx;">深圳市南山区汽车销售服务有限公司</text>
					</view>
					<view class="item-right-2" style="font-size: 24rpx;">深圳市南山区石竹街道弘扬广场</view>
					<view class="item-right-3" style="color: #CCC;font-size: 24rpx;">距离42.30km / 售本省</view>
				</view>
			</view>
			<view class="news-box-item">
				<view class="box-item-left">
					<image style="width: 80rpx;height: 80rpx;margin:auto" :src="carImg">
				</view>
				<view class="box-item-right">
					<view class="item-right-1"><text style="background-color: rgb(138,190,247,0.5);color:#007AFF;font-size: 24rpx;line-height: 48rpx;">4S店</text>
						<text style="margin-left: 20rpx;font-size: 30rpx;">深圳市南山区汽车销售服务有限公司</text>
					</view>
					<view class="item-right-2" style="font-size: 24rpx;">深圳市南山区石竹街道弘扬广场</view>
					<view class="item-right-3" style="color: #CCC;font-size: 24rpx;">距离42.30km / 售本省</view>
				</view>
			</view>
			<view class="news-box-item">
				<view class="box-item-left">
					<image style="width: 80rpx;height: 80rpx;margin:auto" :src="carImg">
				</view>
				<view class="box-item-right">
					<view class="item-right-1"><text style="background-color: rgb(138,190,247,0.5);color:#007AFF;font-size: 24rpx;line-height: 48rpx;">4S店</text>
						<text style="margin-left: 20rpx;font-size: 30rpx;">深圳市南山区汽车销售服务有限公司</text>
					</view>
					<view class="item-right-2" style="font-size: 24rpx;">深圳市南山区石竹街道弘扬广场</view>
					<view class="item-right-3" style="color: #CCC;font-size: 24rpx;">距离42.30km / 售本省</view>
				</view>
			</view>
		</view>
	</view>


</template>

<script>
	export default {
		data() {
			return {
				isActive: '1',
				carImg:'/static/car/奥迪.png'
			}
		},
		onLoad() {

		},

		methods: {
			changType(index) {
				this.isActive = index

			},
			openCarList(name) {
				this.carImg = `/static/car/${name}.png`
			
			},
			getData() {

			},
			goDetail(e) {

			},
			share(e) {}

		}
	}
</script>

<style>
	.new-header {
		width: 100vw;
		height: 60px;
		display: flex;
		justify-content: space-between;
		background-color: #FFFFFF;
	}

	.header-item {
		width: 20vw;
		display: flex;
	}

	.news-title {
		width: 100vw;
		height: 30px;
		display: flex;
		justify-content: space-between;
	}

	.title-item {
		display: flex;
		width: 33vw;
		color: #bababa;
		font-size: 14px;
	}

	.active {
		color: #007AFF;
	}

	.news-box {
		width: 100vw;
		/* height: 150rpx; */
		background-color: #FFF;
		display: flex;
		flex-direction: column;
	}

	.news-box-item {
		display: flex;
		/* border-bottom: 1px #BABABA solid; */
		position: relative;
		width: 100vw;
		margin-bottom: 10rpx;
		/* background-color: #FFF; */
	}

	.news-box-item:after {
		content: '';
		height: 1px;
		width: 90%;
		background-color: #CCC;
		position: absolute;
		bottom: 0rpx;
		left: 5%;
		/* transform: translate(-50%); */
	}

	.box-item-left {
		width: 100rpx;
		height: 150rpx;
		display: flex;

	}

	.box-item-right {
		flex: auto;
		height: 150rpx;
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
		padding: 10rpx;
		justify-content: space-between;

	}
</style>
