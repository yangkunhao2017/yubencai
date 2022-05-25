<template>
	<view style="background-color: #f6f6f6" >
		<view class="uni-flex uni-row item-box">
      <button class="item-box-active" style="background-color: #fc4039;color: #fff;">请假</button>
      <button style="background-color: #fc4039;color: #fff;">报销</button>
	  <button style="background-color: #fc4039;color: #fff;">已处理</button>
    </view>
    <view class="uni-flex uni-column">
      <view class="uni-flex uni-column item-item" v-for="i in 10">
        <view class="uni-flex uni-row view-between">
          <view class="uni-flex uni-column">
            <text style="font-size: 20px">张伟提交的请假</text>
            <text style="font-size: 15px;color: #929292;margin-top: 10px;">请假类型：事假</text>
          </view>
		  
		  <view class="uni-flex" style="border: 1px solid #929292;width: 70px;height: 30px;margin-top: 20px;">
		    <view class="uni-flex view-vertical-center">
		      <text v-if="status==0">拒绝</text>
		    </view>
		  
		 
		  </view>
        </view>
        <view class="uni-flex uni-row view-between">
          <view class="uni-flex uni-column" style="margin-top: 10px;">
            <text style="font-size: 12px;color: #929292">开始时间：2022-05-15 23:59:59 </text>
			<text style="font-size: 12px;color: #929292;margin-top: 5px;">结束时间：2022-05-15 23:59:59 </text>
          </view>
		 
		  <view class="uni-flex" style="background-color: #4c8ce7;width: 70px;height: 30px;color: #fff;margin-top: 20px;">
		    <view class="uni-flex view-vertical-center">
		      <text v-if="status==0">同意</text>
		    </view>
		  </view>
		  
        </view>
      </view>
    </view>
	</view>
</template>

<script>
	export default {
		name:"hz-message-send-list",
		data() {
			return {
				isUser:false,
        status:0,
				type: 3,
			};
		}
	}
</script>

<style>
/*去掉按钮边框*/
button:after{
  border: none;
  
}
.item-box {
  height: 50px;
  background-color: #fc4039;
}

.item-box button {
  width: 25%;
  height: 100%;
  border-radius: 0px;
  line-height: 50px;
  text-align: center;
  color: #333;
  font-size: 14px;
  background-color: #FFFFFF;
}
.item-box-active{
  border-bottom: 2px solid #4c8ce7;
}

.item-item {
  margin-top: 10px;
  height: 125px;
  background-color: #fff;
  border-bottom: 1px solid #e5e5e5;
}

.item-item view{
  padding: 0 5px;
}

.item-option-box {
  width: 100vw;
}

.item-option-box button{
  height: 100%;
  border-radius: 0px;
  line-height: 50px;
  text-align: center;
  color: #2f6ce8;
  font-size: 16px;
  background-color: #FFFFFF;
}

</style>