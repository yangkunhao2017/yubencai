<template>
	<view>
		<view class="bottom-box">
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text >历史记录</text>
				</view>
			</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="bottom-shi" >
				<view class="uni-flex uni-row view-between" style="margin-top: 10px;margin-left: 10px;">
					<text style="font-size: 18px;" >事假</text>
					<view class="uni-flex  view-right">
					<text class="text-leave">2021-11-06 09:00</text>
					</view>
				</view>
				<view class="uni-flex uni-column" style="margin-top: 10px;margin-left: 10px;">
					<text class="text-leave">开始时间: 2021-11-06 09:00</text>
					<text class="text-leave" style="margin-top: 5px;">结束时间: 2021-11-09 09:00</text>
				</view>
				<view class="uni-flex uni-row view-between">
					<text style="font-size: 18px;margin-top: 30px;margin-left: 10px;">审批人: 张三 李四</text>
					<view class="uni-flex view-right">
					<text style="color: #0c7cf9;margin-top: 30px;" v-if="status==0">审批中...</text>
					<text style="color: #4ac94a;margin-top: 30px;" v-if="status==1">已通过</text>
					<text style="color: red;margin-top: 30px;" v-if="status==2">已拒绝</text>
					</view>
				</view>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				status:0,
				type:3,
			}
		},
		methods: {
			
			}
	}
</script>

<style>
	.bottom-box {
		width: 100%;
	  height: 80px;
	  background-color: #0c7cf9;
	}
	.title-text {
		color: #FFFFFF;
		font-size: 18px;
		font-family: sans-serif;
		margin-top: 20px;
	}



	.text-leave {
		color: #c4c3c3;
	}

	.bottom-shi {
	  height: 150px;
	}

</style>
