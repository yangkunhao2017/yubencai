<template>
	<view>
		<view class="bottom-box" >
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text style="margin-left: 60px;">渝额宝</text>
				</view>
				<view class="title-ding uni-flex  view-right">
				<text style="margin-right: 10px;">我的定期</text>
				</view>
			</view>
			<view class="uni-flex uni-column title-text view-vertical-center">
		  <text class="tian-text" style="margin-top: 10px;margin-left: 10px;">总金额(元)</text>
		<text class="rmb">126999.00</text>
		<text class="text-nian" style="margin-bottom: 20px;">年化:1.94%</text>
		</view>
		<view class="bottom-bo">
			<view class="uni-flex uni-row view-between">
				<view class="shou-text uni-flex uni-column view-center">
					<text>昨日收益(元)</text>
					<text>8.8</text>
				</view>
				<view class="shou-text uni-flex uni-column view-center">
					<text>累计收益(元)</text>
					<text>8.8</text>
				</view>
				<view class="shou-text uni-flex uni-column view-center">
					<text>定期金额(元)</text>
					<text>8.8</text>
				</view>
			</view>
		</view>
		</view>
    <view class=" uni-flex uni-row view-vertical-center view-between">
      <button class="button-yu">转出</button>
      <button class="button-gong">转入</button>
    </view>
	<view style="border-bottom: 12px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
    <view>
      <text class="text-profit">资金明细</text>
      <view style="border-bottom: 1px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
    </view>
    <view class="uni-flex uni-column">
    <view class="uni-flex uni-row">
      <text class="text-profit">收益</text>
      <text class="uni-flex view-vertical-center view-right" style="color: #0ac50a">+30000</text>
    </view>
      <view class="uni-flex uni-row">
        <text class="text-time">2022.06.21 08:23</text>
      </view>
    </view>
    <view style="border-bottom: 1px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.title-text {
		color: #FFFFFF;
		font-size: 18px;
		font-family: sans-serif;
		margin-top: 20px;
	}
	.title-ding {
		color:#ffffff;
		font-size: 16px;
		margin-top: 20px;
	}
	.text-nian {
		margin-top: 10px;
		margin-left: 15px;
		color: #d7d5d5;
		font-size: 13px;
	}
	.bottom-box {
		width: 100%;
	  height: 230px;
	  background-color: #0c7cf9;
	}
	.bottom-bo {
		width: 100%;
		height: 60px;
		background-color: #2786f1;
	}
	.tian-text {
	  color: #ffffff;
	  font-size: 15px;
	  
	}
	.shou-text {
	  color: #ffffff;
	  font-size: 15px;
	  margin: 10px;
	  margin-left: 10px;
	  margin-right: 10px;
	}
	
	.rmb {
		color: #ffffff;
		font-size: 20px;
		font-family:sans-serif;
		margin-left: 15px;
		margin-top: 10px;
	}
	.button-yu {
		background-color: #FFFFFF;
		color: white;
		width: 170px;
		line-height: 45px;
		 margin-left: 10px;
		 margin-top: 20px;
		  color: #2786f1;
	}
	.button-gong {
		background-color: #2786f1;
		color: white;
		width: 170px;
		line-height: 45px;
		 margin-top: 20px;
		 color: #FFFFFF;
	}
  .text-profit{
    font-family:sans-serif;
    font-size: 18px;
	margin-left: 10px;
  }
  .text-time {
    color: #919191;
    font-size: 13px;
	margin-left: 10px;
  }
</style>
