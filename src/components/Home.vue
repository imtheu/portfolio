<template>
	<div class="home">
		<hello></hello>
		<about></about>
		<works></works>
		<br>
		<br>
		<br>
		<br>
		<br>
	</div>
</template>

<script>

import Hello from './Hello.vue'
import About from './About.vue'
import Works from './Works.vue'

export default {
	name: 'Home',
	data () {
		return {
			msg: 'Welcome to Your Vue.js App'
		}
	},
	components: {
		Hello,
		About,
		Works
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.home{
		background: #FAFAFA;
	}
</style>
