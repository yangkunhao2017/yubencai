<template>
	<view>
		<view class="bottom-box" :class="isUser?' bottom-box-user':'bottom-box-com'">
			<view class="uni-flex uni-row ">
				<view class="uni-seleton">
						<uni-icons  class="back-btn iconfont iconarrow_btn_left" type="arrowleft"   color="#fff" @click="navBack"/>
					</view>
				<view class="uni-flex title-text view-vertical-center" style="margin-bottom: 10px;margin-top: 10px;">
				<text v-if="isUser">修改登录密码</text>
				<text v-else="isUser">修改登录密码</text>
				</view>
			</view>
		</view>
    <uni-list>
      <uni-list-item title="登录密码" showArrow rightText="点击修改登录密码"/>
      <uni-list-item title="交易密码" showArrow rightText="点击修改交易密码"/>
    </uni-list>
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
		.title-text {
			color: #FFFFFF;
			font-size: 18px;
			font-family: sans-serif;
			/* margin-top: 20px; */
		}
</style>
