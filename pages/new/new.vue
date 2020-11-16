<template>
	<view style="display: block;">
		<view class="new-header"  >
			<view class="header-item">
				<view style="margin:auto;display: flex;flex-direction: column;">
					<view style="margin:auto;"><image style="width: 5vw;height: 5vw;" src="/static/car/大众.png"></view>
					
						<view style="margin:auto;">大众</view>
					</view> 
				</view>
				<view class="header-item">
					<view style="margin:auto;display: flex;flex-direction: column;">
						<view style="margin:auto;"><image style="width: 5vw;height: 5vw;" src="/static/car/奔驰.png"></view>
						
							<view style="margin:auto;">奔驰</view>
						</view> 
					</view>
				<view class="header-item">
					<view style="margin:auto;display: flex;flex-direction: column;">
						<view style="margin:auto;"><image style="width: 5vw;height: 5vw;" src="/static/car/宝马.png"></view>
						
							<view style="margin:auto;">宝马</view>
						</view> 
					</view>
				<view class="header-item">
					<view style="margin:auto;display: flex;flex-direction: column;">
						<view style="margin:auto;"><image style="width: 5vw;height: 5vw;" src="/static/car/马自达.png"></view>
						
							<view style="margin:auto;">马自达</view>
						</view> 
					</view>
					<view class="header-item">
						<view style="margin:auto;display: flex;flex-direction: column;">
							<view style="margin:auto;"><image style="width: 5vw;height: 5vw;" src="/static/car/奥迪.png"></view>
							
								<view style="margin:auto;">奥迪</view>
							</view> 
						</view>
			</view>
			
			<view class="news-title">
				<view class="title-item" @click="changType('1')">
					<view style="margin:auto;" :class="{ active: isActive === '1' }">默认排序</view>
					
					</view>
				<view class="title-item" @click="changType('2')">
					<view style="margin:auto;" :class="{ active: isActive === '2' }">订单最大</view>
					</view>
					
					<view class="title-item" @click="changType('3')">
						<view style="margin:auto;" :class="{ active: isActive === '3' }">离我最近</view>
						</view>
						
					
				
	</view>
	</view>
	
			
</template>

<script>
	export default {
		data() {
			return {
				isActive:'1',
			}
		},
		onLoad() {
			
		},
		
		methods: {
			changType(index) {
				this.isActive = index
				
			},
			getData() {
				
			},
			goDetail(e) {
				
			},
			share(e) {
				}
				
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
	
</style>
