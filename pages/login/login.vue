<template>
	<view>
		<view class="uni-flex view-center" style="margin-top: 5vh;">
			<image class="logo-img" src="../../static/logo.png" mode="scaleToFill"></image>
		</view>
		<view style="margin-top: 5vh;">
			<view>
				<text>手机验证码登录</text>
			</view>
			<view>
				<text>新用户验证通过后，自动注册帐号免密登录</text>
			</view>
		</view>
		<view class="uni-flex uni-column view-center" style="margin-top: 50px;">
			<view class="uni-flex uni-row input-box view-center">
				<uni-icons type="phone-filled"></uni-icons>
				<input class="input-input" placeholder="请输入手机号"/>
				<uni-icons type="closeempty"></uni-icons>
			</view>
			<view class="uni-flex uni-row input-box view-center">
				<uni-icons type="locked-filled"></uni-icons>
				<input class="input-input" password="true" placeholder="请输入密码"/>
				<uni-icons type="closeempty"></uni-icons>
			</view>
		</view>
		<view style="margin-top: 30px;">
			<button type="primary" class="submit-button">登录</button>
		</view>
		<view class="uni-flex uni-column view-center" style="margin-top: 2vh;">
			<view>
				<text>切换企业帐号</text>
			</view>
			<view>
				<text>帐号和密码登录</text>
			</view>
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
	.logo-img{
		width: 200px;
		height: 80px;
	}
	.input-box {
	    /* #ifndef APP-NVUE */
	    display: flex;
	    /* #endif */
	    padding: 10px 5px;
	    flex-direction: row;
	    flex-wrap: nowrap;
	    background-color: #ffffff;
		margin-top: 30rpx;
		width: 80vw;
		border: 2px solid #efefef;
	}
	.input-input {
	    height: 28px;
	    line-height: 28px;
	    font-size: 15px;
	    padding: 0px;
	    flex: 1;
	    background-color: #ffffff;
	}
	.submit-button{
		width: 80vw;
		border-radius: 10rpx;
		background-image:linear-gradient(to right,#3B92FF,#3958E1);
	}
</style>
