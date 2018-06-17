<template>
	<div id="Project">
		<page-header class="inner-page"></page-header>
		<article class="container mt-5">
			<header>
				<h1>{{ project.Name }}</h1>
				<ul id="tags"><li v-for="tag in project.Tags">#{{ tag }}</li></ul>
				<p>{{ project.Description }}</p>
			</header>
			<div class="row mt-5">
				<div class="col-md-7">
		    		<img class="img-fluid img" :src="getImg(project.Imgs['0'])" :alt="project.Name" :title="project.Name">
		    	</div>
		    	<div class="col-md-5 longdesc mt-3">
		    		<p v-html="project.Long_description"></p>
		    	</div>
	    	</div>
	    	<div class="row mt-5">
	    		<div class="col-md-4" v-for="(image, imgKey) in project.Imgs" v-if="imgKey > 0">
	    			<img class="img-fluid img" v-if="image"  :src="getImg(image)" :alt="project.Name" :title="project.Name">
	    		</div>
	    	</div>
		</article>
		<br>
		<br>
		<br>
		<br>
	</div>
</template>
<script>
	import pageHeader from '../includes/Page-Header.vue'
	import pageFooter from '../includes/Page-Footer.vue'
	import data from '../../data/data.json'
	export default{
		name: 'Project',
		components: {
			pageHeader
		},
		data () {
			return {
				id: '',
				project: []
			}
		},
		methods: {
			getImg: function(src){
				let images = require.context('../../imgs/');
				return images('./' + src);
			}
		},
		created: function(){
			this.id = this.$route.params.id;
			this.project = data.Projects[this.id];
			$('html, body').animate({
		        	scrollTop: 0
		    }, 200);
		}
	}

</script> 
<style scoped>
	*{
		font-family: Lato;
	}

	#Project{
		background: #FAFAFA;
		min-height: 97vh;
	}

	article header{
		border-left: 5px solid #685C79;
		padding-left: 20px;
	}

	article h1{
		color: #212121;
		font-size: 92px;
	}

	article p{
		font-size: 17px;
	}
	.img{
		box-shadow: 0px 0px 50px rgba(33, 33, 33, 0.05);
	}

	.longdesc p{
		font-size: 25px;
	}

	#tags{
		font-size: 11px;
		color: #616161;
		padding-left: 5px;
	}
	#tags li{
		display: inline-block;
		padding: 0 1.5px;
		list-style: none;
	}
</style>