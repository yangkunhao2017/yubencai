<template>
	<view>
		<view class="uni-flex uni-column view-vertical-center title-box" style="background-color: #ececec;">
      <image class="message-list-box-logo" src="../../../static/logo.png" ></image>
      <text style="color: #919191">点击修改头像</text>
    </view>
    <view style="background-color: #FFFFFF">
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>昵称</text>
        <text>11111</text>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>性别</text>
        <text @click="showSexPopup()">{{this.sexRange[this.sexValue].text}}</text>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>生日</text>
		<picker mode="date" @change="bindDateChange">
		  <view :class="timeIndex == 4 ? 'active-time' : ''">{{anyDate}}</view>
		</picker>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>身高</text>
        <text>11111</text>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>学历</text>
        <text @click="showAddPopup()">{{this.addEducation[this.addValue].text}}</text>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>现居住地</text>
<!--    <pickerAddress @change="cityChange">-->
<!--          {{this.cityArea}}-->
<!--      </pickerAddress>-->

      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>手机号码</text>
        <text>11111</text>
      </view>
      <view class="uni-flex uni-row view-vertical-center view-between list-item">
        <text>邮箱</text>
        <text>11111</text>
      </view>
    </view>
	</view>
  <!-- 普通弹窗 -->
  <uni-popup ref="sex" background-color="#fff" @change="change">
    <view class="popup-sex " :class="{ 'popup-height': type === 'left' || type === 'right' }">
     <uni-data-select :localdata="sexRange" @change="sexChange" class="view-center"></uni-data-select>
	 </view>
	</uni-popup>
	<uni-popup ref="add" background-color="#fff" @change="change">
	  <view class="popup-add" :class="{ 'popup-height': type === 'left' || type === 'right' }">
	      <uni-data-select :localdata="addEducation" @change="addChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <view class="bottom-box uni-flex view-vertical-center">
    <button class="button-info">保存信息</button>
  </view>
</template>

<script>
// import pickerAddress from '@/components/ss-select-city/pickerAddress.vue
export default {
    // components: {
    //   pickerAddress
    // },
	
		data() {
			return {
        sexValue:0,
        sexRange:[
          {"value": 0,"text": "男"},
          {"value": 1,"text": "女"}
        ],
		addValue:0,
		addEducation:[
        {"value":0,"text":"小学"},
        {"value":1,"text":"初中"},
        {"value":2,"text":"高中/中专"},
        {"value":3,"text":"本科及以上"}
      ],
	  timeIndex:0,
	  anyDate:'请选择出生日期',
	  cityArea:"请选择地区",
	}
    },
    // onLoad(){
    //   this.array = []
    //   console.log(areaData[0].name)
    //   this.array[0] = areaData.map(obj => {
    //     return {
    //       name: obj.name
    //     }
    //   })
    //   console.log(this.array[0])
    // },
		methods: {
			showSexPopup(){
        this.sexValue = 0;
        this.$refs.sex.open('bottom');
      },
	  showAddPopup(){
        this.addValue = 0;
		  this.$refs.add.open('bottom');
	  },
      sexChange(e){
        if(e!=this.sexValue){
          this.sexValue = e;
        }
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
	    this.anyDate = '选择出生日期'
	  },
    //   cityChange(data) {
		  // console.log(data)
    //    this.cityArea  = data.data.join("")
    //   }
		}
	}
</script>

<style>

.title-box{
  height: 150px;
  background-color: #919191;
}
.popup-sex{
  height: 300px;
}
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
	height: 100px;
	background-color: #ececec;
}
</style>
