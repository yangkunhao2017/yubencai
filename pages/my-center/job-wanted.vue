<template>
  <view>

    <view style="background-color: #FFFFFF">
      <view class="uni-flex  uni-row view-vertical-center  view-between  list-item">
        <text class="tian-text">期望职位</text>
		<text @click="showOnPopup()">{{this.onPosition[this.onValue].text}}</text>
		</view>
      <view class="uni-flex uni-row view-vertical-center view-between  list-item">
        <text class="tian-text">期望行业</text>
        <text @click="showUpPopup()">{{this.upIndustry[this.upValue].text}}</text>
      </view>
	  <view class="uni-flex uni-row view-vertical-center view-between  list-item">
	    <text class="tian-text">期望地点</text>
      <text @click="showSexPopup()">{{this.sexCity[this.sexValue].text}}</text>
	  </view>
	  <view class="uni-flex uni-row view-vertical-center view-between  list-item">
      <text class="tian-text">期望薪资</text>
	    <text  @click="showAddPopup()">{{this.addWages[this.addValue].text}}</text>
	  </view>
     
    </view>
  </view>

  <!-- 普通弹窗 -->
  <uni-popup ref ="sex" background-color="#fff" @change="change">
    <view class="popup-sex" :class="{ 'popup-height' : type === 'left' || type === 'right'}">
      <uni-data-select :localdata="sexCity" @change="sexChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <uni-popup ref="add" background-color="#fff" @change="change">
    <view class="popup-add" :class="{ 'popup-height': type === 'left' || type === 'right' }">
      <uni-data-select :localdata="addWages" @change="addChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <uni-popup ref ="up" background-color="#fff" @change="change">
    <view class="popup-up" :class="{'popup-height': type === 'left' || 'right'}">
      <uni-data-select :localdata="upIndustry" @change="upChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <uni-popup ref ="on" background-color="#fff" @change="change">
    <view class="popup-on" :class="{ 'popup-height' : type === 'left' || type === 'right'}">
      <uni-data-select :localdata="onPosition" @change="onChange" class="view-center"></uni-data-select>
    </view>
  </uni-popup>
  <view class="bottom-box uni-flex view-vertical-center" >
    <button class="button-info" style="margin-top: 200px;">保存信息</button>
  </view>

</template>

<script>
import UniPopup from "../../uni_modules/uni-popup/components/uni-popup/uni-popup";
export default {
  components: {UniPopup},
  data() {
    return {
      addValue:0,
      addWages:[
        {"value":0,"text":"3000"},
        {"value":1,"text":"5000"},
        {"value":2,"text":"10000"},
        {"value":3,"text":"10000及以上"}
      ],
      sexValue:0,
	  sexCity:[{"value":0,"text":"北京"},
	  {"value":1,"text":"上海"},
	  {"value":2,"text":"广东"},
	  {"value":3,"text":"深圳"},
	  {"value":4,"text":"重庆"},
	   ],
	   onValue:0,
	   onPosition:[{"value":0,"text":"Java工程师"},
	  {"value":1,"text":"销售经理"},
	  {"value":2,"text":"水电工"},
	  {"value":3,"text":"机修"},
	  {"value":4,"text":"服务员"},
	   ],
	   upValue:0,
	   upIndustry:[{"value":0,"text":"互联网"},
	  {"value":1,"text":"餐饮"},
	  {"value":2,"text":"汽车"},
	  {"value":3,"text":"家电"},
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
    showSexPopup(){
      this.sexValue = 0;
      this.$refs.sex.open('bottom');
    },
    sexChange(e){
      if(e!=this.sexValue){
        this.sexValue = e;
      }
    },
    showUpPopup(){
      this.upValue = 0;
      this.$refs.up.open('bottom');
    },
    upChange(e){
      if(e!=this.upValue){
        this.upValue = e;
      }
    },
	showOnPopup(){
		this.onValue = 0;
		this.$refs.on.open('bottom');
	},
	onChange(e){
		if (e!=this.onValue){
			this.onValue = e;
		}
	}
	
  }
}
</script>

<style>
.popup-add{
  height: 300px;
}
.popup-sex{
  height: 300px;
}
.popup-on{
	height: 300px;
}
.popup-up{
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
  height: 350px;
  background-color: #ececec;
}
.tian-text {
  color: #b4b6b6;
  font-size: 18px;
}
</style>
