<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
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
	page{
		height: 100%;
	}
	view,
	scroll-view,
	button,
	input,
	textarea,
	label,
	image {
		box-sizing: border-box;
	}
</style>
