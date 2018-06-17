<template>
	<div id="app">
		<transition name="page" mode="out-in">
			<router-view/>
		</transition>
	</div>
</template>

<script>
	export default {
		name: 'App'
	}
</script>

<style>
	#app{
		background: #212121;
		overflow-x: hidden;
		min-height: 100vh;
	}
	.page-enter-active, .page-leave-active {
		transition: transform 0.8s linear;
	}
	.page-leave-to {
  		transform: translateX(-100%);
	}
	.page-enter {
		transform: translateX(100%);
	}

</style>
