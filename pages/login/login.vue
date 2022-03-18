<template>
	<view>
		<view style="text-align: center; margin-top: 300rpx;"> 
			<image src="../../static/ypi.jpg" style="width: 150rpx; height: 150rpx;"></image>
		</view>
		<view style="text-align: center; margin-top: 30rpx; font-size: 30rpx;">
			<text >欢迎使用智慧停车场小程序</text>
		</view>
		<view style="margin: 30rpx;">
			<input v-model="username" class="myinput" placeholder="请输入账号" />
			<input v-model="password" class="myinput" placeholder="请输入密码" password="true"/>
		</view>
		<view>
			<button style="margin-top: 30rpx;" @click="logincheck()">登录</button>
		</view>
	</view>
</template>

<script>
	import {loginurl} from '../../common/api.js'
	export default {
		data() {
			return {
				username:"",
				password:"",
				
			}
		},
		methods: {
			logincheck(){
				/* console.log("登录按扭OK"); */
				if(this.username==""||this.password==""){
					// console.log("");
					uni.showToast({
						title:"用户名密码不能为空",
						icon:"none"
					})
				}else{
					uni.request({
						
					})
				}
			}
		}
	}
</script>

<style>
	.myinput{
		background-color: #FFFFFF;
		height: 50rpx;
		font-size: 28rpx;
		padding: 15rpx 25rpx;
		margin-bottom: 30rpx;
	}
</style>
