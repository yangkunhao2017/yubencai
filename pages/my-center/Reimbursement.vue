<template>
	<view>
		<view class="bottom-box">
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text style="margin-left: 60px;">报销</text>
				</view>
				<view class="title-ding uni-flex view view-right">
				<text style="margin-right: 10px;">历史记录</text>
				</view>
			</view>
		</view>
		<view>
			<view class="uni-flex uni-row view-vertical-center view-between list-item">
				<view>
				<text class="text-fu">*</text>
			  <text class="text-leave">报销金额</text>
			  </view>
			  <text class="text-leave">请输入报销金额</text>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			
			
			<view class="bottom-shi uni-flex" >
				<view style="margin-top: 10px;">
				<text class="text-fu" style="margin-left: 10px;">*</text>
			  <text class="text-leave" >费用说明</text>
			  <view class="uni-flex uni-column">
			  <text class="text-leave" style="margin-left: 20px;margin-top: 10px;">请输入报销费用说明</text>
			  </view>
				</view>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="uni-flex uni-row view-vertical-center view-between" style="margin-top: 20px;margin-bottom: 20px;">
				<!-- <view> -->
					<text class="text-leave" style="margin-left: 10px;">报销凭据</text>
				<!-- </view> -->
				<view class="example-body" >
					<uni-file-picker  limit="9" ></uni-file-picker>
				</view>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="uni-flex uni-row view-vertical-center view-between list-item">
			  <view>
			  		<text class="text-fu">*</text>
			  <text class="text-leave">所在部门</text>
			  	</view>
			  <text @click="showSexPopup()">{{this.sexRange[this.sexValue].text}}</text>
			</view>
			
				<view class="uni-flex uni-row view-vertical-center view-between list-item">
					<view>
					<text class="text-fu">*</text>
				  <text class="text-leave">审批人</text>
				  </view>
				  <text class="text-leave" >请选择审批人员(可多选)</text>
				</view>
				 
				
			<view class="button-box uni-flex view-vertical-center" >
			  <button class="button-info" style="margin-top: 10px;">提交申请</button>
			</view>
			
			<uni-popup ref="sex" background-color="#fff" @change="change">
			  <view class="popup-sex " :class="{ 'popup-height': type === 'left' || type === 'right' }">
			   <uni-data-select :localdata="sexRange" @change="sexChange" class="view-center"></uni-data-select>
				 </view>
				</uni-popup>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				sexValue:0,
				sexRange:[
				  {"value": 0,"text": "销售部"},
				  {"value": 1,"text": "后勤部"},
				  {"value": 1,"text": "财务部"}
				],
			}
		},
		methods: {
			showSexPopup(){
			  this.sexValue = 0;
			  this.$refs.sex.open('bottom');
			},
			sexChange(e){
			  if(e!=this.sexValue){
			    this.sexValue = e;
			  }
			},
		}
	}
</script>

<style>
	.example-body {
		/* padding: 10px; */
		/* padding-top: 0; */
		height:20px;
		width: 140px;
		margin-bottom: 20px;
		margin-right: -90px;
	}
	.bottom-box {
		width: 100%;
	  /* height: 50px; */
	  background-color: #0c7cf9;
	}
	.title-text {
		color: #FFFFFF;
		font-size: 18px;
		font-family: sans-serif;
		/* margin-top: 20px; */
	}
	.title-ding {
		color:#ffffff;
		font-size: 16px;
		/* margin-top: 20px; */
	}
	
	.list-item{
	  height: 40px;
	  padding: 10px 0;
	  margin: 10px;
	  border-bottom: 1px solid #e5e5e5;
	}
	.text-leave {
		color: #c4c3c3;
	}
	.text-fu {
		color: red;
	}
	.bottom-shi {
	  height: 200px;
	}
	.popup-sex{
	  height: 300px;
	}
	.button-box {
		height: 150px;
		background-color: #ececec;
	}
	.button-info{
	  background-color: #0c7cf9;
	  color: white;
	  width:95%;
	}
</style>
