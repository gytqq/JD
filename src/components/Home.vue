<template>
	<div>
		<div class="demo_list">
			<div class="demo_item" @click="toPath('/')">
				<img :src="this.$route.path === '/' ? require('../assets/5aa10cd2N46f18ce6.png') : require('../assets/5aa10cd2N1318ac50.png')" alt="">
			</div>
			<div class="demo_item" @click="toPath('/left')">
				<img :src="this.$route.path === '/left' ? require('../assets/060ffe532d67562b.png') : require('../assets/5aa10cdbNa9cd0320.png')" alt="">
			</div>
			<div class="demo_item" @click="toPath('/footer')">
				<img :src="this.$route.path === '/footer' ? require('../assets/5aa10cf6Nbfbdc1af.png') : require('../assets/5aa10ceaN649eec12.png')" alt="">
			</div>
			<div class="demo_item" @click="toPath('/daohang')">
				<img :src="this.$route.path === '/daohang' ? require('../assets/5aa10cf6Nbfbdc1af.png') : require('../assets/5af43af1N04ef5a16.png')" alt="">
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		methods:{
			toPath(path){
				this.$router.replace(path)
				console.log(this.$router)
			}
		}
	}
</script>

<style scoped lang="scss">
	.demo_list{
		width: 100%;
		height: 50px;
		background: palevioletred;
		position: fixed;
		bottom: 0;
		left: 0;
		display: flex;
		.demo_item{
			flex: 1;
			display: flex;
			justify-content: center;
			align-items: center;
			img{
				width: 70px;
			}
		}
	}
	.cla{
		color: red;
	}
</style>