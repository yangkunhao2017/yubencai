<template>
	<view>
		 <view class="uni-flex uni-column">
		      <view class="uni-flex uni-row message-list-box" v-for="index in 10">
		        <view>
		          <image class="message-list-box-logo" src="../../../static/logo.png" ></image>
		        </view>
		        <view class="uni-flex uni-column message-list-context">
		          <view class="uni-flex">
		            <text class="uni-ellipsis" style="font-size: 15px">重庆市梦比优斯网络科技有限公司</text>
		          </view>
		          <view class="uni-flex view-between">
		            <text class="uni-ellipsis-1" style="font-size: 12px;color: #99999a">消息内容消息内容消息内容消息容消息容消息容消息容消息容消息容消息容消息容消息容消息</text>
		            <uni-icons type="smallcircle-filled" color="red"></uni-icons>
		          </view>
		          <view>
		            <text class="uni-ellipsis" style="font-size: 8px">2022-15-13 23:59:59</text>
		          </view>
		        </view>
		      </view>
     </view>
	</view>
</template>

<script>
	export default {
		name:"hz-message-list",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.message-list-box {
  width: 100vw;
  height: 80px;
  background-color: #ffffff;
  border-bottom: 1px solid #e5e5e5;
}

.message-list-box-logo {
  width: 60px;
  height: 60px;
  margin-top: 10px;
  margin-left: 10px;
}

.message-list-context {
  width: 75vw;
  margin: 10px;

}
</style>