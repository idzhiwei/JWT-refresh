<script>
	import userMessage from '@/store/userMessage.js';
	export default {
		onLaunch: function() {
			console.log('App Launch')
			if (!userMessage.state.loginStatus) {
				console.log('未登录，onLaunch 拦截去登录');
				uni.reLaunch({
					url: '/pages/login/login'
				})
			}
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
