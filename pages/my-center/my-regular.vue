<template>
	<view style="background-color: #eae9e9;">
		<view class="bottom-box uni-flex title-text">
				<text style="margin-top: 10px;margin-left: 20vh;">我的定期</text>
		</view>
		<view class="uni-flex uni-column title-text uni-center bottom-bo" style="margin-bottom: 20px">
		  <text class="tian-text" style="margin-top: 10px;margin-left: 10px;">总金额(元)</text>
			<text class="rmb">126999.00</text>
		<view class="uni-flex uni-row view-between">
		<view class="shou-text uni-flex uni-column view-center">
			<text>昨日收益(元)</text>
			<text class="shou">8.8</text>
		</view>
		<view class="shou-text uni-flex uni-column view-center">
			<text>累计收益(元)</text>
			<text class="shou">8.8</text>
		</view>
		<view class="shou-text uni-flex uni-column view-center">
			<text>可取出金额(元)</text>
			<text class="shou">8.8</text>
		</view>
		</view>
		<view class=" uni-flex uni-row view-vertical-center view-between">
		  <button class="button-yu">取出</button>
	  	</view>
	  </view>
    <view class="uni-flex uni-column" >
      <text class="title-ding">我的订单</text>

      <view class="bottm-ding " v-for= "i in 3">
        <view class="uni-flex uni-row view-between">
        <text class="text-profit">订单号: xxxxo344</text>
		  <view class="uni-flex  view-right shou-text">
		  <text >2022.10.1 09:11</text>
		  </view>
        </view>
        <view style="border-bottom: 1px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
		<view class="uni-flex uni-row shou-text view-between">
        <text>存入金额(元):</text>
      <view class="uni-flex  view-right">
      <text>10000.00</text>
      </view>
		</view>
        <view class="uni-flex uni-row shou-text view-between">
          <text>年化收益:</text>
          <view class="uni-flex  view-right">
            <text style="color: red">2.01%</text>
          </view>
        </view>
        <view class="uni-flex uni-row shou-text view-between">
          <text>存入年限:</text>
          <view class="uni-flex  view-right">
            <text>1年</text>
          </view>
        </view>
        <view class="uni-flex uni-row shou-text view-between">
          <text>累计收益(元):</text>
          <view class="uni-flex  view-right">
            <text style="color: red">10000.00</text>
          </view>
        </view>
        <view style="border-bottom: 10px solid #e8e7e7;margin-top: 10px;margin-bottom: 10px"></view>
      </view>
    </view>
	</view>
</template>

<script>
	import UniDataPickerView from "../../uni_modules/uni-data-picker/components/uni-data-pickerview/uni-data-pickerview";
  export default {
    components: {UniDataPickerView},
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
	}
	.title-ding {
		font-size: 18px;
    font-family: Candara;
    margin-bottom: 10px;
    margin-left: 10px;
	}

	.bottom-box {
		width: 100%;
	  height: 160px;
	  background-color: #0c7cf9;
	  border-radius: 0px 0px 50px 50px;
	  margin-bottom: -90px;
	}
	.bottom-bo {
		width: 95%;
		height: 300px;
		background-color: #FFFFFF;
		border-radius: 10px 10px 10px 10px;
		margin-left: 10px;
	}
  .bottm-ding {
    width: 95%;
    height: 200px;
    background-color: #FFFFFF;
    border-radius: 10px 10px 10px 10px;
    margin-left: 10px;
  }
	.tian-text {
	  color: #919191;
	  font-size: 15px;
	  
	}
	.shou-text {
	  color: #919191;
	  font-size: 15px;
	  margin-top: 10px;
	  margin-left: 10px;
	  margin-right: 10px;
	}
	.shou {
		color: #2786f1;
	}
	.rmb {
		color: black;
		font-size: 20px;
		font-family:sans-serif;
		margin-left: 15px;
		margin-top: 10px;
	}
	.button-yu {
		background-color: #FFFFFF;
		width: 300px;
		line-height: 45px;
		border: 1px solid #2786f1;
		  color: #2786f1;
	}

  .text-profit{
    font-family:sans-serif;
    font-size: 18px;
	margin-left: 10px;
	margin-top: 10px;
  }
  .text-time {
    color: #919191;
    font-size: 13px;
	margin-left: 10px;
  }
</style>
