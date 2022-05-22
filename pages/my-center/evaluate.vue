<template>
	<view>
    <view style="border-bottom: 12px solid #dedddd;"></view>
		<view style="background-color: #FFFFFF">
		  <view class="uni-flex  uni-column   list-item">
		    <text style="font-size: 18px;margin-top: 10px;">个人优势</text>
			<text style="color: #b4b6b6;font-size: 15px; margin-top: 10px;">写下你最擅长的事情，展示你的特别之处，分享你在工作中取得的成绩等...</text>
			</view>
		</view>
			<view class="bottom-box uni-flex " >
			  <text class="tian-text" style="margin-top: 10px;margin-left: 10px;">请填写</text>
			</view>
			<view class=" uni-flex view-vertical-center" >
			  <button class="button-info" style="margin-top: 200px;">保存信息</button>
			</view>
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
  height: 200px;
  background-color: #ececec;
  margin: auto;
  margin-top: 40px;
}
.tian-text {
  color: #b4b6b6;
  font-size: 18px;
}
.button-info{
  background-color: #0c7cf9;
  color: white;
  width:95%;
}

</style>
