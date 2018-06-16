<template>
	<div class="home">
		<hello></hello>
		<about></about>
		<works></works>
		<contact></contact>
		<page-footer></page-footer>
	</div>
</template>

<script>

import Hello from './Hello.vue'
import About from './About.vue'
import Works from './Works.vue'
import Contact from './Contact.vue'
import PageFooter from './includes/Page-Footer.vue'

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
		Works,
		Contact,
		PageFooter
	}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.home{
		background: #FAFAFA;
	}
</style>
