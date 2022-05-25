<template>
	<view>
		<view class="bottom-box">
			<view class="uni-flex uni-row ">
				<view class="uni-flex title-text view-vertical-center">
				<text style="margin-left: 60px;">请假</text>
				</view>
				<view class="title-ding uni-flex view view-right">
				<text  style="margin-right: 10px;">历史记录</text>
				</view>
			</view>
		</view>
		<view>
			<view class="uni-flex uni-row view-vertical-center view-between list-item">
				<view>
				<text class="text-fu">*</text>
			  <text class="text-leave">请假类型</text>
			  </view>
			  <text @click="showAddPopup()">{{this.addEducation[this.addValue].text}}</text>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="uni-flex uni-row view-vertical-center view-between list-item">
				<view>
				<text class="text-fu">*</text>
			  <text class="text-leave">开始时间</text>
				</view>
					<picker mode="date" @change="bindDateChange">
					  <view :class="timeIndex == 4 ? 'active-time' : ''">{{anyDate}}</view>
					</picker>
			</view>
			<view class="uni-flex uni-row view-vertical-center view-between list-item">
				<view>
				<text class="text-fu">*</text>
			  <text class="text-leave">结束时间</text>
				</view>
					<picker mode="date" @change="bindDateChange">
					  <view :class="timeIndex == 4 ? 'active-time' : ''">{{anyDate}}</view>
					</picker>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="bottom-shi uni-flex" >
				<view style="margin-top: 10px;">
				<text class="text-fu" style="margin-left: 10px;">*</text>
			  <text class="text-leave" >请假事由</text>
			  <view class="uni-flex uni-column">
			  <text class="text-leave" style="margin-left: 20px;margin-top: 10px;">请输入请假事由</text>
			  </view>
				</view>
			</view>
			<view style="border-bottom: 12px solid #ececec;"></view>
			<view class="uni-flex uni-row view-vertical-center view-between" style="margin-top: 20px;margin-bottom: 20px;">
				<!-- <view> -->
					<text class="text-leave" style="margin-left: 10px;">上传图片</text>
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
			  <text class="text-leave">审批流程</text>
			  <text class="text-leave">部门内逐级上报审批</text>
			</view>
			<view class="button-box uni-flex view-vertical-center" >
			  <button class="button-info" style="margin-top: 10px;">提交申请</button>
			</view>
			<uni-popup ref="add" background-color="#fff" @change="change">
				  <view class="popup-add" :class="{ 'popup-height': type === 'left' || type === 'right' }">
				      <uni-data-select :localdata="addEducation" @change="addChange" class="view-center"></uni-data-select>
			  </view>
			</uni-popup>
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
				addValue:0,
						addEducation:[
				  {"value":0,"text":"事假"},
				  {"value":1,"text":"婚假"},
				  {"value":2,"text":"产假"},
				  {"value":3,"text":"陪产假"},
				  {"value":3,"text":"丧假"},
				  {"value":3,"text":"年假"}
				],
				timeIndex:0,
				anyDate:'请选择日期',
				sexValue:0,
				sexRange:[
				  {"value": 0,"text": "销售部"},
				  {"value": 1,"text": "后勤部"},
				  {"value": 1,"text": "财务部"}
				],
			}
		},
		methods: {
			showAddPopup(){
			  this.addValue = 0;
					  this.$refs.add.open('bottom');
			},
		
			addChange(e){
					  if(e!=this.addValue){
						  this.addValue=e;
					  }
			},
			bindDateChange (e) {
			  console.log(e)
			  this.anyDate = e.detail.value
			  this.timeIndex = 4
			},
			changeTime(index) {
			  this.timeIndex = index
			  this.anyDate = '选择日期'
			},
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
	  /* height: 10px; */
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
	.popup-add{
	  height: 300px;
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
