<template>
	<view>
	
    <view style="background-color: #FFFFFF">
      <view class="uni-flex  uni-column    list-item">
        <text>学校名称:</text>
		<text class="tian-text">请填写</text>
      </view>
	  
      <view class="uni-flex uni-column   list-item">
        <text>专业名称:</text>
        <text class="tian-text">请填写</text>
      </view>
	  <view class="uni-flex uni-row view-vertical-center view-between list-item">
	    <text>学历</text>
	    <text @click="showAddPopup()">{{this.addEducation[this.addValue].text}}</text>
	  </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>入学时间</text>
		<picker mode="date" @change="bindDateChange">
		  <view :class="timeIndex == 4 ? 'active-time' : ''">{{anyDate}}</view>
		</picker>
      </view>
	  <view class="uni-flex uni-row view-vertical-center view-between list-item">
	    <text>毕业时间</text>
	  		<picker mode="date" @change="bindDateChange">
	  		  <view :class="timeIndex == 4 ? 'active-time' : ''">{{anyDate}}</view>
	  		</picker>
	  </view>
    </view>
	</view>
  <!-- 普通弹窗 -->
	<uni-popup ref="add" background-color="#fff" @change="change">
	  <view class="popup-add" :class="{ 'popup-height': type === 'left' || type === 'right' }">
	      <uni-data-select :localdata="addEducation" @change="addChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <view class="bottom-box uni-flex view-vertical-center" >
    <button class="button-info" style="margin-top: 100px;">保存信息</button>
  </view>
</template>

<script>
export default {
		data() {
			return {
		addValue:0,
		addEducation:[
        {"value":0,"text":"小学"},
        {"value":1,"text":"初中"},
        {"value":2,"text":"高中/中专"},
        {"value":3,"text":"本科及以上"}
      ],
	  timeIndex:0,
	  anyDate:'请选择日期',
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
		}
	}
</script>

<style>
.popup-add{
  height: 300px;
}
image{
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
.list-item{
  height: 40px;
  padding: 10px 0;
  margin: 10px;
  border-bottom: 1px solid #e5e5e5;
}
.button-info{
  background-color: #0c7cf9;
  color: white;
  width:95%;
}
.bottom-box {
	height: 260px;
	background-color: #ececec;
}
.tian-text {
	margin-top: 8px;
	color: #b4b6b6;
  font-size: 16px;
}
</style>
