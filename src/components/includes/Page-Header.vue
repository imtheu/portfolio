<template>
	<header class="page-header container">
		<span class="middle-helper"></span>
		<img src="../../assets/logo.svg" alt="Matheus Francisco" class="logo">
		<!-- <span class="middle-helper"></span> -->
		<mainMenu></mainMenu>
		
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
</style>