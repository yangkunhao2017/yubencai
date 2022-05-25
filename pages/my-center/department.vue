<template>
	<view>
		<view class="bottom-box" :class="isUser?' bottom-box-user':'bottom-box-com'">
			<view class="uni-flex uni-row ">
				<view class="uni-seleton">
						<uni-icons  class="back-btn iconfont iconarrow_btn_left" type="arrowleft"   color="#fff" @click="navBack"/>
					</view>
				<view class="uni-flex title-text view-vertical-center" style="margin-bottom: 10px;margin-top: 10px;">
				<text v-if="isUser">我的部门</text>
				<text v-else="isUser">部门管理</text>
				</view>
			</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		<view class="uni-flex uni-row" style="margin-top: 10px;">
		<view class="uni-flex uni-row view-center" style="margin-left: 10px;margin: 10px;">
			<image class="job-logo" src="../../static/logo.png" mode="scaleToFill"></image>
			<text>重庆梦比优斯网络科技有限公司</text>
		</view>
		</view>
		<view style="border-bottom: 12px solid #ececec;"></view>
		
		<uni-collapse v-if="isUser">
		<uni-collapse-item title="市场部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="董事长"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="管理"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="财务部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="财务总监"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="财务主管"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		<uni-collapse-item title="技术开发部(3)">
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李总" rightText="技术总监"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="张三" rightText="技术主管"></uni-list-item>
				</view>
			</uni-list>
			<uni-list>
				<view class="uni-flex uni-row" style="margin-left: 20px;">
				<uni-list-item title="李四" rightText="职员"></uni-list-item>
				</view>
			</uni-list>
		</uni-collapse-item>
		</uni-collapse>
		<view class="uni-flex uni-row" style="margin-top: 10px;" v-else="isUser">
		<view class="uni-flex uni-row view-center" style="margin-left: 10px;margin: 10px;">
			<image class="job-logo" src="../../static/logo.png" mode="scaleToFill"></image>
			<text style="color: darkgray;margin-left: 10px;">新增部门</text>
		</view>
		</view>
		<view v-if="isUser"></view>
		<view v-else="isUser" style="border-bottom: 12px solid #ececec;"></view>
		<view v-if="isUser"></view>
		<view class="uni-flex uni-row view-between" style="margin-top: 20px;" v-else="isUser">
			<text style="margin-left: 10px;">公司成员</text>
			<text class="option" style="color: orange;margin-right: 10px;"><uni-icons type="gear-filled" color="orange"></uni-icons>添加成员</text>
		</view>
		<view v-if="isUser"></view>
		<view v-else="isUser" style="border-bottom: 1px solid #ececec;margin-top: 20px;"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isUser:false,
			}
		},
		methods: {
			// 返回上一页
				navBack() {
					uni.navigateBack();
				}
			}
	}
</script>

<style>
	.bottom-box {
		width: 100%;
	  /* height: 80px; */
	  
	}
	.bottom-box-com {
		background: #fc4039;
	}
	.bottom-box-user {
		background-color: #0c7cf9;
	}
	.title-text {
		color: #FFFFFF;
		font-size: 18px;
		font-family: sans-serif;
		/* margin-top: 20px; */
	}
	.job-logo{
		width: 35px;
		height: 35px;
	}
	.content {
		padding: 15px;
	}
	
	.text {
		font-size: 14px;
		color: #666;
		line-height: 20px;
	}
	.back-btn {
			width: 100%;
			position: absolute;
			z-index: 999;
			padding-top: var(--status-bar-height);
			padding-left: 20upx;
			padding-right: 20upx;
			top: 30upx;
			font-size: 40upx;
			color: #fff;
			display: flex;
			align-items: center;
			.nav-title {
				width: 590upx;
				text-align: center;
			}
		}
</style>
