<template>
	<header class="page-header container">
		<span class="middle-helper"></span>
		<router-link to="/"><img src="../../assets/logo.svg" alt="Matheus Francisco" class="logo"></router-link>
		<!-- <span class="middle-helper"></span> -->
		<span id="mainMenu"><mainMenu></mainMenu></span>
		
	</header>
</template>

<script>
	import mainMenu from './Main-Menu.vue'
	export default {
		name: 'page-header',
		components: {
			mainMenu
		}
	}

</script>
	
<style scoped>
	header{
		position: relative;
		height: 178px;
	}
	.middle-helper{
		display: inline-block;
	    height: 100%;
	    vertical-align: middle;
	}
	.logo{
		vertical-align: middle;
	}

	.inner-page{
		background: #212121;
		min-width: 100%;
	}
	.inner-page{
		height: 100px!important;
		text-align: center;
	}

	.inner-page .logo{
		width: 60px;
	}

	.inner-page #mainMenu{
		display: none;
	}
</style>