<template>
	<view class="content">
		<Index/>
	</view>
</template>

<script>
	//import Index from "../../wxcomponents/index.vue";
	import Index from '../common/index'
	export default {
		components:{
			'Index' : Index
		},
		data() {
			return {

			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.content{
		padding-bottom: 64upx;
	}
</style>
