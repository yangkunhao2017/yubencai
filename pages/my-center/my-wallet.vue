<template>
	<view>
		<view class="bottom-box uni-flex uni-column" >
		  <text class="tian-text" style="margin-top: 10px;margin-left: 10px;">钱包余额</text>
		  <view class="uni-flex uni-row">
		<text class="rmb">126999.00</text>
      <text style="color: #FFFFFF;margin: 15px;margin-left: 5px;" >¥</text>
	  </view>
      <view class=" uni-flex view-vertical-center " >
        <button class="button-info">充值</button>
        <button class="button-ti">提现</button>
      </view>
		</view>
    <view class=" uni-flex uni-row view-vertical-center view-between">
      <button class="button-yu">渝额宝</button>
      <button class="button-gong">预支工资</button>
    </view>
	<view style="border-bottom: 12px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
    <view>
      <text class="text-profit">收益明细</text>
      <view style="border-bottom: 1px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
    </view>
    <view class="uni-flex uni-column">
    <view class="uni-flex uni-row">
      <text class="text-profit">工资发放</text>
      <text class="uni-flex view-vertical-center view-right" style="color: #0ac50a">+30000</text>
    </view>
      <view class="uni-flex uni-row">
        <text class="text-time">重庆梦比优斯网络科技有限公司</text>
        <text class="text-time uni-flex view-vertical-center view-right">2022.05.23 20:11</text>
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
	.bottom-box {
		width: 95%;
	  height: 150px;
	  background-color: #0c7cf9;
	  margin: auto;
	  margin-top: 40px;
	  border-radius: 10px 10px 0px 0px;
	}
	.tian-text {
	  color: #ffffff;
	  font-size: 15px;
	  
	}
	.button-info{
	  background-color: #9bbde3;
	  color: white;
	  line-height: 31px;
	  width: 85px;
	}
	.button-ti {
		background-color:green;
		color: white;
		line-height: 31px;
		width: 85px;
	}
	.rmb {
		color: #ffffff;
		font-size: 20px;
		font-family:sans-serif;
		margin-left: 10px;
		margin-top: 10px;
	}
	.button-yu {
		background-color: #ec9922;
		color: white;
		width: 170px;
		line-height: 60px;
		 margin-left: 10px;
		 margin-top: 20px;
		  
	}
	.button-gong {
		background-color: #f1486f;
		color: white;
		width: 170px;
		line-height: 60px;
		 margin-top: 20px;
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
